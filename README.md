
# Cake Wallet Fiat API

The guides and resources for the leading Cake Labs Pricing API.

## Updating

Simply edit the relevant line(s) in the `Gemfile`.

You will need to have Ruby installed locally, and then run `bundle install` in the folder.

## Adding a plugin

The Just the Docs theme automatically includes the `jekyll-seo-tag` plugin.

To add an extra plugin, you need to add it in the `Gemfile` *and* in `_config.yml`. For example, to add `jekyll-default-layout`:

- Add the following to your site's `Gemfile`:

  ```ruby
  gem "jekyll-default-layout"
  ```

- And add the following to your site's `_config.yml`:

  ```yaml
  plugins:
    - jekyll-default-layout
  ```

## Building and previewing your site locally

Assuming Jekyll and Bundler are installed on your computer:

1.  Change your working directory to the root directory of your site.

2.  Run `bundle install`.

3.  Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.

    The built site is stored in the directory `_site`.

## Licensing and Attribution

This repository is licensed under the MIT License. You are generally free to reuse or extend upon this code as you see fit; just include the original copy of the license.
