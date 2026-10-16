# larsonrecipes.com

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

## Website hosting

The website is built with Middleman and hosted on GitHub Pages.
Pushing to `master` runs `.github/workflows/pages.yml`, builds the static
files, and deploys `build/`. Pull requests build without deploying.

### Local development

Use the Ruby version in `.ruby-version` and an installed Node.js runtime:

```sh
bundle install
bundle exec middleman server
```

To generate the published site:

```sh
bundle exec middleman build
```

### Domain

GitHub Pages uses the custom domain `larsonrecipes.com`. Domain registration
and DNS are managed in Squarespace, using Squarespace's nameservers.
The website does not depend on DreamHost.

| Type | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | ewlarson.github.io |

Keep the custom domain in the repository's Pages settings, and enable
Enforce HTTPS after GitHub provisions its certificate.
