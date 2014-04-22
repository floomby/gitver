require 'rubygems'
require 'rubygems/package_task'
require 'pathname'

spec = Gem::Specification.new do |gem|
    gem.name         = Pathname.new(`git rev-parse --show-toplevel`).basename
    gem.version      = "0.0.1"
    
    gem.author       = "Josh Hoover"
    gem.email        = "floomby@nmt.edu"
    gem.homepage     = "http://github.com/floomby/gitvers"
    gem.summary      = "Ruby gem integration with git"
    gem.description  = "Does versioning, releasing and testing of rubygems with git"
    
    gem.files        = `git ls-files`.split($\)
    
    gem.executables  = ["gitvers"]
end

Gem::PackageTask.new(spec) do |pkg|
    pkg.gem_spec = spec
end
