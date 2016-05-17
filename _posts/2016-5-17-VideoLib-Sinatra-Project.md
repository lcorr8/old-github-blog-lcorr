---
layout: post
title: VideoLib Sinatra Project!
---

I made VideoLib to keep track of the lecture videos I have seen for the topics that im covering in my [LV program](https://learn.co/with/lcorr8). We have access to this awesome video library from the 3 past rounds of Live Lectures Avi has recorded for his students. Each round covers all of the topics so there are multiple videos for each topic, but with different explanations and examples. However it is hard to keep track of which videos you have seen about each topic, so in an attempt to get more organized and to review more I made VideoLib.


#### Project Requirements :mag:

  ✓ Build an MVC Sinatra Application.
  
  ✓ Use ActiveRecord with Sinatra.
  
  ✓ Use Multiple Models.
  
  ✓ Use at least one has_many relationship
  
  ✓ Must have user accounts. The user that created the content should be the only person who can modify that content.
  
  ✓ Models must have validations to ensure that bad data isn't created.
  
  ✓ Any validation failures must be shown to user with an error message.


#### What does my gem do and how does it look? :clapper:

VideoLib allows you to make an account and to essentially make a video library. Your library is divided into sections, where each section will be a topic. For instance some default sections may be: git basics, ruby basics, ruby oo, sql, and so on. Each section holds video links with basic info and the option to embed videos. Once you watch a video you just mark it watched and you can keep track of which videos you have seen.

<iframe width="100%" height="315" src="https://www.youtube.com/embed/L3c1d1QOX_Y" frameborder="0" allowfullscreen></iframe>


#### Process mini summary :chart_with_upwards_trend:

This project was a lot of fun for me. I especially enjoyed writing routes and seeing something I wrote the logic for displayed nicely on a web browser. The models, and relationships were a little hard because at first I didn’t know if I wanted to have the most basic relationships or if I wanted to continue to add relationships. I ended up settling for a happy medium where users have many sections and many videos through sections. 

Writing RESTFUL routes ended up giving me more routes than I found useful for my app, namely the index. I inted made an index for videos you haven't seen yet because it seemed more useful when studying. The app only shows a user his or her content. Another fun part for me was writing specific error messages for each mistake a user can make, for instance trying to create a video that they already have in one of their sections. I might have actually gone a bit overboard with the error messages and redirects. I know that the error messages can be refactored into more vague error messages such as “not your content to modify” but I really liked the way the program tells you “hey this isn’t your video to delete”, specifically.

Probably will deploy after assessment, so my classmates have a better version to use.

#### Validations implemented :vertical_traffic_light:

- No empty fields for creating (section, videos, user) or for login fields
- No empty fields for editing section or videos
- Mandatory radio button selections upon creation and editing of videos
- Deny access to other student's info
- Don’t allow a section to be deleted if it has any videos in it
- Validation for a video that already exists for that user by video link (prevent duplicates)
- Validation for creation of a username that already exists (prevent duplicates)
- Validation for creation of a section that already exists for that user(prevent duplicates)
- Don’t allow any actions other than login, and signup unless logged in.


##### Things I didn’t know when I started this project :bulb:
1. Error message handling. If you have error information DON'T redirect! instead render.
2. Also probably not best practice to use error messages on your urls, this is what I did originally.


#### Biggest challenge :hammer:

My **biggest challenge** with this project was that I had to pause halfway through it and take a forced month study break to work. When I came back to my project I had these crazy bugs and I couldn’t remember why I had done certain things, so I had to in a sense start from the beginning and figure out why I had written very useless lines of code, and how to remove them without breaking everything else. This challenge offered a great opportunity to refactor and judge my work more objectively even though I didn’t remember the specifics of certain lectures and had to spend a lot of time going back to reference little things.

One of the things I seem to have missed from the lectures the first time around was the render vs redirect concept. I think I made the assumption during the lectures that redirecting was better than rendering and consequently only rendered once per each view in my code and redirected the rest of the times. In the Building Authentications in Sinatra (LV 2016) video Avi says “we render when the current request has the data we need. If we don’t need that data anymore we can redirect them along. But if we need the data that was instantiated and built during one request cycle, we must render right away.”


##### Resources
- [Require radio buttons](http://stackoverflow.com/questions/8287779/html5-how-to-use-the-required-attribute-with-a-radio-input-field)
- [Flash messages](https://github.com/vast/sinatra-redirect-with-flash)
- [Proper flash messages LV lecture](https://learn.co/tracks/full-stack-web-development/sinatra/activerecord/sinatra-playlister)
- Building Authentications in Sinatra (LV video lecture, 2016)
- [Learn Verified referral link $250 discount](https://learn.co/with/lcorr8)









