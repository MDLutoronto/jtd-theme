# Map and Data Library JTD Theme
This is a customized version of the [Just the Docs](https://just-the-docs.com) theme for the [Map and Data Library](https://mdl.library.utoronto.ca) at the [University of Toronto Libraries](https://www.library.utoronto.ca).

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

Every time you push changes to your repository, GitHub Pages will automatically fetch the latest version of the theme from this repository.

# Development
## Testing the theme locally
To test the theme locally, you need to have [Ruby](https://www.ruby-lang.org/en/documentation/installation/) and [Bundler](https://bundler.io) installed.
1. Clone the repository:
```bash
git clone https://github.com/MDLutoronto/jtd-theme.git
```
2. Navigate to the repository directory:
```bash
cd jtd-theme
```
3. Install the dependencies and serve the site with live reload:
```bash
bundle install && bundle exec jekyll serve --livereload
```
4. Open your web browser and go to `http://localhost:4000` to view the site.

## Deployment bug fix
If the deployment keeps looping the following messages:
```bash
...
Current status: deployment_queued
Getting Pages deployment status...
...
```
### Unpublishing and republishing the site
A way to fix is is to go to the repository's **Settings** > **Pages**, unpublish the site by clicking the **Unpublish site** button, then republish it by clicking the **Save** button.

### Changing the source temporarily
Another way to fix it is to try the following steps:
1. Cancel the current deployment if it's still in progress.
2. Go to the repository's **Settings** > **Pages**. Find the `Source` under the **Build and deployment** section, change it to `Deploy from a branch`
3. Wait for a few seconds, then change it back to `GitHub Actions`.
4. Retrigger the deployment by pushing a new commit, or re-running the workflow under the **Actions** > **Deploy Jekyll site to Pages**.