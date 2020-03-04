# frozen_string_literal: true

source "https://rubygems.org"

ruby RUBY_VERSION

# Run updates by following the Decidim upgrade instructions:
# https://github.com/decidim/decidim/blob/master/docs/getting_started.md#keeping-your-app-up-to-date
DECIDIM_VERSION = "~> 0.20.0"
DECIDIM_MODULE_VERSION = "~> 0.20.0"

gem "decidim", DECIDIM_VERSION
gem "decidim-consultations", DECIDIM_VERSION
# gem "decidim-initiatives", DECIDIM_VERSION

# gem "decidim-plans", DECIDIM_MODULE_VERSION
gem "decidim-plans", git: "git@github.com:mainio/decidim-module-plans.git"

gem "bootsnap", "~> 1.3"

gem "puma", "~> 3.12"
gem "uglifier", "~> 4.1"

gem "faker", "~> 1.9"

group :development, :test do
  gem "byebug", "~> 11.0", platform: :mri

  gem "decidim-dev", DECIDIM_VERSION
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
