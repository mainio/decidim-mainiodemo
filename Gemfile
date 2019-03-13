# frozen_string_literal: true

source "https://rubygems.org"

ruby RUBY_VERSION

gem "decidim", "0.16.0"
# gem "decidim-consultations", "0.16.0"
# gem "decidim-initiatives", "0.16.0"

gem "decidim-plans", "~> 0.16.0"

gem "bootsnap", "~> 1.3"

gem "puma", "~> 3.0"
gem "uglifier", "~> 4.1"

gem "faker", "~> 1.9"

group :development, :test do
  gem "byebug", "~> 10.0", platform: :mri

  gem "decidim-dev", "0.16.0"
end

group :development do
  gem "letter_opener_web", "~> 1.3"
  gem "listen", "~> 3.1"
  gem "spring", "~> 2.0"
  gem "spring-watcher-listen", "~> 2.0"
  gem "web-console", "~> 3.5"
end

group :production, :staging do
  gem 'dotenv-rails', '~> 2.1', '>= 2.1.1'

  # resque-scheduler still depends on resque ~> 1.25
  # Keep an eye on:
  # https://github.com/resque/resque-scheduler/pull/661
  gem 'resque', '~> 1.26'
  gem 'resque-scheduler', '~> 4.0'
end
