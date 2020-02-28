---
layout: page
title: Now
update: 2020-02-28
tagline: What I'm doing now
permalink: /now.html
ref: now
order: 0
---

My next task I believe will be to get my post-listings-by-categories page up and running. At the moment I am trying to fix a problem with the addressing of my original first 3 posts on this site. All works fine on my local machine, but they are not showing on github. I will get the the bottom of it asap!

Since posts use the date in the file name, and I am only wanting an automatic date for a now page, I am abandoning my quest for automatic
date modification. There is a github plugin for this but it is not white-listed by github and, therefore does, not work on the gh-pages site. 

I have actually solved this problem with a local pre-commit git hook to modify a custom now.md front matter "update" variable. Woo Hoo! Now, I might want to delete the old "update" or replace it with new one. My only complaint now is that the UTC time is not exact to my region, but that may not be worth worrrying about. I will investigate.

Prior to the above, I was working on (and will continue to improve upon) displaying [SVG images]({{ '/web/2020/02/20/SVG-Animations' }}) along with their animation on this jekyll github-pages site. The following is an animated svg image.

{::nomarkdown}
<svg width="200" height=200>
    <circle id="circle-fade" cx="150" cy="100" r="10" fill="blue"/>
</svg>
{:/}
