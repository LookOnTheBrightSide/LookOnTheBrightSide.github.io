---
layout: post
title:  "Portfolio redesign"
permalink: /blog/:title
categories: Design
introduction: How and why I made this website.
---
##### Moving

So when I moved to Dublin from Cape Town I knew I was going to face a challenge. That challenge would be to find a job doing what I love the most - making websites!

##### Err ...

I previously had a portfolio that I had made using Ruby on Rails. The problem with this site though, was that using RoR is overkill for something like a blog/portfolio site. The decision to use Rails had been prompted by the fact that at the time I had just been accepted as an intern at [Platform45](https://www.Platform45.com/){:target="_blank" .site-link} (a Rails shop) so I needed to get some practice.

##### Enter Jekyll

![jekyll logo](https://jekyllrb.com/img/logo-2x.png){: .img-fluid .img-center}

The decision to use RoR was obviously a bad one so I decided to redo it. I did some research and considered my options. The site [StaticGen](http://www.staticgen.com/){:target="_blank" .site-link} helped me narrow my choices down to middleman/ghost/jekyll.

I had used middleman as an intern at [Platform45](https://www.Platform45.com/){:target="_blank" .site-link} before so I thought I should challenge myself and learn something new. It was for this reason that I chose Jekyll. I then went through the docs and [this](https://www.youtube.com/watch?v=oiNVQ9Zjy4o&list=PLWjCJDeWfDdfVEcLGAfdJn_HXyM4Y7_k-){:target="_blank" .site-link} video course on youtube which proved to be enough to get my MVP out.

##### Design

Time was not on my side but I needed to quickly mock up a clean design for my site. I used trusty old Photoshop and this is what I came up with.

![beercan site mock up done in Photoshop](http://i.imgur.com/e8Ewwct.png){: .img-fluid .img-center}


I used Brandon Grotesque in the initial design but then swapped it for a faster Roboto. This was enough to get my MVP out, which is the site that you are on now!

##### Comments

The best way to learn in my opinion is through your peers, so I decided to add a comments section. I am using [disqus](https://www.disqus.com/){:target="_blank" .site-link} for this and the implementation was really as easy as pie.

##### Lessons learnt

I really enjoyed working on this site. What helped a lot was my decision to get all my content together before starting to code. I had a clear picture of what I wanted to achieve before even opening the editor. It was amazing how much it helped me to keep my code lean and it was also so much easier for me to "think in components" just from looking at the design. I reused a lot of css classes, which is good practice, and I managed to keep the said code somewhat [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself){:target="_blank" .site-link}.

****
If anyone is interested in this site, please let me know and
I'll turn it into a theme and Open Source it.
