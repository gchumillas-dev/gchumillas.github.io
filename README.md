# Personal website

A personal website developed in [Jekyll](https://jekyllrb.com/), a static site generator.

## How to run the website locally

The following instructions are based on [this page](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll).

1. Verify that Ruby 2.1.0 or higher is installed or [install it](https://www.ruby-lang.org/en/downloads/):

```bash
$ ruby --version
> ruby 2.X.X
```

2. Install Bundler:

```bash
$ gem install bundler
```

3. Install Jekyll and other dependencies from the GitHub Pages gem:

```bash
$ bundle install
```

4. Install watchy:

```bash
$ npm install -g watchy
```

5. Run your Jekyll site locally:

```bash
$ watchy -w _config.yml -- jekyll serve --watch
```

**Additional information:** The following command won't work, since the website contents are located in the `_config.yml` file, and the Jekyll server doesn't reload when that file changes:

```bash
jekyll serve --watch
```

That's the reason why we use [whatchy](https://www.npmjs.com/package/watchy) to reload the server.
