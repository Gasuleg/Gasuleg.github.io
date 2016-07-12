---
layout: post
title:  "Seventh week: create a new architecture and send a lot of information"
date:   2016-06-29 12:57:51 -0400
categories: weekly report
---

At the begin of this week, I thought my architecture needed to be closer to the call . The goal was to create one class per call to save the different information. With this method, I only need to call the instance who I am interested and I can easly pull the information. <br>  So, I began to rewrite my architecture on the daemon to create an instance of my class link directly with the callID. <br>
After implementing it, I was really disappointed. This class was hardly to call from the upper software layers. Indeed, I didn't know what is the current call display on my client. <br>
I change my mind and I rewrite the architecture again. I observed the information I want to pull (frame rate, bandwidth, resolution...) and they are all generating in my daemon. Therefore, it will update every time something change in the client. So, I just need to catch it and send it to the upper software layers. My new architecture is simply a singleton because I just need one instance and I need to pull it from everywhere in my program. <br>

<br>Beyond that, I wanted to pull some information about the video (frame rate, resolution, codec for the local and remote computer). So, I looked to understand how the frame generate work. Now I can pull: <br>
-Local and remote video codec <br>
-Local and remote frame rate <br>
-Remote audio codec<br>
-Remote resolution<br>
-CallID<br>


--------------------- <br>

Next week, I will begin with working on creating an API on the client library. After that, I will continue to retrieve other information.
