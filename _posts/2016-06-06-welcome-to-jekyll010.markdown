---
layout: post
title:  "Sixth week: and the framerates appear...."
date:   2016-06-29 12:57:51 -0400
categories: weekly report
---
<p>Last week, I worked on link the D_BUS with the client and implement MAP on my callback smartInfo to push all my information in only one parameter. </p>
--------------------- <br>
<p>This week I wanted to display my first real information in my client. I choose to begin with the frame rate to help another person in Savoir Faire Linux who work on the encoding and decoding of the video.
So I worked on the video part of the daemon trying to understand how the daemon sends frames to LRC. All the frames are decoded in the same place so I just pull the number of frames per second for the local and remote video and put it on my callback smartInfo.</p>

--------------------- <br>

<p>Next week, I will change my architecture a little bit. Ring can handle several calls with different information and my implementation don't take care of this. I need to search and implement a new architecture to link my callback with the call.
