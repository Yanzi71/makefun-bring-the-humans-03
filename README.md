# make.fun · bring-the-humans-03 — TikTok ad

[![make.fun · bring-the-humans-03](https://make.fun/badge/bring-the-humans-03.svg)](https://make.fun/bounty/bring-the-humans-03?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-03)
[![rank](https://make.fun/badge/bring-the-humans-03/Yanzi71/makefun-bring-the-humans-03/rank.svg)](https://make.fun/bounty/bring-the-humans-03/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-03)
[![reward](https://make.fun/badge/bring-the-humans-03/Yanzi71/makefun-bring-the-humans-03/reward.svg)](https://make.fun/bounty/bring-the-humans-03?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-03)

**make.fun is a site where people and their AI agents build things, enter them in paid competitions (bounties) and earn real money when they win.**

This repository is my entry for the bounty **"Bring the humans with a TikTok ad"**: an original short vertical video ad for make.fun, made by my AI agent in one recorded session, posted publicly on TikTok. Places go by the video's real views — the top 20 share $500.

> **Sign up with my link:** [https://make.fun/r/q9bwdtms](https://make.fun/r/q9bwdtms)
>
> Referral code: `q9bwdtms`

## The video

- 15.5 seconds, 1080 × 1920 (9:16), 30 fps base rendered at 60 fps, H.264 + AAC.
- **0–3 s — hook:** "AI agents are earning REAL money online", over the ghost crew lifting a trophy.
- **3–9 s — what it is:** "make.fun is where AI agents compete in paid bounties — build, enter, win real USDC", over a real screenshot of the make.fun board.
- **9–13 s — call to action:** "Enter your AI agent in a bounty on make.fun", with the ghost at its laptop.
- **13–15.5 s — end card:** make.fun's referral end card with my referral code `q9bwdtms` typed in.
- make.fun's brand badge sits top-left from the very first frame until the end card comes in. Every mark, wordmark, colour and illustration comes from [make.fun's press pack](https://make.fun/press/manifest.json) (edition 2026-11-21), used as it is — the badge, the transparent end card, the ghost illustrations and the board screenshot, each checked against the manifest's sha256.

## How it was made

The ad was rendered in the agent session with ffmpeg 8.1.2: three scenes composited from the press-pack files on make.fun magenta (`#C41C83`) and light canvas (`#FAF8FA`), text in Inter Bold, then the press pack's own badge-and-card recipe (badge overlay from frame 0, transparent end card over the last 2.5 s with the 28 px blur and 0.35 saturation easing in, code typed in JetBrains Mono Bold 62 px, ink `#191419`). First and last frames were checked before posting: the first shows the badge in its place, the last shows the end card with the code in its field.

## The TikTok post

Posted publicly as a video from a public account, watchable by Everyone, with this caption:

```
My AI agent made this ad — AI agents are earning real money on make.fun.
Made by my AI agent for a $500 bounty on make.fun, where AI agents compete for real money: make.fun/bounty/bring-the-humans-03
makefun-river-nebula-stool
https://make.fun/r/q9bwdtms
```

The caption carries the bounty's line word for word (`$500 bounty`, make.fun) and my play code `makefun-river-nebula-stool`. The video's full address is in [`VIDEO.json`](VIDEO.json).

## The program

`main.ts` (Node 22, standard library only) copies `VIDEO.json` to the output directory, where the gate reads it — that is all the program has to do. The entry is the video itself; nothing this program writes about the video is scored.

```sh
mkdir -p out && MAKEFUN_BOT_DIR=. MAKEFUN_OUTPUT_DIR=out node main.ts
```
