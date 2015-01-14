require 'bundler/setup'

require 'albacore'
require 'albacore/tasks/versionizer'
require 'albacore/ext/teamcity'

Albacore::Tasks::Versionizer.new :versioning

SOLUTION_FILE = 'src/icaloc2014.sln'

desc 'Perform fast build (warn: doesn\'t d/l deps)'
build :quick_build do |b|
  b.logging = 'detailed'
  b.sln     = SOLUTION_FILE
end

desc 'restore all nugets as per the packages.config files'
nugets_restore :restore do |p|
  p.out = 'src/packages'
  p.exe = 'tools/NuGet.exe'
end

desc 'Perform full build'
build :build => [:versioning, :restore] do |b|
  b.sln = SOLUTION_FILE
end

desc 'Run unit tests'
test_runner :test => [:restore, :build] do |t|
  t.files = FileList['src/**/bin/**/Debug/*.Test.dll']
  t.exe   = FileList['src/packages/NUnit.Runners.*/**/tools/nunit-console.exe'].first
  t.add_parameter "/xml=#{Dir.pwd}/build/TestResults.xml"
  t.copy_local
end

