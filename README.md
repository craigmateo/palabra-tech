# Palabra Tech

This is the source for my personal website built with [Hugo](https://gohugo.io/) using the [Lightbi](https://github.com/binokochumolvarghese/lightbi-hugo) theme.  
The site shares writings and reflections on life, literature, ecology, and more.

## 🚀 Development

To run the site locally:

    hugo server -D

Then open [http://localhost:1313](http://localhost:1313) in your browser.

## 🛠️ Build

To generate the static site in the `public/` folder:

    hugo

> Note: The `public/` folder is ignored in version control. It will be generated fresh on each build.

## 📂 Project Structure

- `content/` → site content (posts, pages)  
- `layouts/` → custom templates and overrides of theme partials  
- `assets/` → images, SCSS, JS (processed by Hugo)  
- `static/` → static files copied directly to `/`  
- `themes/` → theme files (Lightbi, as a submodule)  
- `config.toml` → site configuration

> ⚠️ Do **not edit files directly inside `themes/lightbi-hugo/`**. Any customizations should go in `layouts/partials/` or `layouts/_default/` in the main site folder so updates to the theme won’t overwrite them.

## 📦 Theme Submodule

This site uses the **Lightbi theme** as a Git submodule. To set it up after cloning the repo:

    git submodule update --init --recursive

Or, if adding manually:

    git submodule add https://github.com/binokochumolvarghese/lightbi-hugo themes/lightbi-hugo
    git submodule update --init --recursive

This keeps the theme separate from your site content and allows easy updates.

## 📜 Git Ignore

The repo ignores:

    public/

Optionally, if you have local theme edits you don’t want to commit:

    themes/lightbi-hugo/


## 🎨 Customization Guide

To safely customize the site without touching the theme:

1. **Homepage text & title**  
   - Set in `config.toml` under `[params]`:

    ```toml
    [params]
    homeTitle = "Palabra Technical"
    subtitle = "At the interface of computation, visualization, and technical storytelling"
    bigimg = "img/about/about-gallery/1.jpg"
    ```

2. **Logo**  
   - Place your logo in `static/img/profile/logo.jpeg`  
   - Override the navbar in `layouts/partials/nav.html`:

    ```html
    <a class="navbar-brand fw-bold d-flex align-items-center" href="{{ "" | absLangURL }}">
      <img src="/img/profile/logo.jpeg" alt="Logo" style="height:32px; margin-right:8px;">
      {{ .Site.Title }}
    </a>
    ```

3. **Header / homepage overrides**  
   - Copy `themes/lightbi-hugo/layouts/partials/page_header.html` to `layouts/partials/page_header.html`  
   - Make your edits there — Hugo will use this instead of the theme file.

> This ensures all customizations survive theme updates.

## 📜 License

MIT
