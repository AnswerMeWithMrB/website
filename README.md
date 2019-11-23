# Answer Me With Mr B - Website
Welcome! Did you know, Physics is true ya!

Here we have a Work In Progree website for the youtube channel [Answer Me With Mr B](https://www.youtube.com/channel/UCv7XjzuzmAKm458IqFehCPQ).

If you wish to help out, view the [Contributing instructions](#contributing).
# Contributing


## Formatting

### New Video
In the [videos](videos/) directory you will find 4 more directories:

- _National5Teaching
- _National5Music
- _HigherTeaching
- _HigherMusic

In each of these is a list of files, here is an example:

- 001-video-title.md
- 002-video-title.md
- 003-video-title.md
- 004-video-title.md
- index.md

If you wish to help by adding a new video, create a new video with the format below:

> ###-video-title.md

Then copy, paste and fill out the following text:

```
---
order: [Video number]
level: [Academic level]
title: [Video title]
videoId: [Video id]
layout: video
---

[Video description]
```

Here is what each of these means:

- order
  - This is the order that the video comes in the playlist
- level
  - This is the level that the video is aimed at (National 5 / Higher)
- title
  - This is the title that the video has on youtube (ignore number)
- videoId
  - This is the id that the video is given by youtube. You can find it in the url eg:
    - youtube.com/watch?v=[videoId]
- layout
  - This is the layout that tell the site how to display the page. Leave this alone when adding a new video.
    - This will be removed and placed in a default config location in a later version.
    
- [Video description]
  - The line of text below the --- should be the description from the video on youtube.
  
  
Once you have saved, you can submit your pull request and the video shall be live on the site in a few minutes!
