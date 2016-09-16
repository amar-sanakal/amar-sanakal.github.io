require 'jekyll'
require 'html-proofer'
require 'fileutils'

source = File.dirname(__FILE__)
built_site = File.join(source, '_site')

task :default => [:build]

desc 'Check the generated HTML of your site'
task :test => [:build] do |t|
    HTMLProofer.check_directory(built_site).run
end

desc 'Build your Jekyll site'
task :build do |t|
    config = Jekyll.configuration({
        'source' => source,
        'destination' => built_site
    })
    site = Jekyll::Site.new(config)
    Jekyll::Commands::Build.build(site, config)
end

desc 'Clean up the generated site'
task :clean do |t|
    FileUtils.rm_rf(built_site, :verbose => true)
end
