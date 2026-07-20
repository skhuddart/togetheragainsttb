# How to publish a blog post

This guide is for anyone posting to the Together Against TB blog. No coding experience needed — everything can be done in your web browser on GitHub.

Posts are reviewed before they go live. When you've finished your changes, you'll submit them for approval and Sophie will publish them.

---

## The most important thing to know

The template has blanks written in **CAPITAL LETTERS** that end in the word **`HERE`**, like `YOUR TITLE HERE` or `WRITE YOUR OPENING PARAGRAPH HERE`.

Type your own words right over each blank, so that **nothing in capital letters is left behind.** For example, `YOUR TITLE HERE` becomes `World TB Day`.

Before you submit, search your file for the word **`HERE`** — if you find any left over, you missed a blank.

---

## Before you start

You'll need a **GitHub account** with access to this repository. Ask Sophie to add you if you haven't been added yet.

Write your post somewhere first (a Google Doc or notes app) so it's ready to paste in. Have these ready:

- **Title**
- **Date** — in `Month D, YYYY` format, e.g. `May 26, 2026`
- **Category** — pick one: `Organization Updates`, `TB Education`, `Community Stories`, or `Advocacy`
- **Short excerpt** — 1–2 sentences for the blog listing page
- **Body text** — as many paragraphs as you need

---

## Step 1 — Create the post file

1. Go to the repository on GitHub: **https://github.com/skhuddart/togetheragainsttb**
2. Click into the **`posts`** folder
3. Click on **`post-template.html`** to open it
4. Click the **copy icon** (top-right of the file, looks like two overlapping squares) to copy the whole file
5. Go back to the **`posts`** folder
6. Click **Add file → Create new file**
7. Name your file using lowercase letters and hyphens, ending in `.html`:
   - Good: `world-tb-day-2026.html`
   - Good: `patient-story-maria.html`
   - No spaces, capital letters, or special characters
8. Paste the template content into the editor

Now fill in your content. Replace each `... HERE` blank with your own words — the whole blank, so nothing in capital letters is left (see the box at the top of this guide):

| Blank | Replace with |
|---|---|
| `YOUR TITLE HERE` (appears **twice** — search for it) | Your post title |
| `WRITE A 1-2 SENTENCE SUMMARY HERE` | A brief description for search engines |
| `CHOOSE ONE CATEGORY HERE` | One of the four categories above |
| `DATE HERE` | The publish date, e.g. `May 26, 2026` |
| `WRITE YOUR OPENING PARAGRAPH HERE` and the other `... HERE` body blanks | Your actual paragraphs — type over the blank |

9. Delete any sections you don't need (for example, the bullet list or the optional heading). The green comment lines (starting with `<!--`) are just tips for you — you can leave them or delete them; they never show up on the website.
10. **Check for leftover blanks:** press `Ctrl+F` / `Cmd+F` and search for the word `HERE`. Every one should be gone.
11. Scroll down to **Commit changes** and click it to open the dialog
12. Write a short description like `Add post: World TB Day 2026`
13. Select **"Create a new branch for this commit"** — keep the branch name GitHub suggests
14. Click **Propose changes**

> You'll land on an "Open a pull request" page — **don't click anything yet.** Continue to Step 2 first.

---

## Step 2 — Add your post to the blog listing page

Your post file exists now, but it won't show up on the blog page until you add a card that links to it. Stay on the branch you just created.

1. Click **← Code** (top-left) to go back to the repository
2. If you see a yellow banner about recent pushes, **ignore it for now**
3. Switch to your branch: click the branch dropdown (it says `main` by default) and select the branch name you just created
4. Open **`blog.html`** from the file list
5. Click the **pencil icon** to edit it
6. Search (`Ctrl+F` / `Cmd+F`) for `blog-grid` to find where the post cards live. Each existing post is one `<article class="blog-card">…</article>` block.
7. **Copy the blank card below** and paste it directly **below** the `<div class="blog-grid">` line, so it becomes the **first** card (the newest post always sits at the top):

```html
<article class="blog-card">
  <div class="blog-card-body">
    <div class="blog-card-meta">
      <span class="blog-tag">CHOOSE ONE CATEGORY HERE</span>
      <span class="blog-date">DATE HERE</span>
    </div>
    <h3><a href="posts/YOUR-FILE-NAME-HERE.html">YOUR TITLE HERE</a></h3>
    <p>WRITE A 1-2 SENTENCE SUMMARY HERE</p>
    <a href="posts/YOUR-FILE-NAME-HERE.html" class="read-more">Read more &rarr;</a>
  </div>
</article>
```

8. Fill in the blanks, just like you did in the post file. Note that two of them repeat:
   - `CHOOSE ONE CATEGORY HERE` — the same category you used on the post
   - `DATE HERE` — the same date you used on the post
   - `YOUR-FILE-NAME-HERE.html` — the exact filename from Step 1 (e.g. `world-tb-day-2026.html`). This appears **twice** — change both.
   - `YOUR TITLE HERE` — the same title you used on the post
   - `WRITE A 1-2 SENTENCE SUMMARY HERE` — your 1–2 sentence excerpt
9. **Check for leftover blanks:** search the file for the word `HERE`. Every one should be gone.
10. Scroll down to **Commit changes** and click it
11. Write a commit message like `Add post card: World TB Day 2026`
12. Make sure **"Commit directly to [your branch name]"** is selected
13. Click **Commit changes**

---

## Optional — Add a picture to your post

Skip this section if your post is text only. Adding a picture takes two parts: **upload the image file**, then **place it in your post**. Stay on the same branch throughout.

### Part A — Upload the image file

1. Get your image ready on your computer. Use a `.jpg` or `.png` file, and rename it to lowercase letters and hyphens with no spaces — e.g. `world-tb-day-group-photo.jpg`.
   - Tip: very large photos load slowly. If your file is bigger than about 1–2 MB, resize it smaller before uploading.
2. Click **← Code** to go back to the repository, and make sure your branch is still selected in the branch dropdown
3. Click into the **`images`** folder
4. Click **Add file → Upload files**
5. Drag your image in (or click **choose your files** and pick it)
6. Scroll down to **Commit changes**, make sure **"Commit directly to [your branch name]"** is selected, and click **Commit changes**

### Part B — Place the picture in your post

1. Open your post file inside the **`posts`** folder and click the **pencil icon** to edit it
2. Decide where the picture should appear, then paste this line on its own, between two paragraphs:

```html
<img src="../images/YOUR-IMAGE-FILE-NAME-HERE.jpg" alt="DESCRIBE THE PICTURE HERE" style="max-width: 100%; height: auto; border-radius: 10px; margin: 20px 0;">
```

3. Fill in the two blanks:
   - `YOUR-IMAGE-FILE-NAME-HERE.jpg` — the exact filename you uploaded, including `.jpg` or `.png`. Keep the `../images/` in front of it.
   - `DESCRIBE THE PICTURE HERE` — a short description of what's in the photo (this shows if the image can't load, and is read aloud by screen readers)
4. **Check for leftover blanks:** search for the word `HERE`. Every one should be gone.
5. Scroll down to **Commit changes**, keep **"Commit directly to [your branch name]"** selected, and click **Commit changes**

> **Common mix-ups:** the filename in the `<img>` line must match the uploaded file *exactly* (including capitalization and `.jpg` vs `.png`), and the path must start with `../images/`. If the picture doesn't appear when you check the live site, this is almost always why.

---

## Step 3 — Submit for review

Both files are updated now, so you can open the pull request.

1. Click the **Pull requests** tab at the top of the repository
2. Click **New pull request**
3. Set it up so that:
   - **base:** `main`
   - **compare:** your branch (the one you created in Step 1)
4. Click **Create pull request**
5. Give it a title (e.g. `New post: World TB Day 2026`) and optionally add a note for Sophie
6. Click **Create pull request** again to submit

Sophie will get a notification to review your post. Once she approves and merges it, the post will go live automatically.

---

## Step 4 — Check your work

Once Sophie has merged the pull request, visit the live site at **https://togetheragainsttb.org/blog.html** — it may take a minute or two to appear. Click through to your post and confirm:

- The title, date, and category are correct
- **No leftover CAPITAL-LETTER blanks (the word `HERE`) are showing anywhere** on the page
- Your paragraphs read the way you wrote them

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
