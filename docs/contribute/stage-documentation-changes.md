---
title: Staging Your Documentation Changes
---

{% capture overview %}
This page shows how to stage content that you want to contribute
to the IFC documentation.
{% endcapture %}

{% capture prerequisites %}
Create a fork of the IFC documentation repository as described in
[Creating a Documentation Pull Request](/docs/contribute/create-pull-request/).
{% endcapture %}

{% capture steps %}

## Staging from your GitHub account

GitHub provides staging of content in your master branch. Note that you
might not want to merge your changes into your master branch. If that is
the case, choose another option for staging your content.

1. In your GitHub account, in your fork, merge your changes into
the master branch.

1. Change the name of your repository to `<your-username>.github.io`, where
`<your-username>` is the username of your GitHub account.

1. Delete the `CNAME` file.

1. View your staged content at this URL:

        https://<your-username>.github.io

## Staging a pull request

When you create a pull request, either against the master or &lt;vnext&gt;
branch, your changes are staged in a custom version of the docs site to ensure that nothing breaks.(perhaps integrate netlify CI to custom domain& stage)

1. In your GitHub account, in your new branch, submit a pull request to the
bigdoods/bigdoods.github.io repository. This opens a page that shows the
status of your pull request.

## Staging locally

1. [Install Ruby 2.2 or later](https://www.ruby-lang.org){: target="_blank"}.

1. [Install RubyGems](https://rubygems.org){: target="_blank"}.

1. Verify that Ruby and RubyGems are installed:

        gem --version

1. Install the GitHub Pages package, which includes Jekyll:

        gem install github-pages

1. Clone your fork to your local development machine.

1. In the root of your cloned repository, enter this command to start a local
web server:

        jekyll serve

1. View your staged content at
[http://localhost:4000](http://localhost:4000){: target="_blank"}.

<i>NOTE: If you do not want Jekyll to interfere with your other globally installed gems, you can use `bundler`:</i>

 	gem install bundler
 	bundle install
 	bundler exec jekyll serve

<i> Regardless of whether you use `bundler` or not, your copy of the site will then be viewable at: [http://localhost:4000](http://localhost:4000)</i>

{% endcapture %}

{% capture whatsnext %}
* Learn about [writing a new topic](/docs/contribute/write-new-topic/).
* Learn about [using page templates](/docs/contribute/page-templates/).
* Learn about [creating a pull request](/docs/contribute/create-pull-request/).
{% endcapture %}

{% include templates/task.md %}
