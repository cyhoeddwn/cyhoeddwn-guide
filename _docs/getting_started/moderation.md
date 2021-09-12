---
layout: default
title: Post Moderation
parent: User guide
nav_order: 7
has_children: false
last_modified_date: 2021-07-28 10:56
---

# Post Moderation
{: .no_toc }

<details close markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

Cyhoeddwn is based around a community moderation system, where the community is responsible for deciding what content is set to be displayed.

## Overview

Each post contains zero, one, or many reviews. A review contains some free text (up to 500 characters) to allow for appraisal or commentary on a post along with a boolean marking if the post is approved or not. Each time a post receives an update (either an edit of the content, or the addition or removal of a review), the system determines if the post should be displayed or not. This follows the following basic logic:

> The post is set to display if both of the following conditions are met: the post has at least three reviews and the post has a simple majority (> 50%) of positive reviews (compared to negative ones).

You'll get an email notification when your post has been approved, so no need to keep refreshing your post's page!

## Creating a review

To create a review on a post, you must be logged in as a user that is not the post's author. Start by clicking on the 'X review(s)' link under the post (where X is a number). This will bring up the post review view, click the 'Create review' button, and compose your review in the box provided. Tick the checkbox if you would like to mark your review as 'Approved', leave it unchecked if not.

!['Create review' view, a preview of a post advertising a car for sale is on the left, the review panel is on the right. There is one positive review.](/assets/img/create_review.png)

!['Write a review' view, the user is authoring a review that is critical of an advert for selling a car.](/assets/img/write_a_review.png)

!['Create review' view, a preview of a post advertising a car for sale is on the left, the review panel is on the right. There is one positive and one negative review.](/assets/img/you_have_left_a_review.png)

## Deleting a review

Navigate to the post's review page and click the 'Delete review.' link, you will be asked to confirm your action.