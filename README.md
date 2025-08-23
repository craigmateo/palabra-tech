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
- `layouts/` → custom templates
- `assets/` → images, SCSS, JS
- `static/` → static files copied directly to `/`
- `themes/` → theme files (Lightbi)
- `config.toml` → site configuration

## 📦 Theme Submodule

This site uses the **Lightbi theme** as a Git submodule. To set it up after cloning the repo:

    git submodule update --init --recursive

Or, if adding manually:

    git submodule add https://github.com/binokochumolvarghese/lightbi-hugo themes/lightbi-hugo
    git submodule update --init --recursive

This keeps the theme separate from your site content and allows easy updates.

## 📜 License

MIT
