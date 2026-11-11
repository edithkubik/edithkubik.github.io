source "https://rubygems.org"

# Same Jekyll version and plugins that GitHub Pages builds with,
# so the local preview matches the live site.
gem "github-pages", group: :jekyll_plugins

# Ruby 3+ no longer bundles webrick, which `jekyll serve` needs.
gem "webrick"

# jekyll-remote-theme depends on "openssl" with no version cap, so Bundler
# picks the newest release (4.x), which has to be compiled from source and
# fails on Windows without OpenSSL headers. Ruby 3.3 already ships openssl
# 3.2.x prebuilt, so pin to that and skip the compile entirely.
gem "openssl", "~> 3.2"

# Windows-only helpers: timezone data and native file watching.
platforms :windows do
  gem "tzinfo-data"
  gem "wdm", ">= 0.1.0"
end
