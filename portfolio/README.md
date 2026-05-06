# Engineering Portfolio

Personal engineering portfolio website built with plain HTML, CSS, and JavaScript.
No frameworks, no build tools — just open files and edit.

## 🚀 Deploy to GitHub Pages (5 minutes)

1. **Create a new repository** on GitHub named `your-username.github.io`
   (replace `your-username` with your actual GitHub username).

2. **Push this folder** to that repository:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git remote add origin https://github.com/your-username/your-username.github.io.git
   git push -u origin main
   ```

3. Go to **Settings → Pages** in your repository.
   Under "Source", select `main` branch and `/ (root)`.
   Click **Save**.

4. Your site will be live at `https://your-username.github.io` within a minute.

---

## 📁 Folder structure

```
portfolio/
├── index.html                   ← Main page (edit all sections here)
├── assets/
│   ├── css/style.css            ← All styles (edit CSS variables to retheme)
│   ├── js/main.js               ← Filtering, animations, nav
│   └── images/                  ← Shared images (logo, avatar, etc.)
├── projects/
│   ├── robotics/
│   │   ├── index.html           ← Project folder page
│   │   ├── report.pdf           ← Drop your docs here
│   │   └── photo.jpg            ← Drop your images/videos here
│   ├── aerospace/
│   │   └── index.html
│   ├── mechanical/
│   │   └── index.html
│   └── software-ai/
│       └── index.html
└── publications/
    ├── thesis.pdf               ← Drop your PDFs here
    └── paper-2023.pdf
```

---

## ✏️ How to edit each section

### Personal info (name, links)
Open `index.html` and search for `✏️ EDIT` comments.
- Your name appears in `<a class="logo">` in the nav and in the footer.
- Update GitHub / email / LinkedIn in the `#contact` section.

### About me
Find `<section id="about">` and update the `<p>` paragraphs and stat numbers.

### Adding a new project
1. Create a new folder inside `projects/`, e.g. `projects/my-new-project/`.
2. Copy `projects/robotics/index.html` into it and edit the title, description, tags.
3. In `index.html`, duplicate one `<article class="folder-card">` block inside `#projects-grid`.
4. Set `data-category` to one of: `robotics | aerospace | software | mechanical`
   (or add a new category and a matching filter button in `.filter-bar`).
5. Set the `href` on the folder link to `projects/my-new-project/index.html`.

### Adding documents to a project folder
1. Place the file (PDF, notebook, etc.) inside the project's folder.
2. Open that project's `index.html`.
3. Duplicate a `<a class="doc-card">` block.
4. Set `href="your-file.pdf"`, update the type, name, and description labels.

### Adding images or videos
1. Place the `.jpg`, `.png`, or `.mp4` file in the project folder.
2. Open the project's `index.html`.
3. Duplicate a `<div class="media-card">` block.
4. Change `<img src="../../assets/images/placeholder.svg">` to `<img src="your-photo.jpg">`.
5. For videos, replace the `<img>` tag with `<video controls src="your-video.mp4"></video>`.

### Publications
In `index.html`, find `<section id="publications">`.
Duplicate an `<article class="pub-item">` block and fill in year, type, title, venue, abstract.
Drop the PDF in `publications/` and update the `href` on the download link.

### Skills
Find `<section id="skills">` in `index.html`.
Edit the `<li>` items inside each `.skill-block`, or add new `.skill-block` divs.

### Contact form
The form uses [Formspree](https://formspree.io) for free static-site email delivery.
1. Sign up at formspree.io and create a form.
2. Replace `YOUR_FORM_ID` in the `<form action="">` attribute with your real form ID.

### Theming / colours
Open `assets/css/style.css` and edit the CSS variables at the top of `:root {}`.
Change `--ink`, `--bg`, `--card`, `--border`, etc. to retheme the entire site instantly.

---

## 📝 Tips

- Every editable spot in the HTML is marked with a `✏️ EDIT` or `✏️ HOW TO` comment.
- File names in `href` attributes are **case-sensitive** on GitHub Pages (Linux servers).
  Keep all filenames lowercase with hyphens: `my-report.pdf`, not `My Report.pdf`.
- Images should ideally be under 1 MB for fast loading. Use `.jpg` for photos, `.png` for diagrams.
- Test locally by opening `index.html` in your browser before pushing.
