# Answer Me With Mr B - Website
Welcome! Did you know, Physics is true ya!

Here we have a Work In Progree website for the youtube channel [Answer Me With Mr B](https://www.youtube.com/channel/UCv7XjzuzmAKm458IqFehCPQ).

If you wish to help out, view the [Contributing instructions](#contributing).
# Contributing
Glad you're willing to help out!

Have a look at the links below to begin contributing.

New to GitHub? Have a look at this link to see how it all works.
- [How to Github](#how-to-github)

## How to Github

So, you're new to GitHub, eh? Welcome! Github is a platform in which programmers from all over the world share there code to be enjoyed by the masses, for free! Here, we use it in order for many people to collaborate together to manage the AMWMB website.

Github can be very confusing when you first start. If you can manage a quick paced lesson, check out The Coding Train's tutorial [Git and GitHub for Poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV) to get started. Video 1.1 is a useful introduction to GitHub, but video 1.3 will help you out the most here.

All right, you're good to go! If you're looking to start out small, have a look in the [Formatting](#formatting) section below, in order to see how we structure the files to make the magic happen.

Good luck, and happy coding!

P.s. if you're looking to improve your Open Source skills, and it's coming up to October, why not check out [Hacktoberfest](https://hacktoberfest.digitalocean.com/). Running throughout the whole of October, if you complete 4 pull requests, you can earn a nifty t-shirt, shipped all the way from San Francisco, for free!

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
