---
title: Komunitas Bukalapak API Reference

language_tabs:
  - shell

toc_footers:
  - <a href='https://www.bukalapak.com/register'>Register for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - topics
  - comments
  - tags
  - search
  - users
  - notifications

search: true
---

# Introduction

Welcome to the Komunitas Bukalapak API! You can use our API to access Komunitas Bukalapak API endpoints, which can get information on topics, comments, users, etc.

# Authentication


Komunitas Bukalapak uses combination of user_id and API token to allow access for required authentication’s resources. Bukalapak expects for the user_id and API token to be included in all API requests to the server in request that looks like the following:

`curl -u user_id:token`

You can get your user_id and API token after you login [here](http://bukalapak.github.io/api/#authentication).
