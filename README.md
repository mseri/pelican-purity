# Purity Ghost Theme

`purity` is a  [MathJax](http://www.mathjax.org) ready [Pure](http://purecss.io) based theme for [Ghost](http://github.com/tryghost/ghost/).
It is already integrated with [microdata](https://support.google.com/webmasters/answer/176035?hl=en) for search engine optimization and opengraph for better facebook integration.

You can see a running version of the dark theme is on my blog [Tales of a Fractal Spectrum](http://ghost.mseri.me).

Please note that this new version integrates some changes of Ghost 0.4.* and will not work on older installations. **Consider upgrading Ghost to version 0.4.1 before upgrading the theme!**

## What does the ZIP contain
The zip contains the full theme with a detailed README and two main color schemes: dark and light. They can be easily switched or personalized following the instructions contained in the README. 

It is ready to be integrated with your favorite social networks, ready to be used with google+, disqus or Facebook comments and ready to be integrated with google Analytics. Until this will be made automatic with the introduction of plugins in Ghost, you will find detailed instructions on the README file.

_For some of the following operations you need to edit css or hbs files. Use your favourite pure text editor for the purpose. Please avoid Office, LibreOffice/OpenOffice or similar suites._

## Install the theme
Decompress the zip file inside the folder `content/themes/` of your Ghost blog.

## Change color theme
Open the file `assets/css/style.css` and replace the line `@import url(dark.css);` with `@import(light.css);`.
To make your own color set, duplicate `assets/css/dark.css` or `assets/css/light.css`, edit it (you need to know/study a bit of [CSS](http://www.w3schools.com/cssref/pr_text_color.asp)) and replace the line `@import url(dark.css);` with `@import(NAME_OF_YOUR_CUSTOM_COLOR_FILE.css);`.

## Update your social network informations
Open the file `default.hbs` and look for the following lines

```
	<ul class="social-list">
	    {{! In the following six lines edit the links between the quotations marks close to href= with the appropriate content }}
	    <li class="social-item"><a class="subscribe icon-twitter" href="http://www.twitter.com/..." target="_blank"></a></li>&nbsp;
	    <li class="social-item"><a class="subscribe icon-facebook" href="http://www.facebook.com/..." target="_blank"></a></li>&nbsp; 
	    <li class="social-item"><a class="subscribe icon-google-plus" href="http://plus.google.com/..." target="_blank" rel="publisher"></a></li>&nbsp;
	    <li class="social-item"><a class="subscribe icon-github" href="http://www.github.com/..." target="_blank"></a></li>&nbsp;
	    <li class="social-item">&nbsp;</li>
	    <li class="social-item"><a class="subscribe icon-feed" href="{{@blog.url}}/rss/" target="_blank"></a></li>
	</ul>
```

The `icon-SocialNetworkName` identifies which icon is used, slightly on its right you see something like `href="A_Link_..."`. You should replace the content of the quotation marks with the appropriate link to your social network page, or delete the line if you don't have one.
Duplicating those line and editing the name of the icon and the link will add additional social networks, the full list of supported networks is: twitter, google-plus, facebook, linkedin, github, bitbucket, cloud, youtube, flickr, dropbox, tumblr, skype.

## MathJax support
To enable MathJax (if you don't know it, probably you don't need it) it is enough to open the file `default.hbs` and completely delete the two lines containing the text `REMOVE THIS LINE TO ENABLE MATHJAX`.

## Google Analytics support
After having obtained your Account Code from [analytics.google.com](http://analytics.google.com), it is a code of the form `UA-12345678-1`, open the file `default.hbs`, completely delete the two lines containing the text `REMOVE THIS LINE TO ENABLE GOOGLE ANALYTICS` and replace `REPLACE_THIS_TEXT_WITH_THE_ACCOUNT_NUMBER_GIVEN_BY_GOOGLE` with your account code.

## Google+, Disqus or Facebook comments
To set up google+, disqus or facebook comments is enough to open `posts.hbs`, and remove the appropriate lines at the end of the file (they are marked with `REMOVE THIS LINE TO ENABLE ...`). 
For [Disqus](http://disqus.com) you additionally need to register to their website and obtain a website identifier.
You can add the Comments counter on the index page modifying the code according to [Another way of enabling disqus on Ghost](http://blog.reggiesuplido.com/another-way-of-enabling-disqus-on-ghost/).

## Support
I will be updating this theme as-needed for as long as possible following your needs and integrating the features added at each new release of Ghost. 
I will provide general support on getting it setup. I'm unable to guarantee 'lifetime' support or anything of the sort currently however I'll support it for as long as possible.

## Why use pay-what-you-want?
I was inspired by Bios Elemental and decided to try is same experiment. I believe in the open circulation of knowledge and in open-source. I don't want to restrict who can access it, but I still need to eat. If you like this theme and want me to continue work on it and similar projects, please chip in whatever you think it's worth.