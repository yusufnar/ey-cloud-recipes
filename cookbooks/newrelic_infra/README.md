# New Relic Infrastructure

This cookbook can serve as a good starting point for setting up the New Relic Infrastructure agent in your environment.

## Installation

To install this, you will need to add the following to cookbooks/main/recipes/default.rb:

    include_recipe "newrelic_infra"

Make sure this and any customizations to the recipe are committed to your own fork of this
repository.

## Customizations

Some common customizations can be made in `attributes/default.rb`.

### License Key

Please make sure to specify the license key in attributes/default.rb:

```ruby
# Replace value with actual license key
default['newrelic_infra']['license_key'] = "INSERT_NEW_RELIC_INFRA_KEY"
```

This will be used to in generating /etc/newrelic-infra.yml.

### Package Version

The recipe downloads the New Relic Infrastructure .deb package version as specified in the attributes/default.rb. Please update the version number as necessary:

```ruby
default['newrelic_infra']['package_version'] = "1.0.785"
```
