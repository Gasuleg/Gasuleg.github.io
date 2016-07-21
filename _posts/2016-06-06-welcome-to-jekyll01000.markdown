---
layout: post
title:  "Height week: create an API on library ring client (LRC)"
date:   2016-07-21 12:57:51 -0400
categories: weekly report
---

At the beginning of the week, I didn't really use the LRC to communicate with my client.<br>
-The client calls an function in it to call my method who calls my program<br>
-The daemon sends his signal connect to an Qslot in LRC. After that, I just send another signal connect to a lambda function of the client

I have never programmed API before and I began to write some code without checking how doing that. I needed to extract all the information of my map<s,s> sending by the daemon to present all it in my API. After observing the code, I saw LRC follow the <a href="https://community.kde.org/Policies/Library_Code_Policy">kde library code policy</a>. So, I change my architecture to follow the same policies . Basically, I needed to create a public and private header by using the D-Pointer. My private header contains my slot who is connect with the daemon and all private variable. My public header contains a signal connect to lambda function who indicates to the client when some information change and he need to refresh it. This header contains obviously all the getters too.

I have now a functional API. <br>

---------------------

<br>Next week I will work on the gnome client to use this new API.
