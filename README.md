
## Initialize new project

If you create new project from scratch, there are some things you may need to do:

```ruby
### change spree version

## Gemfile
gem 'spree', github: 'spree/spree', branch: '3-0-stable'
gem 'spree_gateway', :git => 'https://github.com/spree/spree_gateway.git', :branch => '3-0-stable'
gem 'spree_auth_devise', :git => 'https://github.com/spree/spree_auth_devise.git', :branch => '3-0-stable'

### you may need to run setup for spree auth devise

bundle exec rake spree_auth:install:migrations
bundle exec rake db:migrate
bundle exec rails g spree:auth:install
bundle exec rake spree_auth:admin:create

### you may need to run setup for spree
rails g spree:install
bundle exec rake railties:install:migrations
bundle exec rake db:migrate
bundle exec rake db:seed
bundle exec rake spree_sample:load


### You may need to change content of
 .rvm/gems/ruby-2.1.3/bundler/gems/spree-665c1c7a537c/core/db/default/spree/countries.rb
 and
 .rvm/gems/ruby-2.1.3/bundler/gems/spree-665c1c7a537c/core/db/default/spree/states.rb

### with content of version 2-3-stable on this address
 https://github.com/spree/spree/tree/2-3-stable/core/db/default/spree

### in case you got error when load sample data
```
