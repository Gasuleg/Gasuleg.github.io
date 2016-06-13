---
layout: post
title:  "Community bounding + 2 weeks at GSoC!"
date:   2016-06-06 12:57:51 -0400
categories: weekly report
---
<p>Welcome in my first and second report!<br/>
The community was really good, I talked with a lot of people from all around the world. All that projects are just awesome and I am happy to be part of this.<br/>
For this first week, I provided a list of all information I need to pull in my client (this list is subject to change a little bit):<br/>
-Call ID <br/>
-Resolution of the camera of all the people connect to the call<br/>
-Percentage of loosing frame<br/>
-Bandwidth (upload + download)<br/>
-Name of Codecs using on the conversation<br/>
-Time to contact the other person<br/>
-The security level<br/>
-Performance using by Ring (RAM + CPU)<br/></p>

<p>I am trying to figure out how work the Ring project.<br/>
-Understand the external exchange by using Wireshark to catch some important packages.<br/>
-Understand the internal exchange between the daemon and clients on the D-Bus by using Bustle<br/></p>

<p>I created my architecture program on the daemon and the D-Bus. [1] You can call the method launchSmartInfo(int x) from the D-Bus (by using D-Feet for example). That will call SmartInfo signal all x ms. This signal can only push an int for the moment, but he will push all the information we want on the clients.</p>

<p>I actually work on the Ring GNU Linux client. So I learn how work the QT and GTK+.</p>

<p>[1]<a href="https://github.com/Gasuleg/Smartlnfo-Ring">github/Gasuleg/Smartlnfo-Ring</a>: I will stop update this repository because I will push my code on the Gerrit draft of Savoir Faire Linux. It's more easy for my team to do some commentary on that platform and it's free software)</p>
