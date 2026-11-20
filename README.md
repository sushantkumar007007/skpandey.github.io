# Personal academic website: Sushant Kumar Pandey

This website is hosted for free on **GitHub Pages**. It stays online around the clock, uses HTTPS and needs no server.

---

## 1. Put the website online (one time, about 10 minutes)

1. Sign in to <https://github.com>.
2. Click **+** (top right) → **New repository**.
3. In **Repository name**, type exactly `YOUR-USERNAME.github.io`, using your own GitHub username (e.g., `skpandey.github.io`).
4. Select **Public**, then click **Create repository**.
5. On the new page, click **uploading an existing file**.
6. Unzip the website package on your computer. Open the folder and **drag everything inside it** (the folders `_data`, `_includes`, `_layouts`, `assets` and all the files) into the upload area.
   > Drag the *contents* of the folder, not the folder itself, so that `_config.yml` sits at the top level of the repository.
7. Click **Commit changes**.
8. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to *Deploy from a branch*, **Branch** to `main` and the folder to `/ (root)`, then click **Save**.
9. Wait 1–2 minutes and open `https://YOUR-USERNAME.github.io`. Your site is live.

The **Actions** tab shows each build. A green tick means the site was updated; a red cross means a typo in one of the files (see section 4).

---

## 2. Everyday updates (all in the browser)

To edit any file, open it on GitHub, click the **pencil icon** (Edit), make the change, then click **Commit changes**. The site updates in about a minute.

| What you want to change | File to edit |
|---|---|
| Add a news item | `_data/news.yml` |
| Add a paper | `_data/publications.yml` |
| Bio, research interests, "prospective students" note | `index.md` |
| Research directions, collaborations, projects | `research.md` |
| Courses | `teaching.md` |
| Students and thesis topics | `supervision.md` |
| Appointments, education, service | `cv.md` |
| Name, title, email, office, profile links | `_config.yml` |
| Photo | replace `assets/img/profile.jpg` (keep the same name; portrait format) |
| Menu items | `_data/navigation.yml` |
| Accent colour | `assets/css/style.css` (the `--accent` line at the top) |

### Add a news item

Open `_data/news.yml` and paste this **at the top**, below the comment lines:

```yaml
- date: "Jan 2027"
  text: "Paper **My Title** accepted at **ICSE 2027**."
```

- `**text**` gives **bold**, `*text*` gives *italic*, and `[text](https://link)` gives a link.
- The home page shows the newest 6 items. The News page shows all of them.

### Add a publication

Open `_data/publications.yml` and paste this **at the top of the list**:

```yaml
- title: "My New Paper Title"
  authors: "A. Author, S.K. Pandey, B. Author"
  year: 2027
  type: conference
  venue_short: "ICSE 2027"
  venue: "IEEE/ACM International Conference on Software Engineering"
  doi: "https://doi.org/10.1145/xxxxxxx"
  selected: true
```

- `type` is one of: `conference`, `journal`, `thesis`, `preprint`.
- Optional lines: `details` (volume/pages), `note` (e.g., "Industry Track"), `doi`, `pdf`, `arxiv`, `code`.
- `selected: true` also shows the paper on the home page. Remove the line to hide it there.
- `S.K. Pandey` is made bold automatically.

### Add your CV as a PDF

Upload the file as `assets/cv.pdf` (**Add file → Upload files** inside the `assets` folder). Then, in `_config.yml`, change `cv_pdf: ""` to `cv_pdf: "/assets/cv.pdf"`. A download button appears on the CV page.

---

## 3. Rules for `.yml` files (avoid broken builds)

- Keep the **indentation** exactly as in the examples: two spaces, never tabs.
- Every entry starts with `- ` (dash and space).
- Put text in **double quotes**. If your text itself contains a double quote, use single quotes `'` inside it instead.

---

## 4. If something goes wrong

- **Site not updating:** open the **Actions** tab. Click the red ✗ to see which file and line has the problem; it is almost always indentation or a missing quote in a `.yml` file.
- **Undo a change:** open the file → **History** → pick the earlier version → copy its content back.

---

## 5. Optional: your own domain

If you own a domain (e.g., `sushantkpandey.com`), go to **Settings → Pages → Custom domain**, enter it, and follow GitHub's DNS instructions. The domain is the only part that costs money; hosting stays free.
