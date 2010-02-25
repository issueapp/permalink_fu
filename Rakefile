require 'rake'
require 'rake/testtask'

begin
  require 'spec/rake/spectask'
rescue LoadError
  puts 'To use rspec for testing you must install rspec gem:'
  puts '$ sudo gem install rspec'
  exit
end

begin
  require 'jeweler'
  Jeweler::Tasks.new do |gemspec|
    gemspec.name = "permalink_fu"
    gemspec.summary = "ActiveRecord plugin for automatically converting fields to permalinks."
    gemspec.homepage = "http://github.com/technoweenie/permalink_fu"
    gemspec.authors = ["rick olson"]
  end
rescue LoadError
  puts "Jeweler not available. Install it with: gem install jeweler"
end


Rake::TestTask.new do |t|
  t.test_files = FileList['test/*_test.rb']
  t.verbose = true
end

desc 'Default: run test examples'
task :default => 'test'