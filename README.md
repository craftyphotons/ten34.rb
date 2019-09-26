# ten34

A globally-distributed, eventually-consistent, 100% available key-value store.

> Route 53 isn't really a database, but then again, neither is Redis.

_[Corey Quinn](https://twitter.com/QuinnyPig/status/1173371936342044672)_

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'ten34'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ten34

## Usage

### Creating a database

```shell
ten34 create-db route53://my.db
```

### Deleting a database

```shell
ten34 delete-db route53://my.db
```

### Setting a key

```shell
ten34 put foo bar -d route53://my.db
```

### Setting a key with encryption

```shell
ten34 put foo bar -d route53://my.db -e --kms-key-id <AWS_KMS_KEY_ID>
```

### Getting a key

```shell
ten34 get foo -d route53://my.db
```

### Deleting a key

```shell
ten34 del foo -d route53://my.db
```

### Listing all keys

```shell
ten34 keys .+ -d route53://my.db
```

### Listing keys matching a pattern

```shell
ten34 keys 'foo*' -d route53://my.db
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/craftyphotons/ten34. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the ten34 project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/craftyphotons/ten34/blob/master/CODE_OF_CONDUCT.md).

## Additional Disclaimer

In addition to the terms of the MIT license, this project and its maintainers shall not be held responsible for costs and repercussions resulting from its use. This includes but is not limited to account closure by your cloud service provider for violating their terms of service and the disappointment of your peers for usage of this project for your actual database.