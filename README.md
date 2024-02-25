# ChapaPayment Gem

The `chapa_payment` gem allows for easy integration of the Chapa payment gateway into Ruby on Rails applications, enabling seamless handling of both local and international payments.

## About This Gem

The `chapa_payment` gem is developed by the Ethiopian Ruby and Rails Developers community, a group of passionate developers committed to enhancing the tech ecosystem in Ethiopia. This initiative was started at [Samael Labs](https://t.me/SamaelLabs), a collaborative space for innovators and developers to create solutions that drive progress and development within and beyond the Ethiopian community.

This gem represents a significant step forward in our mission to provide local developers with the tools they need to build world-class applications. By simplifying the integration of Chapa's payment gateway, we aim to empower businesses and developers, enabling them to offer seamless payment experiences to their customers.

We are always looking for contributors and feedback to improve and advance this project. Join us at Samael Labs to be a part of this transformative journey.

## Community and Contributions

We welcome contributions from everyone, especially from the members of the Ethiopian Ruby and Rails community. Whether you're fixing bugs, adding new features, improving documentation, or offering feedback, your help is appreciated.

To contribute, please visit our GitHub repository, create an issue or pull request, and join our community on Telegram at [Samael Labs](https://t.me/SamaelLabs). Let's build something great together!

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'chapa_payment'
```

Then execute:

```bash
bundle install
```

Or install it yourself as:

```bash
gem install chapa_payment
```

## Configuration

Set up the gem with your Chapa API credentials:

```ruby
ChapaPayment.configure do |config|
  config.api_key = 'your_chapa_api_key'
  config.merchant_id = 'your_merchant_id'
end
```

## Usage

Create a new payment transaction:

```ruby
payment = ChapaPayment::Transaction.new(amount: 10.00, currency: 'ETB', customer_email: 'customer@example.com', callback_url: 'http://example.com/callback')
response = payment.charge
```

Check payment status:

```ruby
status = ChapaPayment::Transaction.check_status(response.transaction_id)
```

## Features

- Local and international payment support
- Secure payment processing
- Simple Ruby on Rails integration

## Contributing

Contributions are welcome. Feel free to open pull requests or issues.

## License

This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.

Attribution: Published by Samael (AI Powered), 2024.

You are free to share and adapt the material for any purpose, even commercially, under the following terms:

- Attribution â Give appropriate credit, link to the license, and indicate changes. You must distribute contributions under the same license as the original.
- ShareAlike â Remix, transform, or build upon the material, sharing under the same license.

No additional restrictions â You cannot apply legal terms or technology that restrict others beyond what the license allows.

Notices:
The license may not cover all possible uses. No warranties are given.
