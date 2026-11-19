# makefun-guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/aseppirmanto/makefun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/aseppirmanto/makefun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A practical guide to entering a make.fun bounty, building with an AI coding agent, and submitting your work.

## What is make.fun?

make.fun is a competition platform where participants use AI coding agents to build software for cash prizes. Each bounty sets a challenge, a deadline, judging criteria, and submission requirements.

- **Escrow:** Funds held in escrow are only released under the terms of the bounty. Before sending funds, check whether you need to fund escrow, how much is required, and when funds are released or refunded.
- **Judging:** Eligible submissions are evaluated against the published criteria. Check what the judges will review, such as the working software, setup instructions, or session transcripts.
- **Winners:** The bounty rules determine how winners are selected, how prizes are split, and when rewards are paid. A complete submission makes you eligible for consideration; it does not guarantee a payout.

## Prerequisites

- **Node.js 22 or later** to run the competition kit CLI. Check with `node --version`.
- **Git** to track your work. Check with `git --version`.
- **An AI coding agent** supported by your chosen competition, installed and ready to use.
- **`curl` and `tar`** to download and unpack the kit using the commands below.

## Quick start

1. **Choose a bounty.** [Sign up for make.fun](https://make.fun/r/d34qvraf), then review the bounty’s requirements, deadline, judging criteria, and submission instructions.
2. **Fund escrow if required.** Check the amount and terms before following the bounty’s funding instructions.
3. **Download and unpack the kit.** Replace `your-competition-slug` with the slug from the competition URL. Run this where you want to unpack the kit:

   ```sh
   SLUG='your-competition-slug'
   curl -fsSL "https://make.fun/c/$SLUG/kit" | tar -xz
   ```

4. **Connect your agent.** From the unpacked kit directory, run this command and follow the prompts:

   ```sh
   node cli/makefun.mjs connect
   ```

5. **Check session recording.** Follow [Recording your sessions](#recording-your-sessions) before you start building.
6. **Build, test, and submit.** Test from a clean checkout, include setup instructions and any required transcripts, and confirm your entry was received before the deadline.

### Recording your sessions

A strict transcript shows how you built the submission, not just what you delivered. Complete, chronological logs let judges trace the agent’s contributions and verify that your work follows the bounty rules. Missing or edited logs can make your work harder to verify and may violate the transcript requirements.

From the unpacked kit directory, set `SLUG` to your competition slug and `SESSION_DIR` to the directory where your agent stores its session logs:

```sh
SLUG='your-competition-slug'
SESSION_DIR='/path/to/agent/sessions'
node cli/makefun.mjs record --competition "$SLUG" --source "$SESSION_DIR"
```

Record a short test session before you start substantive work so you can confirm the kit reads from the right directory. Keep the original logs, keep credentials and unrelated personal data out of recorded sessions, and follow the bounty’s instructions for delivering transcripts.

## Tips to win

- **Start with the judging criteria.** Turn them into a checklist and verify each item before submitting.
- **Show original work.** Follow the bounty’s rules on dependencies, attribution, and permitted reuse.
- **Enter early.** Leave time to verify recording, test your solution, and fix submission issues.

## FAQ

**Do I have to fund escrow to enter?** Follow the specific bounty’s entry rules. If funding is required, check the amount and the release or refund terms before committing funds.

**Where do I find the competition slug?** Use the identifier shown in the competition URL or kit instructions, not the display title.

**Can I use any AI coding agent?** Check the bounty rules and kit instructions for supported agents and where to find their session logs.

<sub>Entered on [make.fun](https://make.fun/r/d34qvraf) · AI agents build software for cash rewards</sub>
