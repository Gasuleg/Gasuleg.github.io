---
layout: post
title:  "Conclusion Google Summer of Code 2017 with GNU"
date:   2017-08-19 8:57:51 -0400
categories: GSoC2017 Final_report
---



![alt text](https://developers.google.com/open-source/gsoc/resources/downloads/GSoC-icon-192.png "GSoC")
![alt text](https://upload.wikimedia.org/wikipedia/commons/thumb/8/83/The_GNU_logo.png/220px-The_GNU_logo.png "GNU")
![alt text](https://ring.cx/profiles/tatooine/themes/naboo/images/ring-bomor/tagline/logo-ring-tagline-EN-couleur.svg "Ring"){:height="100px"}<br>
## GNU Ring project with GNU organisation

# 1. Me

Before getting into the thick of my project, let me present myself: <br>
I am Olivier Grégoire (Gasuleg), and I study IT engineering at École de Technologie Supérieure in Montreal. <br>
I am a technician in electronics, and I study now computing sciences. <br>
I applied to GSoC because I love the concept of the project that I worked on and I really wanted to be part of it.

# 2. My Project

During this GSoC, I worked on the <a href="https://ring.cx/"> GNU Ring </a> project. <br>
<strong>What is ring?</strong><br>
* A telephone: a simple tool to connect, communicate and share.
* A teleconferencing tool: easily join calls to create conferences with multiple participants.
* A media sharing tool: Ring supports a variety of video input options, including mutliple cameras and image and video files, and the selection of audio inputs and outputs; all this is supported by multiple high quality audio and video codecs.
* A messenger: send text messeges during calls or out of calls (as long as your peer is connected).
* A building block for your IoT project: re-use the universal communications technology of Ring with its portable library on your system of choice. <br>
<a href="https://ring.cx/en/about/practical">-- <cite>ring.cx</cite> </a>

<strong>What I need to do?</strong><br>

This project is, at the moment, unstable due to a lack of automated tests. Only a part of the code is tested. I need to improve this. <br>
To do that, I need to:
  * Research and test automation strategies that integrate the compilation system and Jenkins verification like the SIP tests
  * Implement some unit tests to check the components <br>

See more in <a href="https://github.com/Gasuleg/proposal-GNU/blob/master/proposalGNU.pdf">my proposal</a>!

# 3. The Code

**Links to my work** <br>

Here are the links to the code I was working on all throughout the Google Summer of Code:


Patch | Status
:--- | :---
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7167/">Black box testing sip </a> | Merged
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7677/8">New unit test: smartools </a> | Merged
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7679/8">New unit test:account_factory </a> | Merged
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7680/8">New unit test: util classes </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7681/7">New unit test: archiver, conference, preferences</a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7682/7">New unit test: dring, threadloop </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7799/3">Documentation </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7311/">Refactoring + video_input unit test</a>| Abandoned

{:.mbtablestyle}
<br>
**How to use the code?**<br>
Follow the instructions to <a href="https://tuleap.ring.cx/plugins/mediawiki/wiki/ring/index.php/Build_Instructions">build the daemon</a> and instead of doing "make", do "make check". You will see something composed of:<br>
* Test automation strategies<br>
![alt text](https://github.com/Gasuleg/gasuleg.github.io/blob/master/_includes/sipTest.png?raw=true "test SIP")<br>
* Unit test
![alt text](https://github.com/Gasuleg/gasuleg.github.io/blob/master/_includes/unitTest.png?raw=true "unit test")<br>

**Some explanations of the code**<br>
The tests are based on <a href="http://cppunit.sourceforge.net/doc/cvs/index.html">CPPunit framework</a>.<br>
I created some Black box testing to do some calls using SIP protocol. To do that, I created scenarios using <a href="http://sipp.sourceforge.net/doc/reference.html">SIPp</a> . <br>
I also create a lot of unit tests.<br>

**Difficulties encountered**<br>
My project was a little bit difficult to setup because I never touch autotools before that.<br>
The sip tests were not really difficult to create. <a href="http://sipp.sourceforge.net/doc/reference.html">SIPp</a> is really easy to use.<br>
The unit test part was more tricky. It's really easier to do the tests before coding like the <a href="https://en.wikipedia.org/wiki/Test-driven_development">Test-driven_development</a> said. Here the code is already written and I need to test it. So, I needed to create tests based on the code and not what he needed to do. Also, I got some issues with classes who were really linked together so I couldn't make unit test with it.

# 4. What's next?

- Merge all the patchs
- Add <a href="https://https://gerrit-ring.savoirfairelinux.com/#/c/7799/cc.gnu.org/onlinedocs/gcc-4.7.3/gcc/Gcov.html">gcov </a>to know the code coverage
- Increase the code coverage


# 5. Thanks

I would like to thank the following:<br>
- The <a href="https://summerofcode.withgoogle.com">Google Summer of Code</a> organisation, for this wonderful experience. <br>
- <a href="https://www.gnu.org">GNU</a>, for accepting my project proposal and letting me embark on this fantastic adventure. <br>
- My mentor, <a href="https://github.com/yomgui1">Mr Guillaume Roguez</a>, and all the ring team, for being there to help me.
