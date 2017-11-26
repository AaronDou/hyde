---
layout: post
title: How I built this site
---

Wow, this is the first tech blog I've ever written in my life. I'm gonna talk about how I built this website. If you like the looking of the site, you will find it useful.

The site is forked from [Poole](https://github.com/poole), which is called by its author "the butler for [Jekyll](https://jekyllrb.com/)". Jekyll is a famous tool for generating static sites with beautiful Markdown syntax, and Poole simply makes it much more straightforward to use. There are currently two official themes built on Poole, [Hyde](http://hyde.getpoole.com/) and [Lanyon](http://lanyon.getpoole.com/). Personally, I like the two-column layout of Hyde. I host the generated site on [Github Pages](https://pages.github.com/), which fully supports and even advocates blogging with Jekyll. Let's assume you also prefer Hyde and would like to host your site for free on Github Pages, here are what you need to do step by step.

* Fork the [Poole](https://github.com/poole) repo, rename the repo name to **yourgithubusername**.github.io. Repace **yourgithubusername** with your github user name. 
* Clone the repo to your local machine so that you can edit locally. 
`git clone https://github.com/yourgithubusername/yourgithubusername.github.io.git`
* Install Jekyll to your local machine by `sudo gem install jekyll`. 
* Almost done. Before you can see the actual site in your browser, some incompatibility issues due to fact that the Poole repo is based on an old version of Jekyll need to be adressed. Locate `_config.yml` and change the first few lines to the following. Install plugin packages by `sudo gem install jekyll-gist jekyll-paginate`.
{% highlight ruby linenos %}
# Dependencies
plugins:
  - jekyll-gist
  - jekyll-paginate

# markdown:         redcarpet
highlighter:      rouge

# Permalinks
permalink:        pretty
# relative_permalinks: true
{% endhighlight %}
* Now ready to see your site? Go to the root directory of your cloned repo, start a Jekyll server by typing `jekyll serve` in your terminal. Open [http://localhost:4000](http://localhost:4000) in your browser, and here you go!







