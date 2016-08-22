---
layout: post
title:  "Conclusion Google Summer of Code 2016"
date:   2016-08-19 8:57:51 -0400
categories: GSoC2016 Final_report
---


**SmartInfo project with Debian**
![alt text](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-icon-192.png "Gsoc2016")

**1. Me**

Before getting into the thick of my project, let me present myself: <br>
I am Olivier Grégoire (Gasuleg), and I study IT engineering at École de Technologie supérieure in Montreal. <br>
I am a technician in electronics, and I began object-oriented programming just last year. <br>
I applied to GSoC because I loved the concept of the project that I would work on and I really wanted to be part of it. I also wanted to discover the word of the free software.

**2. My Project**

During this GSoC, I worked on the <a href="https://ring.cx/"> Ring </a> project.

*"Ring is a free software for communication that allows its users to make audio or video calls, in pairs or groups, and to send messages, safely and freely, in confidence.*

*Savoir-faire Linux and a community of contributors worldwide develop Ring. It is available on GNU/Linux, Windows, Mac OSX and Android. It can be associated with a conventional phone service or integrated with any connected object.*

*Under this very easy to use software, there is a combination of technologies and innovations opening all kinds of perspectives to its users and developers.*

*Ring is a free software whose code is open. Therefore, it is not the software that controls you.*

*With Ring, you take control of your communication!*

*Ring is an open source software under the GPL v3 license. Everyone can verify the codes and propose new ones to improve the software's performace. It is a guarantee of transparency and freedom for everyone!"* <br>
Source:  <a href="https://ring.cx/en/about/practical">ring.cx </a>


The problem is about the typical user of Ring, the one who don't use the terminal to launch Ring. He has no information about what has happened in the system. My goal is to create a tool that display statistics of Ring.

**3. Quick Explanation of What My Program Can Do**

**The Code** <br>

Here are the links to the code I was working on all throughout the Google Summer of Code (You can see what I have done after the GSoC by clicking on the newest patchs):


Patch | Status
:--- | :---
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/4315/44">Daemon </a> | Merged
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/4388/30">Lib Ring Client (LRC) </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/4384/37">Gnome client </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/4234/2">Remove unused code </a>&nbsp; | Merged

<br>
**What Can Be Displayed?** <br>
This is the final list of information I can display and some ideas on what information we could display in the future:

Information &nbsp; &nbsp;| Details | Done?
:--- | :--- | :---
Call ID | The identification number of the call | Yes
Resolution | Local and remote | Yes
Framerate | Local and remote | Yes
Codec | Audio and video in local and remote &nbsp; &nbsp;| Yes
Bandwidth | Download and upload | No
Performance use | CPU, GPU, RAM | No
Security level | In SIP call | No
Connection time | | No
Packets lost | | No

<br>
To launch it you need to right click on the call and click on "Show advanced information".<br>
![alt text](https://raw.githubusercontent.com/Gasuleg/gasuleg.github.io/master/_includes/smartInfo.png "SmartInfo")<br>
To stop it, same thing: right click on the call and click on "Hide advanced information".<br>

**4. More Details About My Project**


My program needs to retrieve information from the daemon (LibRing) and then display it in gnome client. So, I needed to create a patch for the daemon, the D-Bus layer (in the daemon patch), LibRingClient and the GNU/Linux (Gnome) client. <br>

This is what the architecture of the project looks like. <br>
![alt text](https://raw.githubusercontent.com/Gasuleg/gasuleg.github.io/master/_includes/organisation.jpg "Ring organisation") <br>
source:<a href="https://ring.cx/en/about/technical"> ring.cx </a>

And this is how I implemented my project.<br>
![alt text](https://raw.githubusercontent.com/Gasuleg/gasuleg.github.io/master/_includes/globalSchema.png "My project") <br>


**5. Future of the Project**

- Add background on the gnome client <br>
- Implement the API smartInfoHub in all the other clients <br>
- Gather more information, such as bandwidth, resource consumption, security level, connection time, number of packets lost and anything else that could be deemed interesting<br>
- Display information for every participant in a conference call. I began to implement it for the daemon on <a href="https://gerrit-ring.savoirfairelinux.com/#/c/4315/25"> patch set 25 </a>.

**Weekly report link**

- <a href="https://lists.debian.org/debian-outreach/2016/06/msg00006.html"> Week 1 & 2</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/06/msg00026.html"> Week 3</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/06/msg00045.html"> Week 4</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/06/msg00068.html"> Week 5</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/07/msg00006.html"> Week 6</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/07/msg00021.html"> Week 7</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/07/msg00046.html"> Week 8</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/07/msg00064.html"> Week 9</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/08/msg00005.html"> Week 10</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/08/msg00011.html"> Week 11</a><br>
- <a href="https://lists.debian.org/debian-outreach/2016/08/msg00038.html"> Week 12</a><br>


**Thanks**

I would like to thank the following:<br>
- The <a href="https://summerofcode.withgoogle.com">Google Summer of Code</a> organisation, for this wonderful experience. <br>
- <a href="https://wiki.debian.org/SummerOfCode2016">Debian</a>, for accepting my project proposal and letting me embark on this fantastic adventure. <br>
- My mentor, <a href="https://github.com/yomgui1">Mr Guillaume Roguez</a>, and all his team, for being there to help me.
