# RuboCop Rails

[![Build Status](https://travis-ci.org/toshimaru/rubocop-rails.svg?branch=master)](https://travis-ci.org/toshimaru/rubocop-rails)
[![Gem Version](https://badge.fury.io/rb/rubocop-rails.svg)](https://badge.fury.io/rb/rubocop-rails)

RuboCop configuration which has the same code style checking as official Ruby on Rails.

[Official RoR Rubocop Configuration](https://github.com/rails/rails/blob/master/.rubocop.yml)


## rubocop-rails is renamed to rubocop-rails_config

`rubocop-rails` is renamed to `rubocop-rails_config`. To migrate to new gem, install rubocop-rails_config instead of rubocop-rails. See detail [here](https://github.com/toshimaru/rubocop-rails/issues/31)

```ruby
gem "rubocop-rails_config"
```

Then, run update command.

```console
$ bundle exec rails generate rubocop_rails_config:update
```

## Installation

Add this line to your application's `Gemfile`:

```ruby
gem "rubocop-rails"
```

## Usage

Add this line to your application's `.rubocop.yml`, or just run `rails generate rubocop_rails:install`:

```yml
inherit_gem:
  rubocop-rails:
    - config/rails.yml
```

## Customization

If you'd like to customize the rubocop setting, you can override it.

For example, if you want to change `TargetRubyVersion`, you can do it like:

```yml
inherit_gem:
  rubocop-rails:
    - config/rails.yml

AllCops:
  TargetRubyVersion: 2.3
```

This overrides `config/rails.yml` setting with `TargetRubyVersion: 2.3`.

## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
