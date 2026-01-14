source "https://rubygems.org"

# GitHub Pages gem includes Jekyll and required plugins
gem "github-pages", group: :jekyll_plugins

# Additional plugins not included in github-pages
group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-seo-tag"
  gem "jekyll-sitemap"
end

# Windows and JRuby does not include zoneinfo files
gem "tzinfo", ">= 1", "< 3", platforms: [:mingw, :x64_mingw, :mswin, :jruby]
gem "tzinfo-data", platforms: [:mingw, :x64_mingw, :mswin, :jruby]

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1", platforms: [:mingw, :x64_mingw, :mswin]

# Lock http_parser.rb to v0.6.x on JRuby
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]

# GitHub Pages compatibility - webrick for Ruby 3.0+
gem "webrick", "~> 1.8"
