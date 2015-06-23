# Purity Ghost Theme

`purity` is a  [MathJax](http://www.mathjax.org) ready [Pure](http://purecss.io) based theme for [Pelican](http://blog.getpelican.com/). Adapted from the [Purity Ghost theme](https://github.com/mseri/purity).
It is already integrated with [microdata](https://support.google.com/webmasters/answer/176035?hl=en) for search engine optimization and opengraph for better facebook integration.

You can see a running version of the dark theme is on my blog [Tales of a Fractal Spectrum](http://www.mseri.me).

## Change color theme
Open the file `static/css/style.css` and replace the line `@import url(dark.css);` with `@import(light.css);`.
To make your own color set, duplicate `assets/css/dark.css` or `assets/css/light.css`, edit it (you need to know/study a bit of [CSS](http://www.w3schools.com/cssref/pr_text_color.asp)) and replace the line `@import url(dark.css);` with `@import(NAME_OF_YOUR_CUSTOM_COLOR_FILE.css);`.

## Update your social network informations
Set `SOCIAL= True` and any of the follwing variables with you username: `TWITTER`, `FACEBOOK`, `GPLUS` (for Google+) and `GHUB` (for GitHub).
Alternatively open `templates/social.html` and add anything you need (it's a fairly easy task).

Probably there is a default/standard way to manage the social settings; feel free to submit a Push Request with any fix.

## MathJax support
To enable MathJax it's enough to set `MATHJAX = True`.

## Google Analytics support
After having obtained your Account Code from [analytics.google.com](http://analytics.google.com), it is a code of the form `UA-12345678-1`, add the constant `GOOGLE_ANALYTICS = your_code_goes_here`.

## Google+, Disqus or Facebook comments
To set up google+, disqus or facebook comments is enough to set `DISQUS_SITENAME`, `GOOGLE_COMMENTS` or `FBCOMMENTS_ID`

_Note that for Disqus you may want to open `templates/comments.html` and comment out the line `var disqus_identifier = '{{ article.id }}';`._

## Added basic support for EU Cookies Law
For additional information check the file `templates/cookieconsent.html` and the used script [Cookie-Consent](https://silktide.com/tools/cookie-consent/).

As it stands now it will just inform the user and point him/her to the page `http://{{ SITEURL }}/privacy-policy`. Enable it with `COOKIECONSENT = True`

## TODO
This theme does **not** yet implement `archives`, `author`, `category`, `page` templates. Feel free to send a Push Request with the appropriate changes.

This theme does not (yet) include an appropriate `pygments` css file.
