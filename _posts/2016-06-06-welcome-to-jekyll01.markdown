---
layout: post
title:  "Fifth week at GSoC: push information from the daemon!"
date:   2016-06-29 12:57:51 -0400
categories: weekly report
---
<p>Last week I worked to create a window for the gnome client to display information. </p>
--------------------- <br>
<p>This week I worked on linking the D-BUS with the gnome client.<br>
To do that I needed to modify the LRC. <br>
-Create a QT slot to catch the signal from the D-BUS <br>
-Create a signal connect with a lambda function on the client </p>
<p> Unfortunately, I can only push a single variable at the time. So, I chose to use MAP to contain all my information. After changing this type in the daemon, D-Bus, LRC and the gnome client, everything finally work! </p>
