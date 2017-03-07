source 'https://rubygems.org'

# calling Kernel.require as suggested here - https://github.com/bundler/bundler/issues/5346
Kernel.require 'json'
Kernel.require 'open-uri'

versions = JSON.parse(open('https://pages.github.com/versions.json').read)

gem 'github-pages', versions['github-pages'], group: [:jekyll_plugins]
gem 'execjs'
gem 'therubyracer'
gem 'jekyll-paginate'

gem 'jekyll'
gem 'html-proofer'
