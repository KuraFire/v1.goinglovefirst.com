---
title: Remove The ‘fbclid’ Parameter From URLs
category: how-to
excerpt: Clean URLs help reveal some of the subtle things I’m doing on this site.
tags: [Technical Posts]
---

## Why I strip the Facebook “click ID” parameter
The `?fbclid=<hash>` parameter litters the world’s bookmarks, pinboard pins, and <dfn><abbr title="Universal Resource Locator">URL</abbr></dfn>s all around. Want to share that [interesting article](https://www.abc.net.au/triplej/programs/hack/coronavirus-covid19-isolation-third-quarter-phenomenon-has-begun/12190270) with a friend? Copy, paste and… *what is all this junk?!*

<pre>
https://www.abc.net.au/triplej/programs/hack/coronavirus-covid19-isolation-third-
quarter-phenomenon-has-begun/12190270?<mark><b>fbclid=IwAR3MvgCDBX9v2MWMEIJ8n6TaA0O-
pmBIGsDqGiKFqI59djXjT6duQZyPNxs</b></mark>
</pre>

When people share a page or article from _Going Love First_, I want them to have a clean and enjoyable experience, especially if they’re manually interacting with the link. The `fbclid` junk messes with that, and distracts from some of the intentional little things I’m doing with the URLs across this site.

To improve that experience, across this site I strip that junk from the URL after the page loads.

(I also _suspect_ Facebook is using this to extend its awareness of your social network by tracking which people follow your unique `fbclid` links, suggesting connections that you may not have on the site itself. But note: I have no evidence for this.)

## How to remove the `fbclid` parameter

This is a simple, modern, and [widely supported](https://caniuse.com/#feat=urlsearchparams) solution that uses dedicated <dfn><abbr title="Application Programming Interface">API</abbr></dfn>’s for interacting with search parameters (which the `fbclid` is hijacking). In the case of this particular *gist* (code snippet) below, it uses jQuery for the `document.ready` check, because honestly, that just allowed me to easily implement it on goinglovefirst.com and it’s a more widely understood technique:

<script src="https://gist.github.com/KuraFire/4f9deec8e2a2f3316a9e083f14c4bb07.js"></script>
