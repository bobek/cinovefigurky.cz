require 'fileutils'
require 'yaml'
require 'json'

ENV["LC_ALL"] = "en_US.utf8"

task :default => [:deploy]

task :build do
    system "bundle exec middleman build"
end
  
task :deploy => [:build] do
    system "rsync -av --delete --progress -e 'ssh -p 456' 'build/' 'srv1.trusted.cz:/var/www/cinovefigurky.cz/'"
end
