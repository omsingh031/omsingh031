# Setup Instructions

This folder is a ready-to-push GitHub **profile README repo**. Follow these steps exactly.

## 1. Create the special repo
- Go to GitHub → **New repository**
- Name it **exactly**: `omsingh031` (must match your username character-for-character)
- Make it **Public**
- Do NOT initialize with a README (you already have one here)

GitHub will show a banner: *"omsingh031/omsingh031 is a ✨ special ✨ repository"* — that confirms it's set up correctly and will render on your profile page.

## 2. Push these files
From this folder, run:
```bash
git init
git remote add origin https://github.com/omsingh031/omsingh031.git
git add .
git commit -m "Initial profile README"
git branch -M main
git push -u origin main
```
(If your default branch is `master` instead of `main`, adjust the workflow trigger in `.github/workflows/snake.yml` — currently set to trigger on push to `master`.)

## 3. Enable workflow permissions (required for both workflows to push their generated files)
- Go to your new repo → **Settings → Actions → General**
- Scroll to **Workflow permissions**
- Select **Read and write permissions**
- Save

Without this, the snake and 3D-contribution workflows will fail with a permissions error when they try to push generated files back to the repo.

## 4. Run the workflows once manually (optional, speeds things up)
- Go to the **Actions** tab in your repo
- Click **generate animation** → **Run workflow**
- Click **GitHub-Profile-3D-Contrib** → **Run workflow**
- Both will otherwise run automatically on a schedule (every 24h) or on next push

## 5. What each file does
| File | Purpose |
|---|---|
| `README.md` | Your profile README — renders on github.com/omsingh031 |
| `.github/workflows/snake.yml` | Generates the animated "snake eating your contribution graph" SVG, pushed to an `output` branch |
| `.github/workflows/profile-3d.yml` | Generates a 3D isometric contribution graph, committed directly into `profile-3d-contrib/` in this repo |

## 6. Things you can still customize
- **Cert badges**: currently shields.io text-badges. Send me the public verification links (Credly URL for AWS, Oracle CertView link, NPTEL certificate page) and I'll swap in the real badge artwork.
- **LeetCode/Codeforces handles**: not included yet since you haven't shared them — send them and I'll add a LeetCode stats card + Codeforces rating badge.
- **GitHub stats privacy**: if your GitHub stats are set to private in account settings, the stats/streak cards will show 0s — make sure "Private contributions" visibility allows the stats services to read your activity (this is a public-data read, not a security risk).
