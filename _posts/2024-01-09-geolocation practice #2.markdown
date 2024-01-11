---
layout: post
title:  geolocation practice #2
date:   2024-01-09 13:32:20 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: post-6.jpg # Add image post (optional)
tags: [Blog, trying stuff out]
author: # Add name author (optional)
---
I'm going to try another walkthrough of one of the geolocation challenges kindly provided by Sofia Santos on her [website](https://gralhix.com/list-of-osint-exercises/)

Here is the original problem: 
![original problem]({{site.baseurl}}/assets/img/osint challenge 2/challenge.png)

We want to find the name of the train station and the name and height of the tallest structure seen in the photo. Looking at the photo itself, there are a couple clues to the location:
1. English-speaking country
2. Looks like it's summer based on people's clothing
3. There are 5 buildings and one spire-looking-thing in the background (and maybe one more peeking out on the right hand side?)

At first glance, just based on the traincars, this doesn't look like anywhere in the U.S. The buildings also don't really look like anywhere in the U.K. So maybe Australia or New Zealand? 

Let's do a reverse google image search to take a look:
<img src="{{site.baseurl}}/assets/img/osint challenge 2/google reverse.png" width="80%">

Great! This is the Flinders Street railway station in Melbourne, Australia. Easy-peasy. 

Since the original photo is a bit blurry, I checked out a higher resolution photo of this same location here:
<img src="{{site.baseurl}}/assets/img/osint challenge 2/google reverse2.png" width="80%">
Where I found this (thanks Janice S)
<img src="{{site.baseurl}}/assets/img/osint challenge 2/high res photo.png" width="80%">

So we have a white spire, the HWT building, IBM building, and a blue building that all look pretty tall. 

Let's get to Australia: <img src="{{site.baseurl}}/assets/img/osint challenge 2/australia.png" width="80%">

Zooming into Melbourne: <img src="{{site.baseurl}}/assets/img/osint challenge 2/melbourne.png" width="80%">

Using streeview, I can plop down onto the platform of this train station to take a look:
<img src="{{site.baseurl}}/assets/img/osint challenge 2/photosphere1.png" width="80%">
<img src="{{site.baseurl}}/assets/img/osint challenge 2/panorama from platform.png" width="80%">

Looks like those are our buildings in the background and it seems like they're across the river, not across the street closest to us. 

To doublecheck, we can plop down at a second viewpoint: <img src="{{site.baseurl}}/assets/img/osint challenge 2/viewpoint 2.png" width="80%">

And yep, those are our buildings: <img src="{{site.baseurl}}/assets/img/osint challenge 2/viewpoint from water.png" width="80%">

Now, this part got a little tricky, since some structures are behind and some in front of other buildings. For instance, you can't see the white spire in that viewpoint so it's probably behind the other buildings. 

If we look top-down: <img src="{{site.baseurl}}/assets/img/osint challenge 2/buildings.png" width="80%">
Here are our structures of interest. Left to right, we have tan round theater building (too short to be seen in the original photo), right behind it is the white spire of the Arts Center. Next to the theater, we have the white Quay West Suites, then the two hexagonal copper-colored buildings (one of which is labeled IBM Australia), and then the tan Langham hotel in front. Lastly, the blue building seems to be further behind these ones but let's check the heights of these first. 

A quick google of the arts center spire gives us a wikipedia article with the height: 162 m (531 ft). Pretty tall. 
The IBM and HWT buildings are side by side and the IBM building seems taller from the photo. A quick search gives us a website with the height of various skyscrapers: <img src="{{site.baseurl}}/assets/img/osint challenge 2/ibm building height.png" width="80%">
Ok, so the spire is taller. The Langham and Quay West Suites are definitely shorter, so the last one to check is that blue building. 

It's in the background of the IBM building, so must be a block or so behind it. Clicking around the map and checking out streetview along that major roadway, I found this building: <img src="{{site.baseurl}}/assets/img/osint challenge 2/another building.png" width="80%">

Scrolling through the available photos, it looks like our building (blue glass with balconies, with some red posters): <img src="{{site.baseurl}}/assets/img/osint challenge 2/verify building.png" width="80%">
A quick google search for FOCUS apartments by Central Equity in Melbourne gives us the height: 545 ft. This building is taller than the spire so we have our answer! 

> Thanks to Sofia for a fun exercise and the video walkthrough to check the answer! 
