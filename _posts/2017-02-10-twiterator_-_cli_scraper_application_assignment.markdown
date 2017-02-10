---
layout: post
title:  "TWITERATOR - CLI Scraper Application Assignment"
date:   2017-02-10 17:23:51 +0000
---


Genuine excitement is the only way I can think to start this post. YES! After 2-3 days of some pretty hardcore tinkering and brain-ing, I was able to not only create a CLI scraper app, but also get it running locally as *well* as turn it into a published gem! **Twiterator** is finished (enough). I'm very proud of my first attempt at all of this, and I'm excited to write a bit about it. This post will include my favorite parts of the coding process as well as the biggest humps I overcame.

Repositories:
The majority of commits are on github at [this repository](https://github.com/gloverab/cli-data-gem-assessment-v-000), which I was stupidly working in after opening the lesson of of Learn.co.
After switching to a new project locally, I made a newer, cleaner repository [here](https://github.com/gloverab/twiterator) which contains the most recent updates. It may be wise to figure out how to merge these two.

Let's start with the basics. This app works off of three main classes: `User`, `Tweet`, and `Reply`. `User` scrapes and handles anything necessary on the user's page, including their amount of followers, amount of followees, user name, display name, and of course their tweets. It also stores any tweet it displays by calling the `get_tweet` method, and creating a new instance of `Tweet`.

`Tweet` is pretty simple! This class has a bunch of simple methods for recalling the data of the tweet, which is all stored in its #doc. The most interesting thing that happens here is the #set_replies method, which shovels a bunch of replies into the @replies array that this class initializes with. (Side note here: Twitter only allows an outside program to access 15 replies without diving into their API, so sadly that's the most we can get without the program breaking). To avoid any accidents, `set_replies` takes a look at the number of replies that a given tweet has and compares it against 15. If there are less than 15 replies, the program knows to only display whatever amount their are. If there are more, it knows to cap itself at 15. Either way, for however many replies are appropriate, `set_replies` creates new instances of `Reply`, and shovels those instances into the parent tweet's `self.replies`.

Let's get going into what I believe is the coolest feature of this program, which is its ability to search for twitter users if someone puts in an invalid handle. For instance, if someone types in "jtimberlake" or "@jtimberlake," Twiterator will recognize that as a twitter handle and go directly to Justin Timberlake's user page. However, if someone types in "Justin Timberlake," instead of just saying "Sorry, I don't know who that is," Twiterator will plug those words into twitter's search url, and scrape the first few replies from that page (ex. https://twitter.com/search?f=users&q=justin%20timberlake&src=typd). This is achieved by routing the user's input through a class `Verification` before doing anything else.

`Verification` initializes with a user name, and has only one method: `verify`, which users OpenURI command `rescue` to check whether or not its currently reading off of a 404 page. If it IS, the user is not verified, and we jump up to the search described above. All in all there *may* be a better way to achieve this than a whole seperate class, but I didn't want to overcomplicate the CLI Interface method, or bungle up `User`.

Once my app was working fairly well, I decided it was time to take the plunge and get it working locally, freeing myself of the training wheels that inherently come with working in the Learn IDE. I was able to install homebrew and install navigate RVM, ipso facto updating my computer's Ruby version to 2.3.3. From there I fumbled my way through turning my little program into a gem, and after a couple attemps, it worked! Now you, or anyone else with an updated version of Ruby, should be able to type 'gem install twiterator' into their Terminal and download my little gem.

All in all, this was an incredibly fulfilling assignment, and the first time that I genuinely felt like I could yield ruby as a powerful weapon in my arsenal. I ended up using almost everything I learned over the past month or so, and feeling really good about the direction that my coding is headed.
