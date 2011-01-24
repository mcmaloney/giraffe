require 'rubygems'
require 'bundler'
begin
  Bundler.setup(:default, :development)
rescue Bundler::BundlerError => e
  $stderr.puts e.message
  $stderr.puts "Run `bundle install` to install missing gems"
  exit e.status_code
end
require 'rake'

require 'jeweler'
Jeweler::Tasks.new do |gem|
  gem.name = "giraffes"
  gem.homepage = "http://github.com/mcmaloney/giraffe"
  gem.license = "MIT"
  gem.summary = "Shows you a giraffe: ASCII or image."
  gem.description = "Shows you a giraffe right from your command line! Thanks to Bryan Woods and Kitty."
  gem.email = "maloney.mc@gmail.com"
  gem.authors = ["Michael Maloney"]
  gem.executables << "giraffe"
  gem.require_path = "bin"
  gem.add_runtime_dependency 'launchy'
  gem.add_development_dependency 'launchy'
end
Jeweler::RubygemsDotOrgTasks.new

require 'rake/rdoctask'
Rake::RDocTask.new do |rdoc|
  version = File.exist?('VERSION') ? File.read('VERSION') : ""

  rdoc.rdoc_dir = 'rdoc'
  rdoc.title = "giraffe #{version}"
  rdoc.rdoc_files.include('README*')
  rdoc.rdoc_files.include('lib/**/*.rb')
end
