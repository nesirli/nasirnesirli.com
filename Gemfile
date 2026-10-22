source "https://rubygems.org"

# GitHub Pages' gems don't support Ruby 4 yet; use Ruby 3.3 (brew install ruby@3.3).
ruby ">= 3.1", "< 3.5"

# Same versions GitHub Pages uses, so a local build matches the live site.
gem "github-pages", "~> 232", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-include-cache"
end

gem "webrick" # needed for `jekyll serve` on Ruby 3+
# No longer bundled with newer Ruby versions (3.4+), but Jekyll 3 still needs them
gem "csv"
gem "base64"
gem "bigdecimal"
gem "tzinfo-data", platforms: [:windows, :jruby]
