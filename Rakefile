require 'rubygems'
require 'rubygems/package_task'

spec = Gem::Specification.new do |gem|
    gem.name         = File.basename(`git rev-parse --show-toplevel`).chop
    gem.version      = `gitver version`
    
    gem.author       = `git config --get user.name`
    gem.email        = `git config --get user.email`
    gem.homepage     = "https://github.com/floomby/gitver.git"
    gem.summary      = "Ruby gem integration with git"
    gem.description  = "Does versioning, releasing and testing of rubygems with git"
    
    gem.files        = `git ls-files`.split($\).select { |f| !(f =~ /templates/) }
    
    gem.executables  = ["gitver"]
end

Gem::PackageTask.new(spec) do |pkg|
    pkg.gem_spec = spec
end
