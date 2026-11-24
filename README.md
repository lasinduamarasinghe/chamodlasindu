# Chamod Lasindu – Portfolio

A static portfolio site (plain HTML + CSS, no build step).

## Project structure

```
index.html        ← all the text/content of the site
css/style.css     ← all colors, fonts, sizes, layout
images/me.png     ← your hero photo (transparent PNG)
```

## Host it on GitHub Pages (free)

### Option A – Browser only (easiest)
1. Go to https://github.com/new and create a **public** repository.
   - To get the address `https://YOUR-USERNAME.github.io`, name it exactly `YOUR-USERNAME.github.io`.
   - Any other name also works; the site will then live at `https://YOUR-USERNAME.github.io/REPO-NAME/`.
2. Click **uploading an existing file**, then drag in **everything from this folder**
   (`index.html`, `css/`, `images/`, `README.md`). Keep the folder structure.
3. Click **Commit changes**.
4. Open **Settings → Pages**. Under *Build and deployment*, set
   **Source: Deploy from a branch**, **Branch: `main`**, **Folder: `/ (root)`**, then **Save**.
5. Wait 1–2 minutes. Your live link appears at the top of the Pages screen.

### Option B – Git command line
```bash
cd portfolio
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```
Then do step 4 above (Settings → Pages).

### Updating the site later
Edit a file → commit → push (or edit directly on GitHub with the ✏️ pencil icon).
The live site refreshes within a minute or two.

## How to edit each part

Open `index.html`. Each block starts with a comment such as `<!-- ===== HERO ===== -->`.

| What you want to change | Where |
|---|---|
| Top bar text ("WEB DESIGNER", "AVAILABLE FOR FREELANCE") | `TOP BAR` block |
| Name, role, intro paragraph, location line | `HERO` → `<div class="hl">` |
| Hero photo | Replace `images/me.png` (same name), or change `src="images/me.png"` |
| Big background word "PORTFOLIO" | `<div class="big">` |
| Stats (3+ years, 40+ projects, 20+ clients) | `<div class="stats">` |
| Tagline next to the photo | `<div class="tag">` |
| Project cards (title, category, link) | `SELECTED PROJECTS` → each `<a class="card" href="#">` |
| Education entries | `<div class="ed">` blocks |
| Skills chips | `<div class="chips">` – add/remove `<span>` items |
| Work process steps | `<div class="step">` blocks |
| Quote and signature | `<div class="quote">` |
| Email, phone, website, location | `CONTACT` block |
| Social links | `<div class="soc">` |
| Colors | `css/style.css` → `:root{ --o: … }` (`--o` is the orange accent, `--bg` the background) |
| Fonts | `<link>` in `<head>` + `font:` lines in `css/style.css` |

### Still placeholders – replace these
- Project cards: "Project Name", "PROJECT ONE/TWO/THREE" and `href="#"`
- Education: "Your Degree / Diploma", "University / Institute", "20XX"
- Contact: `www.yourdomain.com`
- "VIEW ALL PROJECTS →" link (`href="#"`)

### Add another project card
Copy one `<a class="card" …> … </a>` block and paste it right after the last one.
(The grid is 3 columns, so a 4th card wraps to a new row.)
For a project image instead of the gradient box, change
`<div class="th t1">PROJECT<br>ONE</div>` to
`<div class="th"><img src="images/project1.png" alt="Project 1" style="width:100%;height:100%;object-fit:cover"></div>`.

## Preview locally
Just double-click `index.html`. (Google Fonts need an internet connection.)
