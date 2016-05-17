---
layout: post
title: Broadway Now CLI Gem!
---

I am now the brand new author of a Ruby Gem! :tada::dancer: It is called Broadway Now and it shows the 20 most popular Broadway Shows currently playing in NYC. The project took me about 4 days to complete, although I spent what felt like most of the time troubleshooting the publishing of the gem. This project was a [Learn](https://learn.co/verified/?coupon=lv-student-referral-25&utm_campaign=Learn%20Student%20Referral%20Program&utm_medium=In%20App%20Email&utm_source=Learn.co%20Email%20Drips) assignment, I was tasked with building and publishing a command line interface (CLI) gem that scrapes data and displays it.

#### Project Requirements :mag:

  ✓ Package as a gem.
  
  ✓ Provide a CLI on gem installation.
  
  ✓ CLI must provide data from an external source, whether scraped or via a public API.
  
  ✓ Data provided must go at least a level deep, generally by showing the user a list of available data and then being able to drill into a specific item.

#### What does my gem do and how does it look? :clapper:

As you know the name of my gem is Broadway Now and it provides a list of the 20 most popular shows currently playing in New York City. Specifically it includes Broadway and Off-Broadway shows (both musicals and plays.) Popularity of the shows is determined by www.Broadway.com. Once you find a show that you like, you can select it by number to get additional information such as: running time, intermission, theater, ticket prices, and a blurb about the show. You can find the Broadway Now gem in it’s [Github Repository]( ) or in [RubyGems.]( https://rubygems.org/gems/broadway_now ) 

<iframe width="100%" height="425" src="https://www.youtube.com/embed/Edv71AV-DGM" frameborder="0" allowfullscreen></iframe>

#### Process mini summary :chart_with_upwards_trend:

This was the first coding project that I completed on my own, well with training wheels actually. :relaxed: Regardless I am proud of myself for finishing a working version of the gem. The more I got done the more I wanted to include on it. I kept having Ideas about what new features to add next. I will continue to work on the new features in tandem with my coursework. 

The hardest part for me was to start with a blank page and no direction. I spent hours researching how I wanted to go about starting this project and I ended up tackling the easiest task first, which ended up being the making a blog for this post. Then I found the [page](http://www.broadway.com/) that I wanted to scrape and I played around with the selectors I knew I would need. I then used my basic pseudo code to make a rough outline of all the tasks I would need to complete.

I used bundler to create the scaffolding for my project as well as to release the gem. The scaffolding got a bit confusing with the executable and environment files being set up differently than in previous projects, however Avi’s CLI Walkthrough lecture does an excellent job of explaining this set up and what specifically should go where and why.

>##### Things I didn’t know when I started this project :bulb:
>1. Use underscore instead of dashes to separate gem name when using `$ gem bundle <name>` otherwise you generate scaffolding with a funky structure.
>2. We are no longer using a file called run or a file called environment. Your executable file is named after your cli gem name and located in bin, and your primary file (aka environment file) in lib should also have the name of the cli gem. [or thats what I understood at least]
>3. Runtime dependencies are those your gem needs to work. They are added in the gemspec file like so: `spec.add_dependency “nokogiri”`
>4.  Development dependencies are those needed during development of your gem. They are added in the gemspec file by: `spec.add_development_dependency “pry”`
>5.  The gemspec file defines what is in the gem, author, version, dependencies, license, description etc.

#### Biggest challenge :hammer:

The **biggest challenge** for me was the publishing of my gem. Some setting was funky and when I tried to publish the action didnt finish and aborted half-way through. 


Errors:


`While executing gem ... (Gem::CommandLineError)
    Too many gem names`

`Failed to load /Users/lauracorrea/.gemrc because it doesn't contain valid YAML hash
Pushing gem to https://rubygems.org...
There was a problem saving your gem: Home does not appear to be a valid URL`

`While executing gem ... (Gem::Package::FormatError)
    No such file or directory @ rb_sysopen - broadway_now-0.1.1.gem`


I eventually changed the gemspec homepage, and fiddled with various other settings until I was able to push my gem. Unfortunately I have not been able to call it properly. I expect to have my code review next week and I will update below on how I manage to resolve this issue, so come back soon for the mystery solution!

##### Resources
- [Build a Jekyll blog with Jekyll Now](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/)
- [Broadway.com](http://www.broadway.com/)
- [Build a gem guide](https://quickleft.com/blog/engineering-lunch-series-step-by-step-guide-to-building-your-first-ruby-gem/)
- [Ruby gems: Make a gem](http://guides.rubygems.org/make-your-own-gem/)
- [Bundler](http://bundler.io/v1.11/bundle_gem.html)
- [Ruby gems: Commands reference](http://guides.rubygems.org/command-reference/)
- [Ruby gems: Publish a gem](http://guides.rubygems.org/publishing/)
- [Workflow Review: Make a gem](http://lcorr8.github.io/Workflow-review-worksheet-cli-gem/)

##### Troubleshooting gem publishing resources
- [Too many gem names error](https://fleetingdev.wordpress.com/2015/03/21/how-to-fix-the-%C2%93too-many-gem-names%C2%94-error-when-running-gem-build/)
- [Specification class reference](http://guides.rubygems.org/specification-reference/)
- [Rubygems is not allowed by gemspec error](http://bparanj.blogspot.com/2015/06/error-httpsrubygemsorg-is-not-allowed.html)









