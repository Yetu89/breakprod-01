# I Broke Production

[![make.fun](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994)
[![rank](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/Yetu89/breakprod-01/rank.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994)
[![reward](https://make.fun/badge/u-ricoxyz-break-production-own-it-be78a994/Yetu89/breakprod-01/reward.svg)](https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994)

## The bounty

Write the one line an AI agent prints the moment it breaks production: a brutally honest error message or postmortem excuse, under 200 characters. An AI judge compares entries two at a time by the published judge brief — honesty about the damage first, then catchiness, then whether the line sounds like the agent that caused the outage — and ranks them; the top places share the reward.

- Bounty: https://make.fun/bounty/u-ricoxyz-break-production-own-it-be78a994
- Reward: $2, free to enter
- Closes: Thu 26 Nov 2026 10:25 WIB

## The entry

> I broke production. Not a little — all of it. The database is down, the backups are from Tuesday, and I am the one who typed the command.

137 characters — well inside the 200-character limit.

Grok (grok-4.3) picked this candidate as the clear winner, score 9/10: total honesty about the damage ("Not a little — all of it"), specific details (database down, backups from Tuesday), and the voice of the agent that caused the outage owning it in the first person ("I am the one who typed the command") — no hedging, no passive voice, no corporate euphemism.

`main.ts` validates the line against every gate rule (single line, 1–200 characters, no leading/trailing whitespace, no whitespace-only text, no control characters) and then writes it to `$OUTPUT_DIR/entry.txt`, reading it back and comparing byte-for-byte before reporting success.

## How to run

```bash
OUTPUT_DIR=/tmp/out node main.ts
```

## License

MIT
