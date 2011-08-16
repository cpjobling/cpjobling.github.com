---
layout: post
title: Introducing BDD to Proman
date: 2010-03-26
categories:
---

Behaviour Driven Development is well known in the Rails development community and I've decided to use it in my re-write of Proman. Following the instructions in Chapter 20 of the 13th beta of [http://www.pragprog.com/titles/achbd/the-rspec-book](The RSpec Book), I installed the necessary gems (version numbers are the values at time of installation):

	sudo gem install rspec --version 1.3.0
	sudo gem install rspec-rails --version 1.3.2
	sudo gem install cucumber --version 0.6.3
	sudo gem install cucumber-rails --version 0.3.0
	sudo gem install database_cleaner --version 0.5.0
	sudo gem install webrat --version 0.7.0
	sudo gem install selenium-client --version 1.2.18

I then installed _rspec_ and _cucumber_ in my new Proman 3 project:

	$ cd ~/dev/Proman-3
	$ mkdir lib
	$ mkdir tasks
	$ ./script/generate rspec
	Configuring rspec and rspec-rails gems in config/environments/test.rb ...

	      exists  lib/tasks
	      create  lib/tasks/rspec.rake
	      create  script/autospec
	      create  script/spec
	      create  spec
	      create  spec/rcov.opts
	      create  spec/spec.opts
	      create  spec/spec_helper.rb
	
	$ ./script/generate cucumber --rspec --webrat
	/usr/local/lib/ruby/gems/1.8/gems/rails-2.3.5/lib/rails/gem_dependency.rb:119:Warning: Gem::Dependency#version_requirements is deprecated and will be removed on or after August 2010.  Use #requirement
	       force  config/database.yml
	      create  config/cucumber.yml
	      create  config/environments/cucumber.rb
	      create  script/cucumber
	      create  features/step_definitions
	      create  features/step_definitions/web_steps.rb
	      create  features/support
	      create  features/support/paths.rb
	      create  features/support/env.rb
	      exists  lib/tasks
	      create  lib/tasks/cucumber.rake

I committed the changes and created a tag _rspeced_.