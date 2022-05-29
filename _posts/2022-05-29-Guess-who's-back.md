---
layout: post
author: TheGreatK0rnholio
---

Well, been a while since I updated this. Kept you waiting, huh? (had to do it). 

I've been extremely busy, with work and also starting IT/cybersecurity classes. But I do have some updates on projects.

## Table of Upcoming Shit™
- [Table of Upcoming Shit™](#table-of-upcoming-shit)
  - [New Android TV fuckery](#new-android-tv-fuckery)
    - [Sussy SAME Headers 2: Electric Boogaloo](#sussy-same-headers-2-electric-boogaloo)
      - [Conclusion](#conclusion)

### [New Android TV fuckery](#new-android-tv-fuckery)

Okay, so first some context: I recently got a smart TV running the Android TV OS as a gift. I've liked it so far but if the people in my family who had the idea to gift me this thought this means I wouldn't do some tinkering, they would be very wrong. 

One of the first things I noticed with it is that if you load APKs onto it, the Android core underneath the TV interface reveals itself a bit since you can actually install even regular tablet apps (just don't expect it to have great controls if it's designed for a touchscreen). I tested this with the DIRECTV Stream app since for some fucking reason, there's no official Android TV app for that service. Now, sure, I do have an old-ass Roku Express sitting in a box somewhere and I could just plug that in, but frankly that's too simple and logical for me. The solution has to be something that makes you question what the hell I'm doing with my life or else it's not a good solution. 

So I took to multiple forums to look into it, and found people have been using the Fire TV version on most Android-based smart TVs without much trouble. Grabbed the APK, shoved it onto my TV, and managed to install it. And yeah, it works. But there are a couple things that lowkey annoy me.

First of all, controls. Your average Android TV remote has different buttons and more of them than a Fire TV remote which is what this version was programmed for. This means that navigating the app is a lot less intuitive than it could be.

Second, it's not exactly properly optimized for this. Not sure how much I can really do about that but hey, that won't stop me from trying.

And third, the UI appears too large on mine a lot of the time; it doesn't properly adjust to the 720p resolution (yes, yes, I know, it's low-res by today's standards but it was a gift so I can't really complain), and I suspect it doesn't adjust that well to 1080p either since this APK was apparently pulled from a 4K Fire Stick, so it might be assuming anything it runs on is 4K unless some device-specific setting is changed.

So that being said, I'm now working on a modified version of the APK to configure it a little better for Android TV and hopefully fix the aforementioned issues. 

#### [Sussy SAME Headers 2: Electric Boogaloo](#sussy-same-headers-2)

And now, after that long ramble about Android TV, the OpenENDEC news!

Not a whole lot of changes, after all the encoder portion is pretty much complete since all event codes and everything have been added and it's passed testing; the only thing with it is the pending upgrade to Python 3. As for the decoder...

The decoder based on multimon-ng/dsame is still somewhat under development. It's ended up being kind of a bitch to get working together with the encoder fully, especially when it comes to automation. Plus I'm also working on packaging it all together so it's not a total pain in the ass to install. The Python 3 version of the encoder I mentioned is in the very early alpha stages of development since I have to do a bit of a code rewrite to make it compatible. The conversion tools out there have done a lot of the work luckily but there's still parts of it that are broken in the Python 3 version that produced, so there's plenty more debugging to do at this point.

##### [Conclusion](#conclusion)

Not a whole lot of big updates, I know, but I am working on all my projects a little bit whenever I get a chance to. As for the modded DIRECTV Stream APK, I won't be able to put any source code of it up here for the sake of avoiding legal issues (although for full disclosure, anyone can get it the same way I did by opening up the APK in Android Studio). I'm already pissing them off plenty by just modifying the app to work better, so here's a disclaimer about that just in case (covering my ass and all):

DIRECTV Stream, DIRECTV, AT&T TV, and all other related brands or services, are owned by DIRECTV LLC and AT&T Inc. TheGreatK0rnholio does not claim ownership of any of the above services and is not endorsed, sponsored, employed, or in any way supported by/affiliated with DIRECTV or AT&T and does not profit from any of these.