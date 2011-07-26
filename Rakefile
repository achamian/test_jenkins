require "rubygems"
require 'bundler'
require 'bundler/gem_tasks'
Bundler::GemHelper.install_tasks

require 'rake'
require 'rspec'
require 'rspec/core/rake_task'

Bundler.setup

desc 'Default: run spec tests.'
task :default => 'rspec:unit'

desc 'Cruise task'
task :cruise => 'rspec:unit'

namespace :rspec do
  desc "Run all unit specs"
  RSpec::Core::RakeTask.new(:unit) do |task|
    task.pattern = 'spec/**/*_spec.rb'
  end
end
