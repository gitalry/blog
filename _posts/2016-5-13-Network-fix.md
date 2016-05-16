---
layout: post
title: The system network services are not compatible 
---
It so happens that I'll start learning Android in the next few days so i headed over to developer dot android and downloaded the android installed it on my 64bit laptop running Ubuntu 14.04  then boom!
..
..
My machine goes off line, no WiFi and cannot connect to the Internet, so i figured hey, why not try wired LAN will solve the problem. Surprise...it doesn't.
Instead it throws me this message "The system network services are not compatible with this version" - Ubuntu 14.04...blah blah.
So what next?
GIYF, Google throws me a million results, long story short, here's what worked for me.

1. Borrow a computer from a friend
2. Go to the below mentioned address.

http://archive.ubuntu.com/ubuntu/pool/main/libn/libnl3/)

3. What you need is these packages

| Packages |
| ------------- |
| libnl-3-200_3.2.21-1_amd64.deb |
| libnl-route-3-200_3.2.21-1_amd64.deb | 
| libnl-genl-3-200_3.2.21-1_amd64.deb |

The above is for 64bit OS, if happen to be running  32bit then use the i386.deb

( please check your OS whether its  32bit or 64bit)

4. Once you've downloaded them,copy them to your USB stick.

5. Put them in a folder call it packages then copy it to your desktop.

6. Open your terminal and navigate into the folder. 
To navigate use cd(Change Directory) eg cd Desktop/packages/

Once you're in it type(at the end of each line, press enter)



| Commands |
| ------------- |
| sudo dpkg -i libnl-3-200_3.2.21-1_amd64.deb |
| sudo dpkg -i libnl-route-3-200_3.2.21-1_amd64.deb | 
| sudo dpkg -i libnl-genl-3-200_3.2.21-1_amd64.deb |



Restart the system, tadaa...

+P.S: Am not saying the Android Studio brought this but hey..... crazy stuff has been known to happen randomly.
