---
layout: post
author: TheGreatK0rnholio
---

Goooooooood morning Viet- wait, this isn't a jungle! This is...the first installment of ***Upcoming Shit™***, a series of posts where I go over what I'm going to be working on. When will there be another? I have no idea, depends on how fast I can get the things I list here done, which might take a bit since I head back to work full-time next week. 

## Table of shitty contents
- [Table of shitty contents](#table-of-shitty-contents)
  - [The ShitDick Chronicles Episode I](#the-shitdick-chronicles-episode-i)
    - [When the SAME headers are sus](#when-the-same-headers-are-sus)
      - [Conclusion](#conclusion)

### [The ShitDick Chronicles Episode I](#the-shitdick-chronicles-ep1)

In the ShitDick news, I've just updated it to .NET 6 after it being developed on .NET Framework 4.7.2 for its entire existence up to this point. 

M$ didn't *really* pester me directly much, but what happened exactly is that I was about to finally code an actual dropper program for it (since ShitDick.C has audio files, images and other things like that it needs to extract somewhere to use in its payloads) and noticed the changes to C# and the lack of a straightforward way to make new projects use 4.7.2 in VS2022. Unlike previous versions, .NET Framework dev tools appear to not be included at all; only .NET 6.0 is included by default when installing the .NET development package, which really in VS2019 was all you needed to do unless you wanted to have compatibility with deprecated OS versions like XP. 

![vs screenshot1](https://i.ibb.co/smDkGZs/Screenshot-2022-03-08-113808.png)

The .NET Framework 4.7.2 version is still functional, but I've seen it being more finnicky on the latest stable version of Win 10, and haven't tested it on Win 11 because not even Microsoft could pay me enough to install that steaming pile of fried ballsack on my PC. But going forward it will mainly be developed for .NET 6 as it is better supported by Microsoft, *and* it means I could eventually do a rewrite of the code to be completely cross-platform and take advantage of the more open nature of .NET 6.0 so that I can also torment an Ubuntu VM with it to express my hatred towards what that distro has devolved into. 

ResonateII's core library, known as JLib, that was adapted for use in ShitDick.C had to be patched slightly because it originally called RNGCryptoServiceProvider, which was deprecated starting in .NET 6.0, instead of just calling RandomNumberGenerator.Create. As a result I also made some slight tweaks to the functions that contained things like `rngCsp.GetBytes(exampleArrayVar)` just a little bit so now they point to the new name I made for using the random number generator when I changed it to use the new proper way of doing things, and thus now it looks like `rng.GetBytes(anotherExample)`. I'm also creating more payloads taking advantage of the actual full functionality of JLib.

Lastly for the ShitDick updates, the original ResonateII file infection code, which the GAiA crew named the Omnivorous iNfection Engine, is being brought back for the destructive variant ShitDick.C! There's still a lot of work to be done on it to get it fully up and running, since as usual for any kind of programming, there's lots and lots of bug fixes that need to be made. I'll be recording a demo video of it running in my Win 10 VM once the next major version is ready, and that'll be on my YouTube channel as well as being linked to in a post here. 

#### [When the SAME headers are sus](#openendec-update)

I'm also continuing the work on OpenENDEC; as of the last GitHub commit a long fucking time ago, all current EAS event codes have been added to the encoder[^1], even the ones that are no longer used just because having options is nice if you're a hobbyist that wants to play around with it. Here's the array that contains them in my code just to show it:

![event codes](https://i.ibb.co/fMbKWsv/Screenshot-2022-03-08-120215.png)

Next up for the project is getting a stable version of the decoder part out. I was on hiatus from making OpenENDEC for a little while so that still hasn't gotten to a point where it's usable, especially since I kind of wanted to write that all from scratch just to see if I could do it but...well, the answer to that is no, I'm not that skilled with making applications for AFSK decoding yet. I just know enough to build on existing code for it. So on that one, I'll have to just take the L this time and go to my plan B - start a fork of a better open source decoder than I know how to make from scratch, and take some time to figure out maintaining and upgrading it much like what I did with the encoder. 

##### [Conclusion](#conclusion)

Well, that's all for this long-as-fuck post. Since this is one that puts together all the shit I want to talk about regarding multiple projects, these posts will probably be very long in the future as well but there will also be shorter, more focused posts about specific things. 

Wait, you're still reading all the way down here? I like your style. Wanna help me take over the galaxy?

---
{: data-content="footnotes"}

[^1]: Link to the mentioned commit here - https://github.com/TheGreatC0deholio/OpenENDEC/commit/84333bf41a0bbe4d2fe3f716d15bdd651ea9f8fa