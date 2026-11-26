# Goal Tracker

A private savings goal tracker in a single HTML file. Set a goal, bring in your bank transactions, approve each one by hand, and see how much you need to save and how much you have spent.

> **Disclaimer:** Goal Tracker records and calculates the figures you give it. It is not financial advice, and it is provided as is, without warranty. Check its numbers against your bank statements, and keep an encrypted backup and its password somewhere safe.

## Use it

1. Open the live app at https://immohit6.github.io/goal-tracker/ or download `index.html` and save it somewhere permanent.
2. Open it in Chrome, Safari or Firefox. The app opens directly to Home.

If you already have a Goal Tracker vault, use your existing passcode or Face ID, if configured, once to move your data to the new storage. Future visits in that browser open directly to Home.

Your data stays in that browser on that device. A different browser, a private tab, a different home-screen icon or a different device starts empty unless you restore a backup. Pick one way to open the app and stick to it.

**On iPhone** you can open the app link in Safari, tap Share, then Add to Home Screen. Use that icon from then on. You can save your backup file to iCloud Drive.

To make a portable backup, open Settings, tap **Back up now** and choose a backup password with at least eight characters. Tap **Prepare backup**, then **Save backup** to save the encrypted file. Keep its password somewhere safe so you can restore the file later.

To recover your data, open Settings and choose **Restore backup**. Enter the password you chose for that file. If you made the backup before this update, use the app passcode you had when you made it.

## What it does

- **Goal:** target, deadline and amount already saved. Shows what you need to save per day, week and month, and whether you are ahead of or behind schedule. It also shows a safe-to-spend figure for today: your recent income per day, minus the saving per day your goal needs, minus what you have spent today.
- **Approve:** imported transactions wait in a queue. You approve, reject or skip each one and set its category and whether it is personal or business. Only approved items reach the report.
- **Add:** type in income and expenses, or import a bank CSV (CBA-style export with no header row, or any CSV with date, description and amount or debit and credit columns). Duplicates are skipped.
- **Shifts:** a week at a time. Pick a day from the strip at the top, then tap the shifts you work that day (Narracan AM or PM, Menorock AM 7.5h, AM 5.5h or PM, Uber). The expected amount shows on the shift and in a running weekly total, and you can type a different amount for a slow or busy day. Copy last week repeats the previous week in one tap, and Quick fill ticks many days at once. Narracan and Menorock start with their own rates, allowances and shift lengths, and Uber starts at $150 a day; change any of them under Workplaces. Public holiday rates, overtime and super are not included.
- **Income bars:** the Goal screen shows two bars for this week or this month: Expected (from the shifts you ticked) and Actual (approved personal income). Pay usually lands after the shift, so Actual trails Expected.
- **Weekly review:** a button on the Goal screen shows the last 7 days (expected against actual income, spending, saving against what the goal needs), next week's planned shifts and bills due in the next 7 days.
- **After-tax pay:** each workplace can use the official ATO PAYG withholding tables (Schedule 1, weekly coefficients published 17 June 2026) entirely offline, with or without the tax-free threshold, or a flat percentage. Tax is worked out per week per job like a payslip and includes Medicare levy but not HELP/HECS. Uber has no withholding by default. Figures are estimates: your payslip is the source of truth, and the tables need updating each 1 July.
- **Next pay:** give a workplace its pay cycle (every 7 or 14 days, a known payday) and the Goal screen estimates the next pay from the shifts in that pay period.
- **Regular payments:** the Report tab lists expenses that repeat weekly, fortnightly or monthly at a steady amount.
- **Daily reminder:** Settings can add a repeating 9am event to your Calendar. The app cannot send notifications itself, because it never connects to a server.
- **Report:** expenses, income and net by period, filtered to personal, business or both, with a spending breakdown.

Keyboard shortcuts on the Approve screen: A approves, R rejects, S skips.

## Privacy

- The app encrypts your data with AES-256-GCM. The browser keeps the device key in IndexedDB so it can open Goal Tracker automatically. Anyone with access to that browser profile can open the app.
- The page has a Content Security Policy that blocks all network requests. It cannot send your data anywhere.
- Settings can save and restore password-protected backup files. Store CSV exports carefully because they contain your transactions in plain text.
- Delete the bank CSV from your disk after importing it.

## Not built yet

- Live bank sync (Australian Open Banking through an accredited provider).
- Recurring bill detection.
- Multiple goals.

## Licence

MIT. See `LICENSE`.
