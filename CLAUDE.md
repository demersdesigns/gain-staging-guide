# Gain Staging Guide — Claude Code Project

## What this project is

A static HTML guide (`index.html`) about gain staging for audio production. There is no build step — the file served as-is by Vercel.

- **Production URL:** https://gain-staging-guide.vercel.app
- **GitHub repo:** https://github.com/demersdesigns/gain-staging-guide
- **Vercel project:** gain-staging-guide (demersdesigns-1309s-projects team)

---

## How to make and preview changes

All content edits happen in `index.html`. Follow this branch-based flow to get a preview URL before anything goes live.

### 1. Create a feature branch

Always work on a branch — never commit directly to `main`.

```bash
git checkout -b feat/<short-description>
# e.g. git checkout -b feat/update-intro-section
```

### 2. Make your edits

Edit `index.html`. There is no dev server required — open the file in a browser locally if you want a quick sanity-check, or just rely on the Vercel preview.

### 3. Commit and push

```bash
git add index.html
git commit -m "Short description of the change"
git push -u origin HEAD
```

### 4. Get the preview URL

After pushing, Vercel automatically builds a preview deployment for any branch connected to GitHub. You have two ways to get the URL:

**Option A — Vercel CLI:**
```bash
vercel ls
```
The most recent non-Production deployment is your branch preview.

**Option B — GitHub PR:**
Open a pull request on GitHub. Vercel posts the preview URL as a PR comment within ~30 seconds.

### 5. Review, then merge

Once the preview looks right, merge the PR into `main` on GitHub. Vercel immediately redeploys the production site.

---

## Branch naming conventions

| Prefix | When to use |
|--------|-------------|
| `feat/` | New content or sections |
| `fix/` | Corrections to existing content |
| `style/` | Visual/layout changes only |

---

## Project structure

```
index.html      ← the entire site
.gitignore
CLAUDE.md       ← you are here
```

No package.json, no build step, no dependencies. Keep it simple.
