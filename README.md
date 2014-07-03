# ControllerSpecificAssets

**Work in progress. Do not use!**

Controller Specific Assets does what it says on the tin: Only loads your controller assets (e.g. `products.css`, `products.js`) into views rendered by the controller with the matching name (i.e. `products_controller.rb` in this case).

An article on the topic (and why this gem is necessary) can be found here: [Controller Specific Assets With Rails 4](http://theflyingdeveloper.com/controller-specific-assets-with-rails-4/)

## Installation

Add this line to your application's Gemfile:

    gem 'controller_specific_assets'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install controller_specific_assets

## Usage

Once the gem is installed, remove the `require_tree .` directives from your application asset files.

In application.css:

    *= require_tree .

In application.js:

    //= require_tree .

This stops Rails from loading all your controller assets automatically.

Add the following line to any layout you want controller assets to appear in:

    <%= controller_assets %>

That's it! The gem will now auto-detect asset files with names matching controllers and add them to the asset pipeline for you.

## Contributing

1. Fork it ( https://github.com/[my-github-username]/controller_specific_assets/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
