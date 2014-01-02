watir-webdriver
===============

Watir implementation built on WebDriver's Ruby bindings.
See http://rubyforge.org/pipermail/wtr-development/2009-October/001313.html.

[![Gem Version](https://badge.fury.io/rb/watir-webdriver.png)](http://badge.fury.io/rb/watir-webdriver)
[![Build Status](https://secure.travis-ci.org/watir/watir-webdriver.png)](http://travis-ci.org/watir/watir-webdriver)
[![Code Climate](https://codeclimate.com/github/watir/watir-webdriver.png)](https://codeclimate.com/github/watir/watir-webdriver)
[![Dependency Status](https://gemnasium.com/watir/watir-webdriver.png)](https://gemnasium.com/watir/watir-webdriver)
[![Coverage Status](https://coveralls.io/repos/watir/watir-webdriver/badge.png?branch=master)](https://coveralls.io/r/watir/watir-webdriver)

Example
-------
```ruby

require 'watir-webdriver'

browser = Watir::Browser.new :firefox
browser.goto "http://google.com"
browser.text_field(:name => 'q').set("WebDriver rocks!")
browser.button(:name => 'btnG').click
puts browser.url
browser.close
```

Description
-----------

The file in lib/watir/elements/generated.rb is autogenerated from the HTML5 spec. This is done by extracting the IDL parts from the spec and processing them with the WebIDL gem (link below).

Specs
-----

watir-webdriver uses [watirspec](http://github.com/watir/watirspec) for testing. After cloning, you should fetch the submodule:

    git submodule init && git submodule update

Specs specific to watir-webdriver are found in spec/*_spec.rb, with watirspec in spec/watirspec.

API docs
--------

* http://rdoc.info/gems/watir-webdriver/ (basic docs, updated on every release)
* http://watir.github.com/watir-webdriver/doc/ (includes all attribute methods, updated occasionally)

See also
--------

* http://watirwebdriver.com
* http://github.com/jarib/webidl
* http://github.com/watir/watirspec
* http://selenium.googlecode.com

Dependencies
------------

* selenium-webdriver

Note on Patches/Pull Requests
-----------------------------

* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a
  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
  (if you want to have your own version, that is fine but bump version in a commit by itself I can ignore when I pull)
* Send me a pull request. Bonus points for topic branches.

Copyright
---------

Copyright (c) 2009-2014 Jari Bakken. See LICENSE for details.
