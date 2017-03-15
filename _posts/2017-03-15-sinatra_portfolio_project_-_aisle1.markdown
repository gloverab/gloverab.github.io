---
layout: post
title:  "Sinatra Portfolio Project - "Aisle1""
date:   2017-03-15 18:13:12 +0000
---


This was the first true web app I'd ever built, and I couldn't be more happy with what I've learned. I spent the better part of 3 days one this project, making sure things were working correctly and linked properly. I'm so jazzed about it that I honestly don't quite know where to begin, but I'll try.

First things first, the struggles. Before this project I had a bit of a difficult time truly understanding the associations in ActiveRecord. I understood basics like `x has_many y` or `y belongs_to x`, but struggled when y also belonged to many x's or had many z's. Luckily, I was able to hammer the information into myself and really understand the value of Join tables, as well as a little of the magic that goes into ActiveRecord itself.

The main purpose of this web app is to help users generate a list based on their recipes for a week. Weeks have many recipes, recipes belong to several different weeks, recipes have many ingredients, and ingredients have several different weeks. I also set myself up for the future by making sure ingredients `belong_to` a category. While that functionality isn't built out just yet, I'm excited to step back at what *is* completed while knowing that something even cooler is on the horizon.

All of this was built into a web interface using erb files. While doing some research for the project I came across an alternatve called HAML which I'd like to delve into in the future, but erb worked just great for now. I also highly recommend the erb-helper package to anyone using Atom, as it makes the tags much less of a hassle.

All in all, I really enjoyed creating this app and learning a bit about associations, while recalling a bunch of ruby that I hadn't used in the last couple of weeks. I was pleasantly surprised to find that I retained a lot more of it than I thought I would have. I'm looking forward to increasing the functionality and look of my application, and getting feedback from others.
