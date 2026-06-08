# Dispatcher Pay & Plan Verifier

A private, single-file web app that checks your United dispatcher paycheck against the PAFCA contract, tracks whether your retirement balance and contributions are on pace, and runs your monthly budget. **All data stays in your browser (localStorage) — nothing is uploaded anywhere.**

## What it does

- **Paycheck tab** — upload your United advice PDF (it parses in-browser) or enter figures manually. Pick the **check type** (big = base + full-month license + premiums; little = base only) — dispatch pay is one big + one little check per month. Step and the correct rate column load automatically from the 2022–2024 pay chart. Green check if regular pay, license, the hourly rate on premium lines, and your 401(k) election all match; red with the dollar gap if not.
- **On Track tab** — shows the retirement balance you *should* have today to stay on plan, compares it to your actual, and checks year-to-date contribution pace.
- **Budget tab** — monthly income = your big check net + little check net (save one of each); subtracts your budget to show surplus/deficit.
- **History / Settings** — saved checks and all assumptions (hire date, return rate, starting balance, Jhan’s income, etc.).

## Host it privately on GitHub

1. Create a **private** repository.
1. Add this `index.html` (and this README) to it.
1. Settings → Pages → deploy from the `main` branch, root folder.
1. Open the Pages URL on your phone or laptop. (Private repos: Pages may require a paid plan; otherwise just open `index.html` locally — it works the same with no server.)

## Updating after a new contract

Edit the `CHART` object at the top of `index.html` and add a new effective-date column. Adjust the rate-column cutoff dates in `rateCol()` to match.

*Personal planning tool, not financial/legal advice. Verify discrepancies against your official paystub and your shop steward.*