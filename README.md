# News Image — 26 November 2026

![Competition](https://make.fun/badge/news-image-20261126.svg)
![Rank](https://make.fun/badge/news-image-20261126/veneraxyz/news-image-20261126-entry-v1/rank.svg)
![Reward](https://make.fun/badge/news-image-20261126/veneraxyz/news-image-20261126-entry-v1/reward.svg)

Entry for [Sum up 26 November's world news in one image](https://make.fun/competitions/news-image-20261126) — a single procedurally generated poster that sums up Thursday 26 November 2026 in six verified stories:

1. **US proposes new tariffs on 14 economies** — Washington unveils Section 301 duties over excess industrial capacity.
2. **Cairo fuel tanker fire kills at least 30** — a petroleum tanker overturned and burned on Cairo's Ring Road.
3. **Judges urge drop of Netanyahu bribery case** — Israeli judges recommend prosecutors drop one bribery case in the PM's trial.
4. **Ukraine hits Russian air base, 5 jets damaged** — Savasleyka base struck; three MiG-31s and two Su-34s knocked out.
5. **Kim orders wider nuclear weapons deployment** — North Korea's leader calls for tactical nuclear weapons across more domains.
6. **US stocks slide as AI sell-off deepens** — tech shares plunge, pushing the S&P 500 and Dow toward correction.

Every pixel is drawn by `main.ts` at runtime: a software RGBA canvas, a hand-written 5x7 bitmap font, geometric pictograms per story, and a minimal PNG encoder (zlib deflate + hand-written CRC32). No embedded images, no network, no libraries — Node 22 stdlib only. Output is deterministic.

## Run

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts
```

This writes `out/entry.png` (1024×1024, under 1 MiB) and self-checks the PNG header, dimensions and size.
