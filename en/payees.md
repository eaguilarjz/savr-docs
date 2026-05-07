---
title: Payees
parent: English
nav_order: 7
---

> {% include lang-globe.html %} Lee esta página en [Español](../../es/payees/)

# Payees

Payees are the people, businesses, or services on the other end of a transaction. The grocery store. Your landlord. That subscription service. Your employer (yes — your employer is a "payee" on your incoming paychecks too).

Payees are optional in savr. You can run a fine budget without ever using them. But they make a few things easier — and once you start using them, you'll wonder why you ever didn't.

---

## When payees actually pay off

Payees are most useful for:

- **Spending pattern questions.** "How much did I actually spend at this restaurant last year?" One filter, instant answer.
- **Filtering on the Transactions page.** Track all the activity with a specific party.
- **Finding duplicates.** When you see "Whole Foods" with 47 transactions and "WHOLE FOODS MARKET" with 3, those are the same place — merge them.

If neither of those sounds compelling, skip payees. savr won't nag you.

---

## Create a payee

Two ways:

### Inline, while creating a transaction

In the transaction dialog's **Payee** field, just type a name. If it doesn't exist, savr creates it automatically when you save the transaction. This is how most people build their payee list — naturally, as they record activity.

### From the Payees page

1. Open **Payees**.
2. Use the **New payee** form at the top.
3. Type a name and save.

Names are case-sensitive but otherwise free-form. Aim for the form you'd recognize at a glance: "Whole Foods", "Spotify", "Acme Corp Payroll", not "WHL FDS MKT 2374 NW PORTLAND OR" (we see you, bank export).

---

## Edit a payee

Click any payee name in the list to edit it inline. Press Enter to save. The change applies everywhere the payee is referenced — transactions, recurring rules, filters.

This is how you clean up bank exports that mangled the name. Edit "WHL FDS MKT 2374" → "Whole Foods" and every related transaction updates.

---

## Delete a payee (and merge duplicates)

Click the delete action on a payee row.

- **If the payee has no transactions**, it's deleted immediately.
- **If the payee has transactions**, savr opens a **reassign** modal:
  1. Pick another payee to take over its transactions (or choose **None** to clear the payee field).
  2. Confirm.

Either way, no transactions are lost — they're just relinked. Then the original payee is removed.

> **Merging duplicates:** Want to merge "Whole Foods Market" into "Whole Foods"? Delete "Whole Foods Market" and reassign its transactions to "Whole Foods." Both lists update. The transactions stay where they were (in their right categories, with their right amounts) but now they're all under one canonical payee.

> **Worked example:** You import a year of bank transactions and end up with 14 variants of Amazon: "Amazon", "AMAZON.COM", "Amazon Prime", "Amzn Mktp", "AMAZON DIGITAL," and so on. Spend five minutes deleting each one with reassignment to a single canonical "Amazon" payee. Now you can see at a glance that you spent — gulp — $3,847 at Amazon last year. (You're welcome.)

---

## Transaction count

Each payee on the list shows how many transactions reference it. Use this to spot:

- **Duplicates** — two near-identical names with low counts each are usually the same payee. Merge them.
- **One-offs** — payees with a single transaction may not be worth keeping in your list. You can leave them, ignore them, or clean them up.

---

## Tips

- **Don't over-curate.** Payees are a side effect of recording transactions. Let them accumulate naturally and clean up periodically. A 10-minute payee cleanup once a quarter is plenty.
- **Use a consistent style.** Pick a casing convention and stick with it (e.g. always title case). Easier to scan, easier to keep duplicates from sneaking in.
- **Income payees count too.** "Acme Corp Payroll" or "Freelance Client X" on income transactions makes year-end review *much* easier when you're trying to remember who paid you what.
- **Bank exports lie.** Bank-provided merchant names are often abbreviated, padded, or mangled. After a CSV import, expect to spend a few minutes cleaning up payee names — it's normal.
