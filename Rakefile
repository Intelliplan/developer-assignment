require 'bundler/setup'

require 'albacore'
require 'albacore/tasks/versionizer'
require 'albacore/ext/teamcity'

Albacore::Tasks::Versionizer.new :versioning

SOLUTION_FILE = 'src/icaloc2014.sln'
SRC_ROOT = 'src/icaloc2014/'

desc 'Perform fast build (warn: doesn\'t d/l deps)'
build :quick_build do |b|
  b.logging = 'detailed'
  b.sln     = SOLUTION_FILE
end

desc 'restore all nugets as per the packages.config files'
task :restore do 
  sh "nuget install #{SRC_ROOT}packages.config -OutputDirectory src/packages"
end

desc 'Perform full build'
build :build => [:versioning, :restore] do |b|
  b.sln = SOLUTION_FILE
end

desc 'Run unit tests'
test_runner :test => [:restore, :build] do |t|
  t.files = FileList['src/icaloc2014.test/**/bin/**/Debug/*.test.dll']
  t.exe   = FileList["#{SRC_ROOT}/packages/NUnit.Runners.*/**/tools/nunit-console.exe"].first
  t.copy_local
end

desc 'Run the application'
task :run => [:restore, :build] do
  sh 'mono src/icaloc2014/bin/Debug/icaloc2014.exe'
end

task :default => :test
