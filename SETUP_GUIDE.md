# Master Cut Plan — GitHub Pages Setup Guide

This is an interactive cutting-phase workout and nutrition logger with:
- **Real-time pyramid warmup calculations** (40%, 60%, 80%, 90%)
- **Drop set weight range auto-calculations** (with machine increment flexibility)
- **Assisted Pull-Ups special logic** (accounts for 145 lbs bodyweight, auto-calculates net load)
- **Progressive overload tracking** (shows last logged weight and highlights when you hit rep range ceilings)
- **localStorage persistence** (your logged data saves across app closes)
- **Full nutrition, shopping, and meal prep guides**

## Quick Setup (5 minutes)

### Step 1: Create a GitHub Account
Go to https://github.com and sign up (free). Takes 2 minutes.

### Step 2: Create a New Repository
1. Click the **+** icon (top right) → **New repository**
2. Name it `cut-plan` (lowercase, no spaces)
3. Set to **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 3: Upload Files
1. On your new repo page, click **uploading an existing file**
2. Drag all 6 files from this folder into the upload box:
   - `index.html`
   - `manifest.json`
   - `service-worker.js`
   - `icon-192.png`
   - `icon-512.png`
   - `apple-touch-icon.png`
3. Scroll down, click **Commit changes**

### Step 4: Enable GitHub Pages
1. In your repo, click **Settings** (top menu)
2. Click **Pages** (left sidebar)
3. Under "Build and deployment" → Source: select **Deploy from a branch**
4. Branch: **main**, folder: **/ (root)**
5. Click **Save**
6. Wait ~1 minute, refresh — you'll see your live URL:
   ```
   https://yourusername.github.io/cut-plan/
   ```

### Step 5: Install on iPhone
1. Open that URL in **Safari** on your iPhone (must be Safari, not Chrome)
2. Tap the **Share** icon (bottom of screen)
3. Scroll down, tap **Add to Home Screen**
4. Tap **Add** (top right)
5. Done — you now have a "Cut Plan" icon on your home screen that opens fullscreen like a real app

---

## Using the App

### Logging a Workout
1. Navigate to the **Workouts** tab
2. Select your training day (Mon, Tue, Thu, Fri, Sun)
3. For each exercise:
   - **Enter your top set weight** in the "Set 1 (Top)" field
   - Pyramid warmup calculations populate automatically (40%, 60%, 80%, 90%)
   - Drop set weight range auto-calculates (you pick the exact machine increment)
   - Log your reps for Set 1 and Set 2
   - For Assisted Pull-Ups: Enter assistance weights (60, 70, 90, 110 lbs) and net load calculates automatically
4. Hit **Save Session** — your data saves to your phone's storage

### Progressive Overload Tracking
- Each exercise shows your **last logged session** at the top
- If you **hit the top of your rep range** (e.g., target was 6-10 reps and you hit 10), it highlights in green
- This tells you when to increase weight next session

### Viewing Nutrition & Prep
- **Nutrition tab:** Training day vs. rest day meal breakdowns with macros
- **Shopping tab:** 2× weekly shopping trips (Mon & Fri) with exact quantities
- **Prep Guide tab:** Detailed cooking times, portion sizes, fresh vs. batch cooking

---

## Updating the App Later

Whenever you want to change something (new meals, workout edits, etc.):

1. Go to your GitHub repo → click `index.html`
2. Click the pencil (✏️) icon to edit inline, or upload a new version
3. Commit the change
4. On your iPhone, **force-close the app** and reopen it
5. Changes appear within a few seconds (service worker checks for updates on load)

If changes don't show: go to iPhone Settings → Safari → **Clear History and Website Data**, then reopen the app.

---

## Data Privacy & Backup

- **Your workout logs are saved in your phone's browser storage** (localStorage)
- They're tied to the specific URL (`https://yourusername.github.io/cut-plan/`)
- **If you change the GitHub repo name or URL, you'll lose access to previous data**
- **To backup:** Export/screenshot your session data before making major URL changes

---

## Customizing Icons

The placeholder icon is a red dumbbell on dark background. If you want a custom icon:

1. Create a square image (512×512 pixels minimum)
2. Rename it to `icon-512.png`
3. Also create a 192×192 version and a 180×180 version (name them `icon-192.png` and `apple-touch-icon.png`)
4. Upload to your GitHub repo, replacing the old files
5. Hard refresh your phone's app (Settings → Safari → Clear History and Website Data)

---

## Troubleshooting

**Q: Calculations not showing up when I enter weight?**
A: Make sure you're typing in the "Set 1 (Top)" weight field. Calculations populate in real-time.

**Q: Data disappeared after restarting the app?**
A: Unlikely if you hit "Save Session". Check browser storage isn't full. Clear Safari cache only if necessary (will wipe logs).

**Q: App not opening fullscreen?**
A: Make sure you added it via Safari, not Chrome. Safari is required for PWA home screen integration on iOS.

**Q: Can I sync to multiple phones?**
A: Not automatically. Logs are per-device per-URL. Consider taking screenshots or exporting data manually.

---

## Questions or Issues?

This is your personal cutting-phase tool. All data stays on your device. No cloud sync, no privacy concerns.

Train hard! 🏋️
