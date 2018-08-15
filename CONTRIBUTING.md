# Contributing to Our Projects, Version 1.5

**NOTE: This CONTRIBUTING.md is for software contributions. You do not need to follow the Developer's Certificate of Origin (DCO) process for commenting on repository documentation, such as CONTRIBUTING.md, INTENT.md, etc. or for submitting issues.** 
**These guidelines were originally developed by code.mil and have been adapted for travisspark.org**

Thanks for thinking about using or contributing to this software ("Project") and its documentation!
* [Policy & Legal Info](#policy)
* [New Developer Guide](#new-developer-guide)
* [Getting Started](#getting-started)
* [Submitting an Issue](#submitting-an-issue)
* [Submitting Code](#submitting-code)
* [News and Events](#news-and-events)

## Policy

### 1. Introduction

The project maintainer for this Project will only accept contributions using the Developer’s Certificate of Origin 1.1 located at https://developercertificate.org (“DCO”). The DCO is a legally binding statement asserting that you are the creator of your contribution, or that you otherwise have the authority to distribute the contribution, and that you are intentionally making the contribution available under the license associated with the Project ("License").

### 2. Developer Certificate of Origin Process

Before submitting contributing code to this repository for the first time, you'll need to sign a Developer Certificate of Origin (DCO) (see below). To agree to the DCO, you'll add your name and email address to [CONTRIBUTORS.md](CONTRIBUTORS.md) file. At a high level, this tells us that you have the right to submit the work you're contributing and says that you consent to us treating the contribution in a way consistent with the license associated with this software (as described in [LICENSE.md](LICENSE.md)) and its documentation ("Project").

### 3. Important Points

Pseudonymous or anonymous contributions are permissible, but you must be reachable at the email provided in the Signed-off-by line.

If your contribution is significant, you are also welcome to add your name and copyright date to the source file header.

U.S. Federal law prevents the government from accepting gratuitous services unless certain conditions are met. By submitting a pull request, you acknowledge that your services are offered without expectation of payment and that you expressly waive any future pay claims against the U.S. Federal government related to your contribution.

If you are a U.S. Federal government employee and use a *.mil or *.gov email address, we interpret your Signed-off-by to mean that the contribution was created in whole or in part by you and that your contribution is not subject to copyright protections.

### 4. DCO Text

The text of the DCO is (from https://developercertificate.org):
```
Developer Certificate of Origin
Version 1.1

Copyright (C) 2004, 2006 The Linux Foundation and its contributors.
1 Letterman Drive
Suite D4700
San Francisco, CA, 94129

Everyone is permitted to copy and distribute verbatim copies of this
license document, but changing it is not allowed.

Developer's Certificate of Origin 1.1

By making a contribution to this project, I certify that:

(a) The contribution was created in whole or in part by me and I
    have the right to submit it under the open source license
    indicated in the file; or

(b) The contribution is based upon previous work that, to the best
    of my knowledge, is covered under an appropriate open source
    license and I have the right under that license to submit that
    work with modifications, whether created in whole or in part
    by me, under the same open source license (unless I am
    permitted to submit under a different license), as indicated
    in the file; or

(c) The contribution was provided directly to me by some other
    person who certified (a), (b) or (c) and I have not modified
    it.

(d) I understand and agree that this project and the contribution
    are public and that a record of the contribution (including all
    personal information I submit with it, including my sign-off) is
    maintained indefinitely and may be redistributed consistent with
    this project or the open source license(s) involved.
```

## New Developer Guide

In the spirit educating Airmen, this repository contains overviews of key concepts in contributing to open source projects. Please visit the [wiki](https://github.com/TravisSpark/spark-website/wiki) to learn about foundational concepts such as:
<ol>
  <li>Programming Languages</li>
  <li>Code Development</li>
  <ol>
    <li>Command Line</li>
    <li>Integrated Development Environments (IDEs)</li>
    <li>Troubleshooting</li>
    <li>Expert Googling</li>
  </ol>
  <li>Collaboration</li>
  <ol>
    <li>Version Control</li>
    <li>Task Delegation</li>
    <li>GitHub</li>
    <li>Open Source Licensing</li>
  </ol>
  <li>spark-website Tools</li>
  <ol>
    <li>Languages</li>
    <li>Testing</li>
  </ol>
</ol>

## Getting Started

travisspark.org is a static web site generated using a piece of software called [Jekyll](https://jekyllrb.com/) which runs in the programming language [Ruby](https://www.ruby-lang.org). Development dependencies are managed using the [Bundler gem](http://bundler.io).

This project uses Ruby version 2.3 which can be installed using a Ruby version manager like [rbenv](https://github.com/rbenv/rbenv).

```
rbenv install 2.3
```

Once you've installed Ruby 2.3, install the Bundler gem and Jekyll:

```
gem install bundler
```

### Making Changes

Now you're ready to [clone the repository](https://help.github.com/articles/cloning-a-repository/) locally and start making changes. All site pages are in the `_pages` directory and are in [Markdown format](https://daringfireball.net/projects/markdown/syntax). There is configuration in the `_config.yml` file as well as in the `_data` directory.

Once you've cloned the repository you will need to install the dependencies using bundler:

```
bundle install
```

Once you're ready to run the site generator and see the site (locally), run:

```
bundle exec jekyll serve
```

Now you can head to `http://127.0.0.1:4000` to see the site locally!

### Code Style

Code formatting conventions are defined in the `.editorconfig` file which uses the [EditorConfig syntax](http://editorconfig.org). There are plugins for a variety of editors that utilize the settings in the `.editorconfig` file. It is recommended that you install the EditorConfig plugin for your editor of choice.

Your bug fix or feature addition won't be rejected if it runs afoul of any (or all) of these guidelines, but following the guidelines will definitely make everyone's lives a little easier.

## Submitting an Issue

You should feel free to [submit an issue](https://github.com/TravisSpark/spark-website/issues) on our GitHub repository for anything you feel needs attention on the site. That includes content, functionality, design, or anything else!

### Submitting a Bug

When submitting a bug on the site please be sure to add extensive information about the problem you're having. Be sure to include (at least):

* What page you were on
* What you did (which could just be trying to load the page)
* What you expected to happen
* What actually happened (or didn't)
* Your browser (including the version number if possible)

## Submitting Code

When making your changes, it is highly encouraged that you use a [branch in Git](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging), then submit a [Pull Request (PR)](https://github.com/TravisSpark/spark-website/pulls) on GitHub. Your request will go through some automated checks using [Travis CI](https://travis-ci.org/TravisSpark/spark-website/), a continuous integration and deployment tool.

After review by the travisspark.org team, your PR will either be commented on with a request for more information or changes, or it will be merged into the codebase which will automatically deploy the changes to the live site.

To join the spark-website team, contact the TravisSpark GitHub organization administrator at 60AMW.PS.PhoenixSpark@us.af.mil

### Check Your Changes

While there are automated checks on every PR, you can run the build process locally first to ensure things are working as expected before submitting your PR. This includes running check against the built HTML using a tool called [html-proofer](https://github.com/gjtorikian/html-proofer). You can run the build and the html-proofer tool using the following command:

```
./build
```

## News and Events

The news and events listed on the website are designed to be quickly edited to reflect how often they change. Consequently, there are two data files that each contain all of the relevant news and events. These data are in a YAML format and follow a template unique to each category. If the intention is to simply change the content of news or events, only these files need to be changed. The changes will automatically be sorted and formatted.

#### News
[File Location](https://github.com/TravisSpark/spark-website/blob/gh-pages/_data/news.yml)

**title**, **author**, **org** *(press organization)*, **desc** *(description)*, and **press_link** are are self-explanatory. **section** is used to sort under which header the event will appear on the site. It must be an exact match for **Collaboration**, **Outreach**, or **Technology**. Otherwise, it will not appear. In fact, this is a good way to hide old articles that shouldn't be displayed but aren't ready to be deleted.  **date** is formatted as YYYY-MM-DD. It is used to sort the articles, from latest to earliest. 
```
- title: 
  author: 
  org: 
  date: #YYYY-MM-DD
  desc: 
  press_link: 
  section: 
```

#### Events
[File Location](https://github.com/TravisSpark/spark-website/blob/gh-pages/_data/events.yml)

**title**, **location**, **desc** *(description)*, and **event_url** are are self-explanatory. **section** is used to sort under which header the event will appear on the site. It must be an exact match for **Courses**, **Conferences**, or **Weekly Meeting**. Otherwise, it will not appear. In fact, this is a good way to hide old events that shouldn't be displayed but aren't ready to be deleted. Because events have different dates or can be recurring, **Text_date** is used only for display purposes. This gives it flexibility in its format. **start_date** is read as a date. It is formatted as YYYY-MM-DD. It is used to sort the events, from earliest to latest. Some recurring events are set far into the past, to make sure they always appear on top. 

```
 - title: 
   location:
   desc: 
   event_url:
   section: ## Sections: Courses, Conferences, Weekly Meeting
   text_date: ## <string> For Display
   start_date:  ## <YYYY-MM-DD For Sorting
```
