---
layout: post
title:  "OO Ruby Programming and Everyday Conversation"
date:   2017-01-18 18:23:22 +0000
---

Think about a conversation, even just a mildly interesting one. What are its core components? We interact with all of them several times each day, but barely need to think about what's going into it. A conversation can be broken down into five key components before repeating portions of the process: Initializing, listening, thinking, speaking, and assessing. Let's compare these components with their OO counterparts.

First, we initialize conversation. Perhaps we wave. Perhaps we show up to a place where our contemporaries are (or vice versa). Maybe, just maybe, we're even initiating the conversation by speaking to a girl. The Ruby equivelent of this should be easy to identify: `def initialize`. However we initialize the conversation is up to circumstance, but it must be initialized in some way before progressing to the next step: Listening.

Okay, *mayyyybe* you're a teenage bro who can't be bothered to hear what his girlfriend is saying. But let's assume otherwise, and say that in order for you to have a conversation you must listen to what was previously said. In Ruby, we can equate this to setting arguments. We're waiting for those blanks to be filled by the speaker, so that we can move on to the next phase of conversation.

Thinking! This is crucial! Okay, *mayyyyyybe* you're a teenage girl whose family is definitely wrong, all the time, and you don't need to think of a response. Conversations may look like the following:
> Honey, you really shouldn't steal your father's car on a regular basis, blindfold yourself and drive it around town blasting Iggy Azalea.
> whatever.
Wow, that sure is one even-keeled mother! For the sake of Ruby-izing this interaction, let's say "whatever" is a default argument. Maybe it looks a little like `def advice(response="whatever")`. As this teenage girl learns to think over time, her response will have been thought upon methodically and hopefully generate something with a bit more wisdom. This would be like taking the advice, and operating on the response to return something more relevant, like "you're right I shouldn't have done that."

Then, we speak! We `puts`! This one is easy, and far less convoluted than the teenage girl example we struggled through together earlier.

Lastly, we assess. This is the equivelent of running our code back. Maybe even running "learn" on it and seeing if it passes the tests. It's not infrequent to have a conversation and think "oh man, I should have said [blank]!" Luckily, as we can go back and modify our code, we will likely have a similar conversation at some other point in our life, where we can learn from our previous mistakes and operate a bit differently.
