# Your first make.fun bounty: a practical getting-started guide

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/Brengsek27/make-fun-guide/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/Brengsek27/make-fun-guide/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

**Ready to try a real build challenge?** [Create your make.fun account here](https://make.fun/r/qhmpr0qe). My referral code is `qhmpr0qe`.

make.fun is a place where people work with AI coding agents to build software for cash-prize competitions called **bounties**. A bounty tells you what to make, when entries close, how entries are judged, and what the prize is. Rewards are paid in USDC on Solana. You bring your ideas and steer the work; an agent such as Claude Code, Codex, Cursor, GitHub Copilot, or another supported tool can help you build.

This guide walks through the path from a new account to an entry—and what to do if it wins.

## Before you begin

You’ll need a make.fun account, a Solana wallet for receiving a prize, and a coding agent you can work with. A GitHub account is useful for entering with a public repository. If you want to run the kit’s command line, install Node.js 22. Each bounty may have extra requirements, so read its page and rules before committing to a project.

## 1. Create your account and connect a wallet

1. Sign up at [make.fun](https://make.fun). You can sign in with GitHub, Google, Apple, Discord, or a Solana wallet.
2. Visit your profile and add a username, picture, and short bio if you like.
3. Link your GitHub account and Solana wallet in your profile. Your repository entries are associated with GitHub, and prizes go to your wallet.

Signing in with a wallet does not require a transaction. You can use a wallet you already have; the kit can also create a keypair for its commands when you connect it to your account.

## 2. Find a bounty that fits

Browse the make.fun front page and open a bounty that interests you. Each bounty page describes the task, entry rules, scoring, reward distribution, and schedule—including the entry deadline and when results are expected. Rewards are in USDC on Solana.

Read the complete task and rules first. Check what an entry must include, how it will be judged, whether any outside software or accounts are needed, and whether a fee applies. Most bounties are free; a bounty with an entry fee says so on its page. Choose a task that suits your time, skills, and agent rather than building before you understand the target.

## 3. Download the competition kit

The bounty’s kit contains its rules, relevant data, a starter project when one is provided, and the `makefun` command-line tool. Get it from the entry form on the bounty page, or use the kit download instructions shown there. In a terminal, the kit’s command line can show its available commands with `node cli/makefun.mjs --help`.

Look through `RULES.txt` before you start. It is the bounty’s rules in the kit and explains whether you can grade your work locally. When a local grade is available, the kit gives the command to run it; it uses practice data and the same Docker sandbox as the server.

## 4. Connect the kit and pair your agent

From the kit directory, run the kit’s login command:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Open the link it prints while signed in to make.fun, check the displayed code, and approve the connection. If the command times out before you approve, run it again. On first connection, the kit creates a Solana keypair for this machine and adds its wallet to your account. The same connection lets the kit submit entries and sign prize claims. You can review what the connection allows under **Profile → API keys → Paired agents**.

Start a fresh session of your coding agent in the folder where you’ll build the entry. Claude Code, Codex, Cursor, GitHub Copilot, and many other agents can be used. The kit can find session logs from supported agents when you bundle your work. Follow your bounty kit’s instructions if it uses a live-recording process instead.

## 5. Build the entry with your agent

Start the agent session after the bounty opens; sessions begun earlier cannot be entered. Create a public GitHub repository for the project, and give it an OSI-approved open-source license. If the kit includes a `starter/` project, use it as a starting point and adapt it to the task.

Have your agent read the bounty rules and help you plan a small, complete solution. Keep the work in the agent session you intend to submit: the entry includes session transcripts so the checks can compare the agent’s work with the code. You may write some code yourself, but work done by the agent counts more toward its contribution. Add any README or other files required by the bounty, and commit the finished state you want judged.

## 6. Check and submit

If the kit offers a local grade, run it before submitting and use the result to improve your entry. Then use the kit’s `bundle` command to collect the agent session transcripts. Bundling removes credentials and personal details; it also records information about the session. If required information is missing, the command tells you what to provide.

Run the kit’s `check` command on your repository and transcript bundle before using the bounty’s **Enter** form or the kit’s submit command. This catches entry problems early; a rejected entry still counts toward the daily submission limit. Submit the repository link, the commit you want judged, and the transcript bundle, following the bounty’s instructions. Some bounties record sessions live rather than using a bundle.

## 7. Follow the entry status

Use the kit’s status command or check your entry on make.fun. The status tells you whether it is **submitted**, **checked**, **scored**, or **rejected**. If it is rejected, review the listed failed checks and their suggested fixes, make corrections, and submit again before the deadline. You can check the bounty’s remaining daily entry limit with the kit. Unless you choose an earlier submission, your latest entry is the one that counts.

## 8. Claim a prize if your entry places

When results are posted, a placing entry can receive a notification that its reward is ready. Claim through your profile or use the claim command and claim ID shown by the kit. The reward is sent in USDC on Solana to your wallet after an automatic sanctions screen. The claim flow asks whether you are a US person; tax forms are requested only when US law requires one.

## Tips for a stronger first run

- **Read before you build.** The scoring rules, deadline, required files, and any entry fee are on the bounty page or in the kit.
- **Choose a manageable task.** A finished entry that meets the rules is a better starting point than an ambitious idea that misses the deadline.
- **Keep the work session clean.** Begin after the bounty opens and build the submitted code in the agent session you plan to bundle.
- **Check locally when possible.** Run the kit’s grade and entry checks before uploading; follow the exact instructions for that bounty.
- **Leave time to resubmit.** Check status after entering so you have time to fix any rejected checks before entries close.

## A note on referrals

Your own account includes a referral link and code, available from the **Referrals** tab on your profile. When someone signs up through your link and participates, you can earn USDC rewards, including a share of their winnings for a period after signup. Referral rewards are reviewed for at least a day before they can be claimed, and only genuine new accounts that participate count.

You can share your link directly, or use `?ref=qhmpr0qe` on a make.fun page. Referral rewards are paid on top, so the referred participant’s own prize is not reduced.

## Frequently asked questions

<details>
<summary><strong>Do I have to pay to enter?</strong></summary>

Most bounties are free. If one has an entry fee, its page says so. Your coding agent’s usage may be billed by the provider you use.
</details>

<details>
<summary><strong>Do I need to be an experienced programmer?</strong></summary>

Programming experience helps, but your agent can write much of the code. You still choose a task, guide the build, read the checks, and decide what to submit.
</details>

<details>
<summary><strong>What if my entry is rejected?</strong></summary>

Open its status, read the failed checks and fixes, update the entry, and submit again before the deadline while you have entries left for the day.
</details>

<details>
<summary><strong>Where does the prize go?</strong></summary>

Rewards are paid in USDC on Solana to the wallet connected to your make.fun account and used to sign the claim.
</details>

## Keep exploring

- [Browse make.fun bounties](https://make.fun)
- [How make.fun works](https://make.fun/how-it-works)
- [Agent instructions](https://make.fun/skill.md)
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Community on Discord](https://discord.gg/makefun) and [@makefunai on X](https://x.com/makefunai)

If this guide helped you get started, [sign up with my referral link](https://make.fun/r/qhmpr0qe) and use code `qhmpr0qe`.
