Spree Zero Stock Products
======================
[![Build Status](http://img.shields.io/travis/swrobel/spree_zero_stock_products/master.svg?style=flat)](https://travis-ci.org/swrobel/spree_zero_stock_products) [![Dependency Status](http://img.shields.io/gemnasium/swrobel/spree_zero_stock_products.svg?style=flat)](https://gemnasium.com/swrobel/spree_zero_stock_products) [![Coverage Status](http://img.shields.io/coveralls/swrobel/spree_zero_stock_products/master.svg?style=flat)](https://coveralls.io/r/swrobel/spree_zero_stock_products) [![Code Climate](   http://img.shields.io/codeclimate/github/swrobel/spree_zero_stock_products.svg?style=flat)](https://codeclimate.com/github/swrobel/spree_zero_stock_products)

Restore the `show_zero_stock_products` preference & related functionality in Spree 2.0+

The preference defaults to true, which is the out-of-the-box behavior in Spree 2.0+

Set it to `false` to avoid showing products with zero stock on any product listing/taxon pages.

Installation
------------
**This documentation is for the master branch. You probably want [2-0-stable](https://github.com/swrobel/spree_zero_stock_products/tree/2-0-stable), [2-1-stable](https://github.com/swrobel/spree_zero_stock_products/tree/2-1-stable), or [2-2-stable](https://github.com/swrobel/spree_zero_stock_products/tree/2-2-stable), or [2-3-stable](https://github.com/swrobel/spree_zero_stock_products/tree/2-3-stable), or [2-4-stable](https://github.com/swrobel/spree_zero_stock_products/tree/2-4-stable) instead**

1. Add spree_zero_stock_products to your Gemfile:

  ```ruby
  gem 'spree_zero_stock_products', github: 'swrobel/spree_zero_stock_products'
  ```

1. Bundle your dependencies:

  ```shell
  bundle
  ```

1. Set the preference in an initializer such as `config/initializers/spree.rb`:

  ```ruby
  Spree.config do |config|
    config.show_zero_stock_products = false # Default is true
  end
  ```

1. Profit.

Versioning
----------
Versions files the pattern MAJOR.MINOR.PATCH [SemVer-style](http://semver.org/). MAJOR.MINOR version will always match the Spree version that gem is compatible with. PATCH version is incremented as new bugfix releases of this gem come out, indepently of new Spree PATCH versions.

For example, version 2.1.0 is compatible with the Spree 2.1.x series, while version 2.0.4 is compatible with the Spree 2.0.x series.

You should not need to worry about this, as the gemspec has the appropriate constraints. But hey, the more you know.

Testing
-------
This extension is tested against the following rubies:

* 1.9.3
* 2.0
* 2.1
* 2.2
* 2.3
* jruby (experimental)
* rubinius (experimental)

As well as the following databases:

* sqlite
* postgres
* mysql

### Running the tests locally

Be sure to bundle your dependencies and then create a dummy test app for the specs to run against.

```shell
bundle
bundle exec rake test_app
bundle exec rspec
```

License
-------

Copyright (c) 2013 Stefan Wrobel, released under the MIT License
