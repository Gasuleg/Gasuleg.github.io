---
layout: post
title:  "Community bounding + 2 weeks at GSoC!"
date:   2016-06-06 12:57:51 -0400
categories: jekyll update
---
Welcome in my first and second report!
The community was really good, I talked with a lot of people from all around the world. All that projects are just awesome and I am happy to be part of this.
For this first week, I provided a list of all information I need to pull in my client (this list is subject to change a little bit):
-Call ID
-Resolution of the camera of all the people connect to the call
-Percentage of loosing frame
-Bandwidth (upload + download)
-Name of Codecs using on the conversation
-Time to contact the other person
-The security level
-Performance using by Ring (RAM + CPU)

I am trying to figure out how work the Ring project.
-Understand the external exchange by using Wireshark to catch some important packages.
-Understand the internal exchange between the daemon and clients on the D-Bus by using Bustle

I created my architecture program on the daemon and the D-Bus. [1] You can call the method launchSmartInfo(int x) from the D-Bus (by using D-Feet for example). That will call SmartInfo signal all x ms. This signal can only push an int for the moment, but he will push all the information we want on the clients.

I actually work on the Ring GNU Linux client. So I learn how work the QT and GTK+.

[1] https://github.com/Gasuleg/Smartlnfo-Ring (I will stop update this repository because I will push my code on the Gerrit draft of Savoir Faire Linux. It's more easy for my team to do some commentary on that platform and it's free software)
