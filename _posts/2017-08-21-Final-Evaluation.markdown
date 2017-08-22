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
  * Reimplement some unit tests to check the components of the SIP pur account.
  * Research and test automation strategies that integrate the compilation system and Jenkins verification.
  * Write more unit tests for the critical functions in order to increase the code coverage.


See more in <a href="https://github.com/Gasuleg/proposal-GNU/blob/master/proposalGNU.pdf">my proposal</a>!

# 3. What my code can do

**The Code** <br>

Here are the links to the code I was working on all throughout the Google Summer of Code:


Patch | Status
:--- | :---
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7167/">Black box testing sip </a> | Merged
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7710/1">Fix sip error </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7677/2">New unit test: smartools </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7679/2">New unit test:account_factory </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7680/2">New unit test: util classes </a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7681/2">New unit test: archiver, conference, preferences</a> | On Review
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7682/2">New unit test: dring, threadloop </a> | WIP
<a href="https://gerrit-ring.savoirfairelinux.com/#/c/7708/2">Refactoring + video_input unit test  </a>  <br><a href="https://gerrit-ring.savoirfairelinux.com/#/c/7311/">Base on this patch</a>| On Review
{:.mbtablestyle}

# 4. What's next?

- Add gcov to know the code coverage
- Increase the code coverage


# 5. Thanks

I would like to thank the following:<br>
- The <a href="https://summerofcode.withgoogle.com">Google Summer of Code</a> organisation, for this wonderful experience. <br>
- <a href="https://www.gnu.org">GNU</a>, for accepting my project proposal and letting me embark on this fantastic adventure. <br>
- My mentor, <a href="https://github.com/yomgui1">Mr Guillaume Roguez</a>, and all the ring team, for being there to help me.
