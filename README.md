# Commanding

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/commanding`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'commanding'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install commanding

## Usage

Run this command:

```
commanding install new_command_name shell_relative_path
```
then a command line tool named **new_command_name** will be created, which link to
**shell_relative_path**. When you run new_command_name, actually the shell file at
**shell_relative_path** will run.

When you don't need the **new_command_name**, just run this command:

```
commanding uninstall new_command_name
```

then this command **new_command_name** will be removed.

if after **commanding** run, nothing to happen, just quit current terminal, and then
restart it.

### Example

if you develop a shell file to pull code from the right remote branch, here suppose the
shell path you developed is pull.sh. In the past you need to run this pull.sh at its parent
directory, you can't directly run this pull.sh at other project. But with is **commanding**
command line tool, everythins become easy. Just run this command at pull.sh parent directory:

```
commanding install pull pull.sh
```
Then you can run pull at any git project. After then pull code become this:

```
pull
```
When someday the pull command no needed, just run this command:

```
commanding uninstall pull
```
Then it clean.

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/commanding. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
