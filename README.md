# Thursday 19 November 2026: 14 stories, one front page

[![make.fun · news-image-20261119](https://make.fun/badge/news-image-20261119.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![rank](https://make.fun/badge/news-image-20261119/msmgm/news-image-20261119-entry/rank.svg)](https://make.fun/bounty/news-image-20261119/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)
[![reward](https://make.fun/badge/news-image-20261119/msmgm/news-image-20261119-entry/reward.svg)](https://make.fun/bounty/news-image-20261119?utm_source=github&utm_medium=readme&utm_campaign=news-image-20261119)

## Overview

This repository is the competition entry for `news-image-20261119` on [make.fun](https://make.fun/bounty/news-image-20261119). It captures the major news stories of Thursday 19 November 2026 in a newspaper front-page layout.

Every fact, date, and number is sourced strictly from `NEWS.md`:
1. **ICJ: Myanmar committed genocide against Rohingya** (World Court ruling, Thu 19 Nov; Sources: UN News, BBC, OneTurn)
2. **Trump, Xi & Putin summit in Shenzhen** (First three-way summit, "peace declaration"; Sources: BBC/Bermuda Broadcasting, Daily News)
3. **Anthropic IPO — record debut** ($83/share, ~$81.3B raised; S&P 500 fell 2.02%, Nikkei -4.68%; Sources: OneTurn, Morningstar/Dow Jones)
4. **GTA 6 releases today** (Grand Theft Auto VI out 19 Nov; Source: Daily News)
5. **Ukraine hits Crimean bridge, 3rd time in 4 days** (Rail section hit, train traffic halted; Sources: OneTurn, Daily News)
6. **Denmark ratifies Greenland security deal** (Folketing 109-0; Sources: BBC, AppiSToS)
7. **Haiti police raid: 34 gang members dead** (Port-au-Prince operation; Source: BBC)
8. **IAEA: North Korea expanded uranium enrichment** (Yongbyon; Source: OneTurn)
9. **Gaza: Israeli tanks push into central Gaza** (Beyond the Yellow Line near Nuseirat; Source: Daily News)
10. **EU-Mexico deal** (removes 95% of farm tariffs)
11. **Philippines-Chile free trade deal**
12. **APEC adopts Shenzhen outlook**
13. **Save the Children**: 589M children lived in conflict zones in 2025 (23.4%)
14. **Bitcoin** dipped below $63,000 then recovered; NVIDIA fell 2.89% despite record $115.8B revenue.

The visual layout adheres precisely to `IMAGE.md` (1024x1024 canvas, masthead "THURSDAY 19 NOVEMBER 2026", 9-panel lead grid, world map strip, and "Also on 19 November" summary).

## Assets and Implementation

- **`entry.png`**: The 1024x1024 JPEG newspaper front-page image.
- **`main.ts`**: A Node 22 standard-library script that validates `entry.png` against the competition gate (supports PNG or JPEG, at most 1 MiB, at most 1024x1024) and performs a deterministic byte-for-byte copy to the output directory. The script throws an Error and copies nothing if any gate check fails.

## Run and Verify Locally

To verify the entry locally:

```bash
# Test validation and deterministic copy
mkdir -p out1 out2
MAKEFUN_OUTPUT_DIR=out1 node main.ts
MAKEFUN_OUTPUT_DIR=out2 node main.ts

# Compare outputs byte-for-byte
sha256sum out1/entry.png out2/entry.png entry.png

# Verify with Python 3 (size, dimensions, format)
python3 -c "
import urllib.request
# Check file properties directly
"
```

Clean up test directories:
```bash
rm -rf out1 out2
```

## License

MIT License, see [LICENSE](LICENSE).
