# metteko.net  
### Automated blog using Jekyll, GitHub Pages, and Minima  

This repository contains a **Jekyll-powered blog** hosted on **GitHub Pages**, using the **Minima** theme. The setup is fully automated—whenever changes are pushed to GitHub, Jekyll builds the site and updates it online.

---

## 1. Blog Structure  
### `_posts/` Directory (Blog Posts)  
Jekyll treats `_posts/` as your **blog post storage**.  
- Each `.md` file in `_posts/` represents a separate blog post.
- The **filename format matters**:  
  ```
  YYYY-MM-DD-title.md
  ```
- Jekyll automatically converts these Markdown files into HTML using the Minama's Layout.

---

## 2. Workflow (How the Blog Updates)  
1. Write a new blog post inside `_posts/`.
2. Push changes to GitHub.
3. GitHub Pages automatically runs Jekyll:
   - Reads `_config.yml` for settings.
   - Processes `_posts/` and applies **Minima’s layouts**.
   - Generates a fully static website.
4. The updated site is deployed and served online.

---

## 3. Important Files  
### `_config.yml` (Jekyll Configuration)  
This file controls how Jekyll builds the blog.  
- Defines settings like:
  - `theme: minima`
  - `permalink: /blog/:title/` (Overrides Jekyll’s default behavior and applies this URL structure only to posts inside `_posts/`, ensuring they appear under `/blog/post-title/`. Pages do not inherit this setting and must manually define their permalinks in Front Matter --> example blog.html)
  - `header_pages:` (controls which pages appear in the navigation bar)

---

## 4. Notes on Minima Theme  
- Jekyll does not require a `_layouts/` folder because Minima provides layouts automatically.
- To override Minima, create your own `_layouts/` folder and customize files.

---

## 5. Future Improvements  
- Add a `_layouts/` override to customize Minima.

---

### `CNAME` (Custom Domain Setup)  
The `CNAME` file is used to assign a custom domain to the GitHub Pages site.  
- When GitHub Pages sees this file, it automatically configures the site to be accessible at that domain.

