---
layout: post
title :  How to solve “Unable to run mksdcard SDK tool” when installing Android Studio
categories : [linux]
---
I was installing Android Studio on a 64-bit ubuntu 14.04 when I ran to the above error. I tried all tricks i knew (I got the JRE and JDK pre-requisites installed, 
unpacked the Android Studio installation, and from its "bin" directory issued "sh studio.sh" to complete the installation.) but failed. Luckily one user on
 stack overflow ran to the same problem and managed to get if fixed. 
Apparently unlike my ubuntu that didnt holla back as to what the cause is, this stack overflow user was on fedora and it "suggested that 32-bit libraries might be needed."
 The answers from the community had identified the libraries and amma shared them too, they might come in handy next time.
So to cut the long story short, installing the below libraries will sort out the issue.
Open your terminal and paste the below command, run it.

|-------------|
| sudo apt-get install lib32z1 lib32ncurses5 lib32bz2-1.0 lib32stdc++6 |
|-------------|


Then retry installing android studio again
