---
layout: default
title: Example workflow
parent: Maintaining the guide
nav_order: 3
has_children: false
last_modified_date: 2021-06-09 20:42
---

# Example workflow
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
Now we have the forked GitHub repository up and running, it's now possible to start using GitHub's tools for contributing and running the system democratically. It would be impossible to summarise all GitHub has to offer in this guide, so provided here is an example workflow with a scenario for adding a new page. If you are unfamiliar with using GitHub, the [GitHub docs](https://docs.github.com/en/get-started/onboarding/getting-started-with-your-github-account) provide a good primer.

## Step-by-step
Let's say someone has the idea to add the names/contact details for oversighters on the wiki for accountability and to raise issues. You could start this by creating a discussion on your forked GitHub repository for `cyhoeddwn-guide`.

![](/assets/img/guide/github/site_pre_edit.png)

Click on the discussions tab and raise a new discussion, adding a title and description as necessary, we'll add the 'Ideas' tag here:

![](/assets/img/guide/github/new_discussion.png)

This will show up on the discussion board, for all to see. Assuming it gets enough traction, it could be made into an issue. An issue is a request to fix code or writing, let's assume someone has opened this as an issue, it will appear in the issues board.

![](/assets/img/guide/github/issues_page.png)

If you are planning to author a long change, or add many new files, you should clone the directory, make changes locally, and then push to a new branch. If you are unfamiliar with using Git/GitHub, [this video](https://www.youtube.com/watch?v=1qJ5YNJRLtU) provides a good primer. In this case, we'll use the online file editor to add changes and commit them.

![](/assets/img/guide/github/adding_commit.png)

Here we are opening a [pull request](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests), which will be dealt with according to the settings configured by your administrator.

![](/assets/img/guide/github/adding_pr.png)

![](/assets/img/guide/github/merge_pr.png)

In this case, auto-merge has deemed the pull request to be non-breaking, hence giving us the option to merge. This will depend on the settings used in your fork. Here we have merged the changes, and GitHub Actions has rebuilt and hosted the changes requested:

![](/assets/img/guide/github/site_post_edit.png)