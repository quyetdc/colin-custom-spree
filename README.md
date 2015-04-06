
Spree devise
--------
bundle exec rake spree_auth:install:migrations
bundle exec rake db:migrate
bundle exec rails g spree:auth:install
bundle exec rake spree_auth:admin:create

rails g spree:install
bundle exec rake railties:install:migrations
bundle exec rake db:migrate
bundle exec rake db:seed
bundle exec rake spree_sample:load

Note:
You may need to change content of
 .rvm/gems/ruby-2.1.3/bundler/gems/spree-665c1c7a537c/core/db/default/spree/countries.rb
 and
 .rvm/gems/ruby-2.1.3/bundler/gems/spree-665c1c7a537c/core/db/default/spree/states.rb

 with content of version 2-3-stable on this address
 https://github.com/spree/spree/tree/2-3-stable/core/db/default/spree