### Knasack
---
https://github.com/KnapsackPro/knapsack_pro-ruby

```ruby
group :test, :development do
  gem 'knaspack_pro'
end

KnapsackPro.load_tasks if defined?(KnapsackPro)

# spec/spec_helper.rb
require 'vcr'
VCR.configure do |config|
  config.hook_into :webmock
  config.ignore_hosts('localhost', '127.0.1', '0.0.0.0', 'api.knapsackpro.com')
end
require 'webmock/rspec'
WebMock.disable_net_connect!(allow: ['api.knapsakpro.com'])
require 'fakeweb'
FakeWeb.allow_net_connect = %r[^https?://api\.knapsackpro\.com]

```

```
bundle install

```

```
```
