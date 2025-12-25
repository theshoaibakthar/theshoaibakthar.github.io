source "https://rubygems.org"

# 1. Standard Jekyll pin
gem "jekyll", "~> 3.9.0"

# 2. THE FIX: Manually force ActiveSupport to version 7.x.
# This prevents it from installing version 8.x, which causes the crash.
# gem "activesupport", "~> 7.1"

# 3. GitHub Pages sync
gem "github-pages", group: :jekyll_plugins

# 4. Required for Ruby 3.0+
gem "webrick"

# Windows performance
# gem "wdm", "~> 0.1.0" if Gem.win_platform?

# Plugins
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
  gem "hawkins"
end

gem "tzinfo-data", platforms: [:mingw, :mswin, :x64_mingw, :jruby]