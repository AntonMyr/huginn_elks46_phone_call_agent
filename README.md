# 46elks Phone Call agent

## What is this?

This is an agent that allows you to make phone calls with the help of https://46elks.com.

## Installation

This gem is run as part of the [Huginn](https://github.com/huginn/huginn) project. If you haven't already, follow the [Getting Started](https://github.com/huginn/huginn#getting-started) instructions there.

Add this string to your Huginn's .env `ADDITIONAL_GEMS` configuration:

```ruby
huginn_elks46_phone_call_agent
# when only using this agent gem it should look like this:
ADDITIONAL_GEMS=huginn_elks46_phone_call_agent
```

And then execute:

    $ bundle

You can now make phone calls from your Huginn instance, have fun!

## Want more?

Check out these agents as well:

-   [Sending MMS from Huginn](https://github.com/AntonMyr/huginn_elks46_mms_agent)
-   [Sending SMS from Huginn](https://github.com/AntonMyr/huginn_elks46_sms_agent)

## Development

Running `rake` will clone and set up Huginn in `spec/huginn` to run the specs of the Gem in Huginn as if they would be build-in Agents. The desired Huginn repository and branch can be modified in the `Rakefile`:

```ruby
HuginnAgent.load_tasks(branch: '<your branch>', remote: 'https://github.com/<github user>/huginn.git')
```

Make sure to delete the `spec/huginn` directory and re-run `rake` after changing the `remote` to update the Huginn source code.

After the setup is done `rake spec` will only run the tests, without cloning the Huginn source again.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release` to create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

1. Fork it ( https://github.com/[my-github-username]/huginn_elks46_phone_call_agent/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
