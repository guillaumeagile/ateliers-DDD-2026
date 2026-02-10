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
2. Install Bundler: `gem install bundler`
3. Install dependencies: `bundle install`
4. Run Jekyll: `bundle exec jekyll serve`
5. Open `http://localhost:4000` in your browser.

To deploy on GitHub:
Push these files to the `main` branch and enable GitHub Pages in your repository settings (Settings > Pages).
