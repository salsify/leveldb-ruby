require 'rubygems'
require 'rubygems/package_task'
require 'bundler'
require 'rake'
require 'rake/extensiontask'

spec = Gem::Specification.load('leveldb-ruby.gemspec')

# task :rdoc do |t|
#   sh "rm -rf doc; rdoc #{spec.rdoc_options.join(' ')} #{spec.extra_rdoc_files.join(' ')} lib/leveldb.rb"
# end
#
# require 'rake/testtask'
# Rake::TestTask.new(:test) do |test|
#   test.libs << 'ext' << 'test'
#   test.pattern = 'test/**/*_test.rb'
#   test.verbose = true
# end
#
# task :build do |t|
#   sh "cd ext/leveldb && ruby extconf.rb && make"
# end

# add your default gem packing task
Gem::PackageTask.new(spec) do |pkg|
end

gem 'rake-compiler'

# feed the ExtensionTask with your spec
Rake::ExtensionTask.new('leveldb', spec) do |ext|
  ext.lib_dir = "lib/leveldb"
  ext.source_pattern = "*.{cc}"
end

# vim: syntax=ruby
