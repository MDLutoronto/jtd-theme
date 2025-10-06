# Map and Data Library JTD Theme
This is a customized version of the [Just the Docs](https://just-the-docs.com) theme for the [Map and Data Library](https://mdl.library.utoronto.ca) at the [University of Toronto Libraries](https://www.library.utoronto.ca).


# Using the template
This repository is a [GitHub template repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-repository-from-a-template) that you can use to create your own documentation site using the [Just the Docs](https://just-the-docs.com) theme.

To create a new site using this template, click the green "Use this template" button above. This will create a new repository in your GitHub account with the contents of this repository.

# Using as a remote theme
You can use this repository as a remote theme, powered by the [jekyll-remote-theme plugin](https://github.com/benbalter/jekyll-remote-theme). 

To do so, add the following two lines to your site's `_config.yml` file:
```yaml
remote_theme: "MDLutoronto/jtd-theme"

plugins:
    - ... (if you have other plugins)
    - jekyll-remote-theme
```
Also, you need to install the `jekyll-remote-theme` (version 0.4.3) gem by adding this line to your `Gemfile`:
```ruby
gem "jekyll-remote-theme", "~> 0.4.3"
```