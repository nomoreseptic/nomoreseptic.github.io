---
layout: page
title: Now
update: 2020-03-03
tagline: What I'm doing now
permalink: /now.html
ref: now
order: 0
---

I added an initial css-animated logo to the Contact Page. It needs work yet. I, also, see my "Now" page date is not updating, so I will be checking on that.

I fixed an issue with the routing of my post links on github when they functioned perfectly on my local machine. It seems I accidently deleted some front matter and permalinks or reverted git too far back in my site building. However, I am glad to have been faced with the challenge of fixing the issue because it helped me understand th path variables and how they are used on github. My site is not configured exactly as before because I learned how to make use of ```baseurl```. This page instantly shed enlightment on ```baseurl```:[Clearing Up Confusion Around baseurl -- Again](https://byparker.com/blog/2014/clearing-up-confusion-around-baseurl/)

Prior to the above, I was working on (and will continue to improve upon) displaying [SVG images](Awaiting-my-Slate-for-SVG) along with their animation on this jekyll github-pages site. The following is an animated svg image.

{::nomarkdown}
<svg width="200" height=200>
    <circle id="circle-fade" cx="150" cy="100" r="10" fill="blue"/>
</svg>
{:/}
