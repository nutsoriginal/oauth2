source 'https://rubygems.org'

git_source(:github) { |repo_name| "https://github.com/#{repo_name}" }

group :test do
  ruby_version = Gem::Version.new(RUBY_VERSION)
  if ruby_version >= Gem::Version.new('2.1')
    # TODO: Upgrade to >= 0.59 when we drop Rubies below 2.2
    #     Error: Unsupported Ruby version 2.1 found in `TargetRubyVersion` parameter (in .rubocop.yml). 2.1-compatible analysis was dropped after version 0.58.
    #     Supported versions: 2.2, 2.3, 2.4, 2.5
    gem 'rubocop', '~> 0.59.2'
    gem 'rubocop-rspec', '~> 1.30.0'
  end
  gem 'pry', '~> 0.11' if ruby_version >= Gem::Version.new('2.0')
  gem 'rspec-pending_for'
end

# Specify non-special dependencies in oauth2.gemspec
gemspec
