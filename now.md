---
layout: page
title: Now
update: 2020-02-28
tagline: What I'm doing now
permalink: /now.html
ref: now
order: 0
---

My have my post-listings-by-categories page up and running. At the moment I am trying to fix a problem with the addressing of my original first 3 posts on this site, both on the home page and on the topics page. All works fine on my local machine, but they are not showing on github. I have tried numerous things, and it makes no sense that the other test pages I put up are linked up fine, and they are built the same. As per my GLITCH post, I am just going to sit on this for a few days to make progress in other areas to see if something resolves on Github.

I was able to get this 'NOW' page to update with a local pre-commit git hook to modify a custom now.md front matter "update" variable. Woo Hoo! Now, I might want to delete the old "update" or replace it with new one. My only complaint now is that the UTC time is not exact to my region, but that may not be worth worrrying about. I will investigate.

Prior to the above, I was working on (and will continue to improve upon) displaying [SVG images]({{ '/web/2020/02/20/SVG-Animations' }}) along with their animation on this jekyll github-pages site. The following is an animated svg image.

{::nomarkdown}
<svg width="200" height=200>
    <circle id="circle-fade" cx="150" cy="100" r="10" fill="blue"/>
</svg>
{:/}
