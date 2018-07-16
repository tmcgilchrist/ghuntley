---
title: closed captioning
---

Baking captions onto a video stream isn't accessible. Captions need to be embedded as text into the video so that text is readable by JAWS and other screen reader packages. There appears to be two ways to do this:

* [CEA-708/EIA-608](https://en.m.wikipedia.org/wiki/CEA-708) embedded in the video elementary stream as described in ATSC A/72 ([SEI user_data](https://software.intel.com/en-us/blogs/2014/08/18/how-to-add-closed-caption-messages-in-avc-and-mpeg2-streams))
* [CEA-708/EIA-608](https://en.m.wikipedia.org/wiki/CEA-708) transmitted via RTMP onCaptionInfo script/AMF0 tag

https://github.com/szatmary/libcaption/

# live streaming services
* https://help.twitch.tv/customer/portal/articles/2564215
* https://support.google.com/youtube/answer/3068031?hl=en

# research
* https://youtu.be/Dx-iqLD5b3I?t=7723

