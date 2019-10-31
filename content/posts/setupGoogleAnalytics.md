+++ 
draft = false
date = 2019-10-31T00:06:19Z
title = "Setting up Google Analytics"
description = ""
slug = "" 
tags = []
categories = []
externalLink = ""
series = []
+++

These are the steps I took to set up Google Analytics and link it to this website of mine.

1. The first thing to do is set up a [Google Analytics account](https://analytics.google.com/analytics/web/?authuser=0#/provision) with your google account.
2. From the resulting dashboard, click on 'ADMIN' at the bottom left. With your account selected, expand `Tracking Info` under `Property`, and then click on `Tracking Code`. Your unique Tracking ID will be displayed.
3. Open the `config.toml` file of your website and add `googleAnalytics` variable if it is not already there, and set your Tracking ID to it.
4. Copy the `header.html` file from `themes/<YOURTHEME>/layouts/partials/`. Paste the copy into the `layouts/partials/` folder of the root of your website. 
5. Add {{ template "_internal/google_analytics.html" . }} to your header.html.