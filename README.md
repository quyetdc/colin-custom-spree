
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

## Testing

#### Login with
```ruby
account: spree@example.com
password: password
```

#### Test admin
```ruby
url: localhost:3000/admin
account: spree@example.com
password: password
```

## TODO

#### 1. There are a lot of things I wanna improve. These include some gems like:

gem 'spree_fancy'

gem 'spree_social'

gem 'rubocop', '0.24.1'

gem 'friendly_id'

And some ones from awesome ruby gems list


#### 2. I also wanna custom views, model, controllers ...



