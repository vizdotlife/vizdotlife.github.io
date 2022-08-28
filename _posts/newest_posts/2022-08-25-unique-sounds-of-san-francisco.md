---
layout: post
title: Unique Sounds of San Francisco
description: 
date:   2022-08-25 15:01:35 +0300
image: '/images/posts/unique_sounds/fog-horns-chart-2.png'
include_flag: 'exclude_from_homepage'
num: 1
newest_tags:   [include]
tags:   [Data Viz,Sounds]
---

If you'd like to hop straight to listening to some of the sounds check out the podcast link below, however if you're interested in hearing more about how the project started please continue reading on.

![](/images/sounds/season-1-sounds-of-sanfrancisco.png)

[Listen to soundtracks here](https://open.spotify.com/show/42cRLn2YRwyLHiFRAHlSrw)

## In summary this project is about sounds and patterns
This project is primarly focused on recording unique sounds, extracting the raw data from .wav files, turning it to life with visuals, and looking at patterns.  

## It all started with a cable car ride
The first high quality sound recording I did was of a cable car ride from Ghiradelli Square to downtown Powell Street. 

![](/images/sounds/cable-car-ride-night.jpg)

A random Saturday night after spending time researching the best devices to record high quality sounds I decided to stop by a local guitar store right before they closed to purchase a Zoom recorder. I was super excited to try it out and within a few minutes of testing at home I headed off to record sounds around the city! 

![](/images/sounds/zoom-recorder.jpg)

Soon after a brisk walk from North Beach to Ghiradelli Square I hopped on a cable car and picked a front row seat. Given it was around 11pm at night and chilly, there were plenty of seats to pick from. I reached for the recording device out of a Trader Joe's bag, turned it on, and started recording shortly before the ride started. 

<iframe src="https://www.youtube.com/embed/B_cwgXwMzAk" width="320" height="180" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

As you might expect I did indeed get a few weird looks from people sitting around me for holding a foreign looking device in one hand and gripping a handle bar in the other hand. Over time it got easier to ignore peoples expressions, but it was one of the challenges throughout the entire project recording sounds.

## Ginormous file size!
Soon after getting home I transferred the sound wave file from the recording device to my Mac and I loaded the raw data into what's called a DataFrame using Python and Pandas. My computer crashed in the process! After booting up again I checked the file size and it was almost 200MB, which means there's a LOT of data! 

## Visualizing Sounds
After a few tries I was finally able to load the file into a dataframe to plot a visual representation of sounds during the cable car ride. 

![](/images/sounds/cable-car-ride.png)

Want to guess how many data points are collected in a 19 minute cable car ride visualized in the chart above?

After a little research I learned that 44,100 records are added per second in a 16 bit wave file. After some quick math it equates to over 50 million records in the dataset!

## This got me hooked
For many years professionally I worked and consumed a vast amount of data on a daily basis for analytics, however it was a new experience to generate data on my own. I was fascinated with this new experience and the limitless learnings that could come out of collecting and analyzing patterns of sounds.  

## Fog Horns on Golden Gate Bridge
![](/images/sounds/cable-car-ride.png) 

A next step in this project was to wake up super early on a foggy Saturday morning to record the fog horns on Golden Gate Bridge. 

Coming soon...

![](/images/sounds/fog-horns-chart-1.png)

## Thank you


