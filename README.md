# GitHub Pages Jekyll Site

To view this site locally (MacOS only):

1. Install Ruby (if not already installed). On macOS with Homebrew:
   ```bash
   brew install ruby
   ```
   **Crucial Step:** Homebrew installs Ruby as "keg-only", so you must add it to your `PATH` to use it instead of the system Ruby. Run these commands:
   ```bash
   echo 'export PATH="/opt/homebrew/opt/ruby/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```
   Verify with `ruby -v`. It should show 3.2.0 or higher.
   *Note: For Ruby 3.4.0 and higher (including 4.0), some libraries like `csv` and `base64` are no longer included by default. They have been added to the `Gemfile`.*
2. Install Bundler: `gem install bundler`
3. Install dependencies: `bundle install`
4. Run Jekyll: `bundle exec jekyll serve`
5. Open `http://localhost:4000` in your browser.

### Troubleshooting
- **GitHub Pages compatibility:** The site uses the `jekyll-relative-links` plugin. This allows you to use standard Markdown links like `[Link](./file.md)` in your content. Jekyll will automatically convert these to the correct relative URLs, taking into account the `baseurl` configured in `_config.yml`.
- **Base URL:** The `_config.yml` is configured with `baseurl: "/ateliers-DDD-2026"` to ensure assets and links work correctly on GitHub Pages. Avoid using absolute paths starting with `/` in your Markdown; instead, use paths relative to the current file.
- **Theme:** This site uses the `jekyll-theme-minimal` theme.
- **Sass Deprecation Warnings:** The site uses `@use` in `assets/css/style.scss` to avoid deprecation warnings associated with older `@import` syntax in newer Ruby/Sass environments.
- **Ruby version:** This project requires Ruby 3.2.0 or higher.

To deploy on GitHub:
Push these files to the `main` branch and enable GitHub Pages in your repository settings (Settings > Pages).
