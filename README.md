Rails 3, RSpec, Factory Girl, Haml, and jQuery
==============================================

Easily generate a Rails 3 beta 4 application with RSpec, Factory Girl, Haml, and
jQuery in one line:

    % rails new three -J -T -d postgresql \
    -m http://github.com/mylescarrick/rails3-app/raw/master/app.rb


### Rails 3 beta 3 or earlier?

    % rails new three -J -T -d postgresql \
    -m http://github.com/mylescarrick/rails3-app/raw/master/app.rb


## Need Cucumber?

Use this generator file instead:

    % rails new my_app -J -T -m \
    http://github.com/leshill/rails3-app/raw/master/cuke.rb

rvm
---

We love `rvm`, so the application has an `.rvmrc` generated to specify a gemset.

Generators
----------

This also gives you a ton of generators, including the Machinist and Haml ones
from http://github.com/indirect/rails3-generators

JavaScript Includes
-------------------

Since the Rails helper `javascript_include_tag :defaults` is looking for
Prototype, we use a snippet from Yehuda to change the default JavaScript
Includes to be jQuery.

git
---

We love `git`, so the application has a git repo initialized with all the initial changes staged.

Wrap Up
-------

After the application has been generated, there are a few clean up commands to run:

    % cd my_app
    % gem install bundler
    % bundle install
    % bundle lock
    % script/rails generate rspec:install
    % script/rails generate cucumber:install --rspec --capybara
    % ...then follow any remaining machinist instructions
      at http://wiki.github.com/notahat/machinist/installation
