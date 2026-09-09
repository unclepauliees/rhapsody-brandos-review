# Deploying to GitHub Pages

The repo is already initialized with the first commit made. Three steps.

## 1 | Create the empty repo on GitHub

Go to https://github.com/new, name it (for example, `rhapsody-brand-os`), and **do not** add a README, .gitignore, or license. This repo already has files.

**Choose Private unless you have consciously decided otherwise.**
See "Visibility" below. This matters.

## 2 | Push

From this folder:

```bash
git remote add origin https://github.com/<your-username>/<repo-name>.git
git branch -M main
git push -u origin main
```

## 3 | Turn on Pages

Repo > **Settings** > **Pages** > Source: **Deploy from a branch**
> Branch: **main**, folder: **/ (root)** > Save.

Live in ~60 seconds at:
`https://<your-username>.github.io/<repo-name>/`

`.nojekyll` is already included so Jekyll won't touch the asset folders.

---

## Visibility: read before you publish

**GitHub Pages sites are publicly readable on Free, Pro, and Team plans.**
Making the repo private does *not* make the Pages site private on those plans.
Private Pages (visible only to authenticated org members) requires
**GitHub Enterprise Cloud**.

This document is stamped *Internal / Confidential* and contains the brand
firewall rationale, GC Veto Gate, data-plane segregation, capacity governance, and an **uncleared trademark**. If the repo is on a Free/Pro/Team plan, publishing Pages puts all of that on the open internet where it can be indexed.

**Options, in order of preference:**

1. **GitHub Enterprise Cloud** with private Pages. Reviewers sign in and nothing is public.
2. **Private repo, no Pages.** Reviewers are added as collaborators and open
   `index.html` locally, or you send them the PDF. Zero exposure.
3. **Public Pages with a redacted build.** Strip Section 11 Governance and the
   Symphony Space references, and remove the "Internal / Confidential" stamp.
   Ask and I'll generate that build.
4. Public Pages with the full document, only after GC sign-off.

A URL with no link to it is *not* private. Assume anything on public Pages
can be found.
