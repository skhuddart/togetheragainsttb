# How to publish a blog post

This guide is for anyone posting to the Together Against TB blog. No coding experience needed — everything can be done in your web browser on GitHub.

---

## Before you start

You'll need a **GitHub account** with access to this repository. Ask Sophie to add you if you haven't been added yet.

---

## Step 1 — Write your post

Write your post in a Google Doc or notes app first. Have ready:

- **Title**
- **Date** (e.g. May 26, 2026)
- **Category** — pick one: `Organization Updates`, `TB Education`, `Community Stories`, or `Advocacy`
- **Short excerpt** (1–2 sentences for the blog listing page)
- **Body text** (as many paragraphs as you need)

---

## Step 2 — Create the post file

1. Go to the repository on GitHub: **https://github.com/skhuddart/togetheragainsttb**
2. Click into the **`posts`** folder
3. Click on **`post-template.html`** to open it
4. Click the **copy icon** (top-right of the file, looks like two overlapping squares) to copy the raw content — or click the pencil icon to edit, select all (`Ctrl+A` / `Cmd+A`), and copy
5. Go back to the **`posts`** folder
6. Click **Add file → Create new file**
7. Name your file using lowercase letters and hyphens, ending in `.html`
   - Good: `world-tb-day-2026.html`
   - Good: `patient-story-maria.html`
   - Avoid spaces or special characters
8. Paste the template content into the editor
9. Replace every `[PLACEHOLDER]` (they're in square brackets) with your real content:

| Placeholder | Replace with |
|---|---|
| `[POST TITLE]` (appears twice) | Your post title |
| `[SHORT DESCRIPTION OF POST — 1-2 sentences]` | A brief description for search engines |
| `[CATEGORY]` | One of the four categories above |
| `[DATE]` | The publish date, e.g. `May 26, 2026` |
| `[Opening paragraph…]` | Your actual paragraphs — delete the placeholder text and type yours |

10. Delete any sections you don't need (e.g. the bullet list, optional heading)
11. Scroll down to **Commit changes**, write a short message like `Add post: World TB Day 2026`, and click **Commit changes**

---

## Step 3 — Add the post to the blog listing page

1. Go back to the repository root and open **`blog.html`**
2. Click the **pencil icon** to edit it
3. Find this comment block (use `Ctrl+F` / `Cmd+F` to search for `HOW TO ADD`):

```
<!-- ============================================================
     HOW TO ADD A NEW POST:
     ...
```

4. Follow the instructions inside that comment:
   - **First time only:** delete the `<div class="empty-state">` block (the "posts coming soon" message) — search for `empty-state` to find it
   - **First time only:** uncomment the `<div class="blog-grid">` by deleting the `<!--` line above it and the `-->` line at the very end
   - Copy one `<article class="blog-card">` block and fill in the four `[REPLACE: ...]` items:
     - **Category** — same as your post
     - **Date** — same as your post
     - **filename** — the name you gave the file in Step 2 (without `.html`)
     - **Post Title** — same as your post
     - **Excerpt** — the 1-2 sentence summary
   - Put the newest post at the **top** of the grid

5. Scroll down, write a commit message like `Add post card: World TB Day 2026`, and click **Commit changes**

---

## Step 4 — Check your work

Visit the live site at **https://togetheragainsttb.org/blog.html** — it may take a minute or two for changes to appear. Click through to your post to make sure everything looks right.

If something looks off, go back to GitHub and edit the file to fix it.

---

## Quick reference — category tags

| Category | Use for |
|---|---|
| `Organization Updates` | News about TaT programs, milestones, announcements |
| `TB Education` | Facts about TB, treatment, stigma, resources |
| `Community Stories` | Stories from patients, volunteers, or partners |
| `Advocacy` | Policy, campaigns, coalition work |

---

## Need help?

Email Sophie at sophie.huddart@gmail.com.
