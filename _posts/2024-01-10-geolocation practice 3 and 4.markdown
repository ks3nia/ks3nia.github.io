---
layout: post
title:  geolocation practice 3 and 4
date:   2024-01-10 13:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: post-6.jpg # Add image post (optional)
tags: [Blog, trying stuff out]
author: # Add name author (optional)
---
I'm going to try another walkthrough of a couple geolocation challenges by Sofia Santos ([website](https://gralhix.com/list-of-osint-exercises/).)This time I'll go through challenge #3 and 4 since 3 didn't end up taking too long. 

> Challenge #3

Here is the original problem: 
![original problem]({{site.baseurl}}/assets/img/osint challenge 3/challenge.png)
Our task is to find where this photo was taken (name and coordinates of the location). 

Looking at the photo, there are a couple clues:
1. Meeting between the president of Somalia and the Turkish president 
2. Meeting took place in 2017 in Turkey
3. The door behind them has some pretty distinctive features (red and gold, blue carpet, white columns, flags of each country on the sides)

First things first, let's do a reverse google image search: 
<img src="{{site.baseurl}}/assets/img/osint challenge 3/door.png" width="80%">

Looks like this particular door is a common backdrop for meetings with other world leaders. A quick search through these results and I find this article with the same door and caption that says the meeting took place in Ankara:

<img src="{{site.baseurl}}/assets/img/osint challenge 3/aljazeera article.png" width="80%">

Now to find the building in Ankara. I did a basic search for the president of Turkey and the Presidential Complex in Ankara seems like a good place to hold state visits:
<img src="{{site.baseurl}}/assets/img/osint challenge 3/residence.png" width="80%">
<img src="{{site.baseurl}}/assets/img/osint challenge 3/presidential complex.png" width="80%">

Switching over to googlemaps, there's no streetview for obvious reasons but lots of pictures to look through:

<img src="{{site.baseurl}}/assets/img/osint challenge 3/googlemaps.png" width="80%">

Ok back to that door. Looking through the photos on googlemaps, I find this (looks like a press briefing photo of some kind). We have white columns and the characteristic red and gold circles on the door itself. 

<img src="{{site.baseurl}}/assets/img/osint challenge 3/the door.png" width="80%">

However, looking at googlemaps, the building is symmetrical and there are two entrances...so which door is it? 

Again, scrolling through the photos, there are these two that show the different entrances:
<img src="{{site.baseurl}}/assets/img/osint challenge 3/front entrance.png" width="80%">
<img src="{{site.baseurl}}/assets/img/osint challenge 3/backdoor.png" width="80%">

Comparing the first viewpoint to the wikipedia, that looks like the front entrance that faces the reflecting pool and gardens. The second photo must be the back of the building which faces a plaza (makes sense to have press briefings there). Now looking at the doors, the first one does not have a red circle on the middle door, while the second one does! We've got our location. 

> Challenge #4

Here is the original problem: 
![original problem]({{site.baseurl}}/assets/img/osint challenge 4/challenge.png)
This is a photo of a resort located on an island. We need to find out the name of the resort, the coordinates of the island, and the cardinal direction the camera was facing when the photo was taken.

Reverse google image search gives us a couple clues (I realized after looking at other folks' walkthroughs that I went down a bit of a rabbit hole at first. I had different search results, not sure why).
<img src="{{site.baseurl}}/assets/img/osint challenge 4/reverse.png" width="80%">

This brings up lots of similar looking islands and one resort, Tailana Island. Clicking on their website, it looks promising:
<img src="{{site.baseurl}}/assets/img/osint challenge 4/resort.png" width="80%">
<img src="{{site.baseurl}}/assets/img/osint challenge 4/address.png" width="80%">

I then switched to google earth pro to take a closer look and put myself in the same angle as the camera but even though the island looks similar, the islands in the background didn't seem quite right:
<img src="{{site.baseurl}}/assets/img/osint challenge 4/not right island.png" width="80%">

Let's go back to our google search results and maybe narrow down the lens:
<img src="{{site.baseurl}}/assets/img/osint challenge 4/redo.png" width="80%">

This time, the Oan Resort pops up and it's exactly the same photo on their website: 
<img src="{{site.baseurl}}/assets/img/osint challenge 4/oan resort.png" width="80%">

Going back to google earth, this is the right island (you can see the two islands and a peak in the background across the water). And we are facing northwest!
<img src="{{site.baseurl}}/assets/img/osint challenge 4/rightisland.png" width="80%">


