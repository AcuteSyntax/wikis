source "https://rubygems.org"

gem "github-pages", "~> 207", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.13.0"
end

install_if -> { RUBY_PLATFORM =~ %r!mingw|mswin|java! } do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

gem "wdm", "~> 0.1.0", :install_if => Gem.win_platform?

gem "kramdown-parser-gfm"

