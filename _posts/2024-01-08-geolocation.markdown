---
layout: post
title: geolocation practice
date: 2024-01-08 13:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: post-6.jpg # Add image post (optional)
tags: [Blog, trying stuff out]
author: # Add name author (optional)
---

I decided to take a stab at some geolocation challenges kindly provided by Sofia Santos on her [website](https://gralhix.com/list-of-osint-exercises/)

Without further ado, let's dive in. 
Here is the original problem: 
![original problem]({{site.baseurl}}/assets/img/osint challenge 1/challenge details.png)
We want to find the coordinates of where this photo was taken. Now, assuming there's nothing tricky about the source image or the translated text itself, we can figure out a couple things right off the bat: 
1. This was taken in the city of Kiffa
2. It's translated from Arabic, so maybe that can give us a clue to narrow down the country
3. This was taken in the morning, on February 20th, 2013, posted in the afternoon
4. The person taking the photo is talking about "newcomers" or visitors to the city
5. There's a paved road, some one story buildings, and lots of trees. 

First things first, let's google Kiffa. Looks like a city in Mauritania in Northwest Africa:
<img src="{{site.baseurl}}/assets/img/osint challenge 1/kiffa google maps_zoomout.png" width="80%">

This looks like a pretty small city so let's zoom in some more: 
<img src="{{site.baseurl}}/assets/img/osint challenge 1/kiffa google maps.png" width="80%">
Arabic is the official language so seems like we're in the right place. 

Let's narrow it down. There are only a few major roads in Kiffa (marked in yellow) and unfortunately no streetview. If we zoom in further, most of them are not paved. For instance, if we zoom into this road:
<img src="{{site.baseurl}}/assets/img/osint challenge 1/kiffa google maps_zoom into road.png" width="80%">

It looks like only the four major ones have asphalt: <img src="{{site.baseurl}}/assets/img/osint challenge 1/paved roads.png" width="80%">
This photo was taken in the morning, so the sun is fairly low on the horizon and almost directly in the east. The person is likely located on a paved road which goes north-south, and is facing south. There are only three of those which narrows things down significantly!

We also have some trees in the background of the photo. This seems to be a very arid landscape but there are pockets of green in and around the city. Let's take a closer look. 
In the northwest corner, we have the road going north-south and a lake with some green around it but it's fairly sparse:
<img src="{{site.baseurl}}/assets/img/osint challenge 1/not enough trees.png" width="80%">
Probably not our location. 

The southern-most road crosses a river with a lot more green. Maybe that's our spot?
If we zoom in there <img src="{{site.baseurl}}/assets/img/osint challenge 1/kiffa google maps_zoominsouth.png" width="80%">
it looks promising: <img src="{{site.baseurl}}/assets/img/osint challenge 1/trees and hotel.png" width="80%">
There's even a hotel which might fit with our photographer talking about "newcomers". 

Since there's no streetview, I switched to GoogleEarth to verify the location. Here, I can rotate the whole map so that I'm facing south like the photographer: 
![kiffa googleearth]({{site.baseurl}}/assets/img/osint challenge 1/kiffa north south roads.png). Since this photo was taken in 2013, I can also play around with historical satelite images.

If I find and zoom into that same road with the trees and the river, I can see this: 
![kiffa googleearth]({{site.baseurl}}/assets/img/osint challenge 1/kiffa final loc.png)

If we zoom in even more and scroll through the time of day to look at shadows
![kiffa googleearth]({{site.baseurl}}/assets/img/osint challenge 1/kiffa final loc zoom.png)
we can see a paved road with low buildings a bit further away from the road, telephone poles along the side, large trees behind the building across the street, and trees in the near distance. Looks like the spot!

One final check, this image was taken 11/26/2010 so just to make sure all this still looked the same in 2013, we can look at the next time this place was imaged (7/19/2013) and verify the buildings and trees are still there:
![kiffa googleearth]({{site.baseurl}}/assets/img/osint challenge 1/kiffa final loc_verify date.png)

> Thanks to Sofia for a fun exercise and the video walkthrough! Hopefully the photographer isn't too weirded out by random people all over the world geolocating their 11-year-old twitter post :) 


