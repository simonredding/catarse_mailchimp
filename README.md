# CatarseMailchimp

Catarse mailchimp integration with [Catarse](http://github.com/danielweinmann/catarse) crowdfunding platform

## Instalation

Add this lines to your Catarse application's Gemfile:

    gem 'catarse_mailchimp'

And then execute:

    $ bundle

## Usage

Add on user model app/models/user.br

    class User < ActiveRecord::Base
      ...

      sync_with_mailchimp

      ...
    end

### Configurations

Create this configurations into Catarse database:

    mailchimp_api_key, mailchimp_list_id

In Rails console, run this:

    Configuration.create!(name: "mailchimp_api_key", value: "API_KEY")
    Configuration.create!(name: "mailchimp_list_id", value: "LIST_ID")

Create a mailchimp configuration file on config/initilazers/mailchimp.rb and add:

    MAILCHIMP_API_KEY = Configuration[:mailchimp_api_key]
    MAILCHIMP_LIST_ID = Configuration[:mailchimp_list_id]

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request


This project rocks and uses MIT-LICENSE.
