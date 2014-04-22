GitVers - Ruby Gem Auto Versioning
==================================

Usage
-----

I got tired of messing with ruby gem versioning, so
in my normal fashion I automated it. Now when I want
to make a ruby gem I do the following.

 * Create the remote on github (eg: https://github.com/floomby/gemness)

```
git clone https://github.com/floomby/gemness.git
cd gemness
gitvers install
```
 * Then edit the Rakefile to suit you needs
 * Code your gem

```
git add <files>
git commit -m "Release 1.0.0"
rake package && gem install pkg/gemness-1.0.0.gem
```

TODO
----

 * Using the github api to grab the description and
   website for the gem would be neat
 * Add install target to Rakefile

