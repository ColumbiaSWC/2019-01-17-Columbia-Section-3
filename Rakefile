require 'colorize'
require 'html-proofer'
require 'yaml'

desc 'run link + html tests'
task :test do
  config      = YAML.load(File.open('./_config.yml'))
  baseurl     = config.fetch('baseurl', nil)
  site_dir    = './_site'
  target_dir  = "#{site_dir}#{baseurl}"

  puts 'Testing links and html tags...'.green

  FileUtils.rm_rf site_dir
  `bundle exec jekyll build -d #{target_dir}`
  HTMLProofer.check_directory(site_dir, { assume_extension: true }).run
end
