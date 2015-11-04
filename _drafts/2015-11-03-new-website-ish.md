---
title:  "New Website-ish"
description: Github Pages, Jekyll, and the Meaning of Life
date: 2015-11-03 14:50:00
---

What were you waiting for? I've been busy with other worthwhile things. You know, for example, not talking about myself.

I suppose I'll take this opportunity to describe the road I ended up going down toward this result. In other words, the obligatory post about why and how I'm contributing my words to the internet. I've known about Github Pages for quite some time and have used it for a few things over the years. In particular, [Death Metal Family Radio](http://deathmetalfamilyradio.com/) and some legacy [API Documentation for CheddarGetter](cg-docs).

## First Foray into Jekyll

The Death Metal Family Radio site was something I helped get started for the [Bloomington Playwrights Project](http://www.newplays.org/) show, [Death Metal Podcast for Kids](http://www.newplays.org/node/376?sc1=yes&subnid=377) at the [Indianapolis Fringe Festival](http://www.indyfringe.org). We used a [Twitter Bootstrap](http://getbootstrap.com) structure and recreated a few style elements from some themes found laying around. Yes, it's supposed to look like that. [Jekyll](jekyll) was used to generate the static content and it's served via [Github Pages](https://pages.github.com/). The code is [here](https://github.com/bppwrite/deathmetalfamilyradio).

## REST API Documentation Framework Selection

The [API Documentation for CheddarGetter](cg-docs) is the third incarnation of the same documentation we've had for years. In preparation for a new set of documentation, we needed a new place for it to live so we could be more flexible with making changes. @maggieoconnor did much of the legwork on researching the available modern REST API documentation frameworks. The short list ended up including just a few candidates:

* [Swagger](swagger)
* [Slate](slate)
* [FlatDoc](flatdoc)

Our criteria for choosing a documentation framework was fairly straightforward:

* Play nice with our current documentation direct links
* Include inline example code in multiple different languages
* Searchable
* Play nice with search engines indexers
* Easy to get going
* Enable the public to contribute fixes and improvements
* Developer friendly - ideally a one-page design, static page(s)

[Swagger](swagger) is way bigger than what we were looking for. The learning curve was too much and the result using the standard Swagger UI is a bit clunky and ugly. As a result, we were generally turned off by it. I am, however, currently writing our new API specification in Swagger from the bottom up, so expect a post about that soon.

[FlatDoc](flatdoc) at first glance is a really nice approach to the problem. In the end, we decided against it because of the potential SEO implications brought on by the heavy client-side processing. We didn't do enough research to determine if that was a valid concern, so take that for what it's worth.

We ended up going with [Slate](slate). It has it's own issues but they were fewer and less of a problem than the alternatives. The end product is slick and it's easy to deploy changes. We [contributed Vagrant support](https://github.com/tripit/slate/pull/350) to it once we got everything smoothed out.



[jekyll]:     http://jekyllrb.com
[swagger]:    http://swagger.io/
[flatDoc]:    http://ricostacruz.com/flatdoc/
[slate]:      https://github.com/tripit/slate
[cg-docs]:    http://docs.cheddargetter.com
