require 'rake'

task :default => :gendoc

task :clean do
  `rm -rf doc`
  `rm -rf .yardoc`
end

task :gendoc => :clean do
  `yardoc -e ./lib/yard-cucumber.rb 'example/**/*' --debug`
end

task :gem do
  `gem build city.gemspec`
  `gem install --local yard-cucumber-2.0.2.gem`
end