require 'nokogiri'
require 'rake'
require 'rubygems'

desc 'Check outbound url links'
task :default do
  sh 'check-links --no-warnings'
end

desc 'Build release and copy to release directory'
task release: :build do
  sh 'rm -rf release'
  sh 'cp -r build release'
end

desc 'Generate the book using paperback'
task :build do
  sh './bin/stubs/paperback build'
end

desc 'Build and open a PDF version'
task open: :build do
  sh 'open build/playbook.pdf'
end
