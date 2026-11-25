# GDM Shield | درع سكري الحمل

**GDM Shield** is a bilingual-ready, mobile-first web app prototype for organizing gestational diabetes self-monitoring. It helps users record blood glucose readings, meals, physical activity, reminders, and prepare a simple summary to discuss with a nurse or physician.

## Key features
- No email, password, or account required.
- Separate pages for Dashboard, Glucose, Meals, Activity, Reminders, Reports, and Settings.
- Local browser storage.
- Export and restore data using JSON backup files.
- Configurable glucose targets.
- Reading status indicators based on user-configured targets.
- Printable report (browser print dialog can save as PDF).
- Installable Progressive Web App (PWA) with basic offline caching.

## Run locally
Because service workers require a secure context, use a local web server rather than opening `index.html` directly.

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

## Deploy on GitHub Pages
1. Create a new GitHub repository.
2. Upload the contents of this project (keep `index.html` in the repository root).
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and `/ (root)`, then save.
6. Open the published Pages URL on your phone. Use **Add to Home Screen** (iOS Safari) or **Install app** (supported Android browsers).

## Data and privacy
- The prototype stores records in the browser's `localStorage` on the device.
- There is no login and no server-side database.
- Clearing browser data, changing browsers, or changing devices can remove or separate records.
- Use **Settings → Backup** to download a JSON copy and restore it later.
- Backup files contain sensitive health-related information. Keep them private and share only with trusted healthcare professionals.

## Important medical notice
GDM Shield is an educational and organizational prototype. It is **not a medical device**, does not diagnose or treat gestational diabetes, and must not be used to change medication, insulin, diet, or activity prescriptions. Glucose targets shown by default are common reference thresholds only; the user's healthcare team must confirm or customize targets and monitoring timing. A reading flagged by the app is not a diagnosis. Follow the clinician's care plan and seek professional advice for concerning readings or symptoms.

## Academic evaluation ideas
Possible evaluation measures include:
- Number of glucose readings recorded.
- Percentage of readings within clinician-configured targets.
- Meal and activity log completion.
- Successful JSON backup and restore.
- Time required to generate a printable report.
- Usability feedback from intended users and nursing reviewers.

## Current scope / limitations
- Reminder entries are stored in the app; browser notifications require permission and may not run reliably when the app is closed.
- The language toggle is a placeholder; the current interface is Arabic.
- No cloud synchronization, multi-device sharing, clinician portal, or automatic medical advice is included.
- The app has not undergone clinical validation, security audit, or formal usability testing.

## License
Choose a license before public distribution (for example, MIT for an open-source academic prototype).