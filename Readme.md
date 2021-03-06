![logo](http://seekingsustenance.files.wordpress.com/2010/04/manioc-whole.jpg)

RSpec extension to run Gherkin steps

[![Gem Version](https://badge.fury.io/rb/maniok_bdd.png)](http://badge.fury.io/rb/maniok_bdd)
[![Dependency Status](https://gemnasium.com/21croissants/maniok_bdd.png)](https://gemnasium.com/21croissants/maniok_bdd)
[![Build Status](https://travis-ci.org/21croissants/maniok_bdd.png?branch=master)](https://travis-ci.org/21croissants/maniok_bdd)
[![Coverage Status](https://coveralls.io/repos/21croissants/maniok_bdd/badge.png?branch=master)](https://coveralls.io/r/21croissants/maniok_bdd)
[![Code Climate](https://codeclimate.com/github/21croissants/maniok_bdd.png)](https://codeclimate.com/github/21croissants/maniok_bdd)
[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/21croissants/maniok_bdd/trend.png)](https://bitdeli.com/free "Github Analytics Bitdeli Badge")

# Documentation

Please read the [announcement blog post](https://github.com/21croissants/maniok_bdd/blob/master/introducing.md).

Warning, this project is a Work In Progress. Before going further, I would like to find fellow rubists who practice "Specification By Example" and got hurt by cucumber step definitions lack of readability and maintenance.

Please keep in touch through [twitter](https://twitter.com/21croissants) or this [github issue]( https://github.com/21croissants/maniok_bdd/issues/1 ).

# Example

```ruby
require 'spec_helper'

# type :feature is for Capybara 
Feature "The Simplest Feature", type: :feature  do

  shared_steps "home" do
    Given "I am on the home page" do
      visit "/"
    end
  end

  Scenario "The Simplest Scenario" do
    include_steps "home"

    When "something happens" do

    end

    Then "it should assert correctly" do
      true.should be_true
    end
  end
end
``` 

# Author

[Jean-Michel Garnier](http://21croissants.com)<br/>

Heavily inspired by http://coulda.tiggerpalace.com/ & [Railsware rspec-example_steps](https://github.com/railsware/rspec-example_steps)

License: MIT<br/>
