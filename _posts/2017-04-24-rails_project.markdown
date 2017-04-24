---
layout: post
title:  "Rails Project"
date:   2017-04-24 14:59:37 +0000
---


Wow, it's been a little while since I wrote a blog! I've been very busy on Learn.co, slowly but hopefully methodically working through the Ruby on Rails segment in order to get...here! To my final project blog post!

This project helped solidify a *lot* of Rails concepts for me. Not only did it help me to really wrap my head around routing, but also helped me to really appreciate the cornucopia of helper methods that come with Rails. A quick Google search with the desired result often led me to a new built-in method that I never would have known existed otherwise (A good example here is `distance_of_time_in_words(x_time, y_time)` which of *course* should exist, but perhaps I wouldn't have assumed it was there). I can't imagine how many more there are.

As predicted by the good folks over at Learn.co, I came to love and hate devise. It was great for rolling out the sign in/edit user/sign out/delete user system, but once it came time to customize the flow of things, I was really kicking myself. Luckily, a big portion of the internet also had this problem, and had posted most of their relevant findings. Through this, as well as the Devise docs on GitHub, I was able to learn some new things about Devise that I didn't know were previously possible with it, as well as wrap my head around what it's really doing behind the scenes.

One thing that I really came to realize while building this is the true value of thinking through a site map before building it! Obviously in a production environment one would be working with a designer or client, and would have that site map described to them already. But if I were to do something like this again, with all of the features and pages/look/feel already in mind, I would have set up my stylesheets completely differently, as I think they are currently a huge mess.

In the future, I'd like to update this app with more sort-ability, notifications for users, and more types of voting (A user can currently submit aa vote on an expired dilemma. I struggled with this because their input *is* still valid, and maybe fun for the community to see, but also not really relevant for the OP anymore. I'd like to think this through and figure out the best way to handle it.
