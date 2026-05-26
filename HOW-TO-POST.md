# How to publish a blog post

This guide is for anyone posting to the Together Against TB blog. No coding experience needed — everything can be done in your web browser on GitHub.

Posts are reviewed before they go live. When you've finished your changes, you'll submit them for approval and Sophie will publish them.

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
11. Scroll down to **Commit changes** and click it to open the dialog
12. Write a short description like `Add post: World TB Day 2026`
13. Select **"Create a new branch for this commit"** — GitHub will suggest a branch name, which is fine to keep
14. Click **Propose changes**

> You'll land on an "Open a pull request" page — **don't click anything yet**. Continue to Step 3 first.

---

## Step 3 — Add the post to the blog listing page

You need to make one more edit before submitting for review. Stay on your new branch.

1. Click **← Code** (top-left) to go back to the repository
2. You should see a yellow banner saying your branch had recent pushes — **ignore it for now**
3. Switch to your branch: click the branch dropdown (it says `main` by default) and select your new branch name
4. Open **`blog.html`** from the file list
5. Click the **pencil icon** to edit it
6. Find this comment block (use `Ctrl+F` / `Cmd+F` to search for `HOW TO ADD`):

```
<!-- ============================================================
     HOW TO ADD A NEW POST:
     ...
```

7. Follow the instructions inside that comment:
   - **First time only:** delete the `<div class="empty-state">` block (the "posts coming soon" message) — search for `empty-state` to find it
   - **First time only:** uncomment the `<div class="blog-grid">` by deleting the `<!--` line above it and the `-->` line at the very end
   - Copy one `<article class="blog-card">` block and fill in the four `[REPLACE: ...]` items:
     - **Category** — same as your post
     - **Date** — same as your post
     - **filename** — the name you gave the file in Step 2 (without `.html`)
     - **Post Title** — same as your post
     - **Excerpt** — the 1-2 sentence summary
   - Put the newest post at the **top** of the grid

8. Scroll down to **Commit changes** and click it
9. Write a commit message like `Add post card: World TB Day 2026`
10. Make sure **"Commit directly to [your branch name]"** is selected
11. Click **Commit changes**

---

## Step 4 — Submit for review

Now that both files are updated, you can open the pull request.

1. Click the **Pull requests** tab at the top of the repository
2. Click **New pull request**
3. Set it up so that:
   - **base:** `main`
   - **compare:** your branch (the one you created in Step 2)
4. Click **Create pull request**
5. Give it a title (e.g. `New post: World TB Day 2026`) and optionally add a note for Sophie
6. Click **Create pull request**

Sophie will get a notification to review your post. Once she approves and merges it, the post will go live automatically.

---

## Step 5 — Check your work

Once Sophie has merged the pull request, visit the live site at **https://togetheragainsttb.org/blog.html** — it may take a minute or two to appear. Click through to your post to make sure everything looks right.

If anything needs fixing, open a new pull request with the correction (follow the same steps above).

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
