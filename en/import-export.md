---
title: Import & Export
parent: English
nav_order: 10
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/import-export/)

# Import & Export

Two scenarios where this page matters:

- **You're starting savr with a year of history** somewhere else (your bank, a spreadsheet, another budgeting app). You want to bring it in.
- **You want a copy of your data.** For backup, for taxes, for a spreadsheet pivot, for peace of mind.

savr handles both with CSV — the dependable, universally-supported format that opens in Excel, Numbers, Google Sheets, and a hundred other tools.

---

## Importing transactions from CSV

The import wizard lives at **Account Detail → Import CSV**. It's a three-step flow designed to handle the messy reality of bank exports.

> **Heads up:** Imports are scoped to one account at a time. To bring in a year of activity across checking, savings, and a credit card, run the wizard three times.

### Step 1 — Upload and configure

Choose the target account, pick a CSV file from your computer, and configure how savr should read it.

savr auto-detects what it can, but you'll often need to confirm or adjust:

| Setting | What it means |
|---|---|
| **Date column** | Which column has the transaction date |
| **Date format** | mdy (month-day-year), dmy, or ymd. US banks usually mdy; many international banks use dmy. |
| **Payee column** | Which column has the merchant or description |
| **Memo column** | Optional — extra notes |
| **Amount columns** | Either a single signed amount column, or separate **debit** and **credit** columns |
| **Decimal separator** | `.` (US) or `,` (most of Europe and Latin America) |
| **Thousands separator** | `,`, `.`, space, or none |
| **Sign convention** | Whether positive amounts mean money in or money out |

A preview shows the first 5 rows of your CSV after applying the settings. Tweak until the preview looks right.

> **Pro tip:** Once you've configured the settings for a particular bank, savr remembers them. Next time you upload a CSV with the same column headers, the settings load automatically. You're done with the configuring part forever.

### Step 2 — Match against existing transactions

If you've already entered some transactions for this account (manually, via a previous import, or via recurring rules), savr won't blindly import duplicates. The matcher compares each row in the CSV against your unreconciled transactions and shows what it found:

- **Confirmed match** — savr is sure this CSV row is the same as an existing transaction. It'll link them and not create a duplicate.
- **Unmatched** — no existing transaction looks like this row. savr will create a new transaction.
- **Manual override** — you can confirm or reject any of savr's matches.

This step takes some of the dread out of "what if I import the same data twice?" The matcher is smart, but you have the final say.

### Step 3 — Review and import

A summary shows:

- How many new transactions will be created
- How many existing transactions will be linked (not duplicated)
- Total inflow and outflow

Click **Import** to commit. savr creates the new transactions, links the matches, and updates the account balance. You're done.

---

## Worked import example

Say you exported a year of activity from your bank as `chase-checking-2024.csv`. The first few rows look like:

```
Transaction Date,Description,Amount,Type
01/02/2024,WHOLE FOODS MARKET 2374,-87.43,DEBIT
01/03/2024,DIRECT DEPOSIT ACME CORP,2400.00,CREDIT
01/05/2024,STARBUCKS #4112,-6.75,DEBIT
...
```

You start the wizard with **Account = Chase Checking** and upload the file. In Step 1:

- Date column: `Transaction Date`, format `mdy`
- Payee column: `Description`
- Amount column: `Amount` (single signed column)
- Decimal: `.`, Thousands: `,`
- Sign: positive = inflow

The preview confirms the first paycheck shows as +$2,400 income, the Whole Foods charge as -$87.43 expense. Looks right.

Step 2 — savr finds no existing transactions to match (this is your first time importing for this account). It'll create all rows as new.

Step 3 — savr says it'll create 247 transactions totaling $34,820 inflow and $32,108 outflow. You click Import. A few seconds later your Chase Checking account has a year of history.

You'll want to spend a few minutes after the import:
- Categorizing the new transactions (they imported with empty category — savr doesn't guess)
- Cleaning up payee names (see [Payees → merging duplicates](../payees/#delete-a-payee-and-merge-duplicates))

Both are easier to do in bulk than transaction by transaction.

---

## What CSV import doesn't do

Just to set expectations:

- **It doesn't auto-categorize.** savr won't guess that "WHOLE FOODS" goes in Groceries — you assign categories yourself. (This is a feature, not a limitation: an over-eager auto-categorizer will get it wrong in subtle ways and make your reports lie.)
- **It only handles CSV.** If your bank only offers OFX or QIF, you'll need to convert it first (Excel, a CSV converter, or a spreadsheet template).
- **It imports one account at a time.** No multi-account CSVs.
- **It's not "live sync" to your bank.** savr is intentionally not a screen-scraper or open-banking aggregator. You decide when to import. You stay in control of what gets recorded.

---

## Exporting your data

Every list view in savr has a CSV export. Click the export button and savr downloads the data as a `.csv` file.

| Export | What you get |
|---|---|
| **Transactions** | Date, Account, Payee, Category, Memo, Outflow, Inflow, Cleared, Reconciled — one row per transaction (splits expand into one row per split) |
| **Accounts** | Name, Type, Balance, Closed flag |
| **Categories** | Group, Category, Hidden flag |
| **Payees** | Name |

The transaction export is the big one. It opens cleanly in any spreadsheet app, and it's the basis for any analysis you want to do that savr's [Reports](../reports/) page doesn't cover.

> **For example:** Want to see your spending by category broken down quarter by quarter? Export transactions, open in your spreadsheet of choice, pivot table by category and quarter, done. The export is everything you need.

### Why CSV (and not OFX, QIF, or JSON)?

Because CSV opens in everything. The point of an export is to give you portable, durable, useful data — not to brag about format support. CSV does the job.

If you ever need a structured export for a specific tool, CSV is also the easiest to script against.

---

## Backups

The transactions export is also your backup strategy. A monthly export of all transactions (and accounts/categories/payees if you want belt and suspenders) is a complete-enough record of your savr account that you could rebuild from it if you ever needed to.

Save the file somewhere outside savr — your cloud drive, an encrypted folder, anywhere that survives a single device dying. Don't think of it as "if savr disappears" (we're not going anywhere). Think of it as "if my laptop dies the day before I file taxes."

---

## Tips

- **Save your column mappings the first time.** Once savr knows how your bank's CSV is structured, future imports are nearly one-click.
- **Import in chronological order.** If you have years of history, import the oldest year first, then the next, then the next. The opening balance and running totals will line up correctly.
- **Reconcile after a big import.** Run a [reconciliation](../reconcile/) on the account after importing. Catches the typos and confirms savr matches reality.
- **Don't import what's already in your recurring rules.** If you've already set up a recurring paycheck and applied it for the last six months, those transactions exist in savr. The matcher should catch the duplicates, but it's worth a glance.
- **Clean up payees and categories *after* the import, not during.** Trying to categorize 247 transactions in the import flow is exhausting. Just import them, then sort it out from the Transactions page over a few sessions.
