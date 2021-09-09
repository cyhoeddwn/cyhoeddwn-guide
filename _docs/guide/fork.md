---
layout: default
title: Forking cyhoeddwn-guide
parent: Maintaining the guide
nav_order: 2
has_children: false
last_modified_date: 2021-06-09 20:42
---

# Forking cyhoeddwn-guide
{: .no_toc }

<details close markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

## Overview

## Step-by-step

Visit the [GitHub mirror](https://github.com/cyhoeddwn/cyhoeddwn-guide) of the cyhoeddwn-guide repository and click on the 'Fork' button in the top-right corner. Select your organization on the 'Where should we fork cyhoeddwn-guide?' dialogue box. You are now ready to set up the forked repo's settings.

![](/assets/img/guide/github/fork.png)
![](/assets/img/guide/github/forked_repo.png)

### Options

|Tag|Parent|Item|Action|
|---|------|----|------|
|Necessary|Features|Issues|On|
|Recommended|Features|Preserve this repository|Off|
|Recommended|Features|Table of contents|Off|
|Necessary|Features|Discussions|On|
|Recommended|Merge button|Allow auto-merge|On|

### Branches

You'll need to add branch protection rules to add the required democratic functions to GitHub. Add the following branch protection rules by clicking the 'Add rule' button and then changing the following rules (numbered items have additional description given following this list):

- Pattern name: `master`
- Require pull request review before merging: mandatory on (1)
  - Dismiss stale pull request approvals when new commits are pushed: mandatory on
  - Restrict who can dismiss pull request reviews: mandatory on (2)
- Require status check before merging: mandatory on (3)
- Require conversation resolution before merging: optional on (4)
- Restrict who can push to matching branches: mandatory on (2)
- Allow force pushes: mandatory on (5)
- Allow deletions: mandatory on (5)

1. Select the number of approving reviews, this can be between 1 and 6 inclusive
2. Set this to members who have administrator and/or oversight responsibilities
3. Add `jekyll` to this list
4. To allow for discussions to conclude
5. Set this to members who have administrator responsibilities

### Pages

Select the `gh-pages` branch from the drop-down and then click 'Save'. Enter your chosen domain in the provided box, if you do not have a custom domain, you can [ask for one to be provided for you]({% link _docs/deployment/domains.md %}). Make sure to provide the following in your request, filling in as appropriate:

> `[requested-domain].cyhoeddwn.wales 3600 IN CNAME [your-organization-name].github.io`

If you are not using a subdomain on `cyhoeddwn.wales`, please follow the instructions provided on the page. After you have configured your DNS settings and added your domain, GitHub will automatically configure your TLS certificate. You should return in about 24 hours to enable 'Enforce HTTPS' when the certificate has been provisioned.

![](/assets/img/guide/github/gh_pages.png)