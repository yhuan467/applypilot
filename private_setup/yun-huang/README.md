# Yun Huang ApplyPilot Setup

This folder contains a private ApplyPilot starter setup for Yun Huang.

Do not publish or commit this folder if you want to keep personal details private.

## Included Files

- `candidate_profile.json`: source-of-truth candidate facts.
- `application_rules.md`: screening and handoff rules.
- `resume_routing.md`: resume selection strategy.
- `answer_bank.md`: reusable truthful wording.
- `dashboard/`: CSV dashboard for trials and real runs.

## Current Run Mode

- Setup mode: `Volume`
- First trial boundary: `Lead finding only`

That means the first run should:

- Find 3-5 jobs.
- Classify them as `Pending`, `Needs user`, or `Skipped`.
- Update the dashboard.
- Avoid opening real application flows.
- Avoid submitting applications.

## Recommended Prompt

Use this with an agent:

```text
Use ApplyPilot with /Users/katiehuang/Desktop/BSS-research/applypilot/private_setup/yun-huang.
Run a lead-finding-only trial for 3-5 fresh entry-level roles that fit my rules.
Search LinkedIn, company sites, Simplify, and Handshake.
Update the dashboard, but do not open application flows or submit anything.
```

## When the Agent Must Stop

The agent should stop and hand off for:

- CAPTCHA, Cloudflare, login, or 2FA.
- Work authorization wording that does not match the stored profile.
- Compensation requests outside the stored range.
- Missing files or unclear uploads.
- Sensitive legal or identity questions.
- Final submit.

## Next Improvements

- Split the technical resume into separate SWE and ML variants if needed.
- Add a portfolio URL if you want it reused automatically.
- Add company preferences once you see what kinds of roles convert best.
