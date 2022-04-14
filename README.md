## My Personal Website. <a href="http://sayakbiswas.github.io/">Here!</a> [![Build Status](https://travis-ci.org/sayakbiswas/sayakbiswas.github.io.svg?branch=master)](https://travis-ci.org/sayakbiswas/sayakbiswas.github.io)

<p align="center">This is a repository for my personal website. This will also hold my blog migrated from sayakbiswas.wordpress.com.
This site is based on the brilliantly minimalist <a href="https://github.com/sergiokopplin/indigo">Indigo theme</a> by <a href="https://github.com/sergiokopplin">Kopplin</a></p>

***

![Screenshot](http://sayakbiswas.github.io/assets/images/screenshot.png)

***

## Changes from Base Theme
1. Changes to font families and font sizes throughout.
2. Added some CSS classes for blog posts.

***

## Setup
1. Clone repo.
2. Install Jekyll, NodeJS and Bundler.
3. `bundle install`
4. `bundle exec jekyll serve --config _config.yml,_config-dev.yml`
5. Site can be viewed at `http://localhost:4000`

## Changes and Deployment
1. Switch to gh-pages branch using `git checkout gh-pages`.
2. Make changes and preview using commands described in the earlier section.
3. Commit and push to `origin/gh-pages`.
4. Switch to master using `git checkout master`.
5. Merge from `gh-pages` using `git merge gh-pages`.
6. Push to `origin/master`.

## License

[MIT](http://kopplin.mit-license.org/) License © Sérgio Kopplin
