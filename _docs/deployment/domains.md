---
layout: default
title: Domains
parent: CMS deployment
grand_parent: Deploying cyhoeddwn
nav_order: 3
has_children: false
last_modified_date: 2021-07-03 16:38
---

# Domains

In order to create a successful deployment, you'll need to send your users to a memorable domain name. A domain name is formed of two main parts: a top-level domain (TLD), which is the final part of the domain that is read, and lower-level domains, which come further back in the domain name.

In the domain name `help.cyhoeddwn.wales`, `.wales` is the TLD, subdomains on this TLD are managed by many third party companies on behalf of [Nominet](https://www.nominet.uk/). The second-level domain is `cyhoeddwn`, which is registered with Nominet by [IONOS](https://ionos.co.uk). `help` is a subdomain of `cyhoeddwn.wales`, which has a `CNAME` record that points to `cyhoeddwn.gitlab.io` (where the site is stored) along with a `TXT` record that tells GitLab that the site belongs to the correct persons and that when `cyhoeddwn.gitlab.io` is accessed from `cyhoeddwn.wales`, it needs to load the static site for the help website. Phew, that was a lot of information, let's break it down!

## Why do we need a domain?

The domain name system (DNS) is a wonderful system that (amongst other things), converts human-readable addresses (like `google.com`) to IP addresses (a series of numbers separated by decimal points, like `142.250.180.14` — at the time of writing, this is the IP address in use for the UK version of Google). While you can get away with not having a domain name, or using a domain name that is provided to you by a hosting service (like for example: `cyhoeddwn.herokuapp.com`), this is a bit clunky to remember, and makes it more difficult for people in your community to use your website.

## Where can we get a domain? 

Domains are available to purchase from many registrars on the internet, such as [Google Domains](https://domains.google.com/registrar/) or [IONOS](https://ionos.co.uk). Domain registration can be relatively inexpensive, at only a few pounds per year. While you are free to use your own domain to host your instance of cyhoeddwn on, we recommend that [you ask the project contributors](mailto:contact-project+cyhoeddwn-cyhoeddwn-support@incoming.gitlab.com) to set up you a subdomain on the `cyhoeddwn.wales` domain, which will be free (gratis) to you, so long as you use it for cyhoeddwn-related purposes only. When you do this, be sure to include which DNS entries are required. Your email should look something like:

> I would like to set up a subdomain for an instance of cyhoeddwn, the subdomain I require is: `example-subdomain`
> The DNS settings required are:

> `example-domain.cyhoeddwn.wales 3600 IN CNAME somedomain-asd34asd.herokudns.com`

> `example-domain.cyhoeddwn.wales 3600 IN MX 10 mxdomaina.example.com`

> `example-domain.cyhoeddwn.wales 3600 IN MX 10 mxdomainb.example.com`
