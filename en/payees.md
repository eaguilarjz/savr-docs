---
title: Payees
parent: English
nav_order: 7
---

> 🌐 Lee esta página en [Español](../es/payees/)

# Payees

Payees are the people, businesses, or services you pay (or receive money from). They're optional on transactions but useful when you want to track who you're spending money with — the local grocery store, your landlord, a specific subscription service, or your employer for incoming paychecks.

The Payees page lists every payee you've created or used, along with how many transactions reference each one.

---

## When to use payees

Payees are most valuable in two scenarios:

- **Tracking spending patterns** — over time, payees give you a sense of "I've spent how much at this restaurant?" without you having to dig through transactions.
- **Filtering** — on the Transactions page, you can filter by payee to see all activity with one party.

If you don't care about either, you can skip payees entirely. savr doesn't require them.

---

## Create a payee

Two ways:

### Inline, while creating a transaction

In the transaction dialog's **Payee** field, type a name. If it doesn't exist, savr creates it automatically when you save the transaction. This is the fastest way to build out your payee list naturally as you record activity.

### From the Payees page

1. Open **Payees**.
2. Use the **New payee** form at the top.
3. Type a name and save.

Names are case-sensitive but otherwise free-form. Aim for the form you'd recognize at a glance: "Whole Foods", "Spotify", "Acme Corp Payroll".

---

## Edit a payee

Click any payee name in the list to edit it inline. Press Enter to save. The change applies everywhere the payee is referenced — transactions, recurring rules, filters.

This is the cleanest way to merge variants ("WHOLE FOODS MARKET" → "Whole Foods") into a single canonical name.

---

## Delete a payee

Click the delete action on a payee row.

- **If the payee has no transactions**, it's deleted immediately.
- **If the payee has transactions**, savr opens a **reassign** modal:
  1. Pick another payee to reassign all transactions to (or choose **None** to clear the payee field).
  2. Confirm.

Either way, no transactions are lost — they're just relinked or unlinked. Then the original payee is removed.

> **Merging payees:** To merge "Whole Foods Market" into "Whole Foods", delete "Whole Foods Market" and reassign its transactions to "Whole Foods". Both lists' counts update accordingly.

---

## Transaction count

Each payee on the list shows how many transactions reference it. Use this to spot:

- **Duplicates** — two near-identical names with low counts each are usually the same payee. Merge them.
- **One-offs** — payees with a single transaction may not be worth keeping in your list. You can leave them or clean them up.

---

## Tips

- **Don't over-curate.** Payees are a side effect of recording transactions. Let them accumulate naturally and clean up periodically.
- **Use a consistent style.** Pick a casing and stick with it (e.g. always title case). It makes the list easier to scan.
- **Income payees count too.** "Acme Corp Payroll" or "Freelance Client X" on income transactions makes year-end review much easier.
