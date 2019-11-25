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

So, you're new to GitHub, eh? Welcome! Github is a platform in which programmers from all over the world share their code to be enjoyed by the masses, for free! Here, we use it in order for many people to collaborate together to manage the AMWMB website.

Github can be very confusing when you first start. If you can manage a quick paced lesson, check out The Coding Train's tutorial [Git and GitHub for Poets](https://www.youtube.com/playlist?list=PLRqwX-V7Uu6ZF9C0YMKuns9sLDzK6zoiV) to get started. Video 1.1 is a useful introduction to GitHub, but video 1.3 will help you out the most here.

All right, you're good to go! If you're looking to start out small, have a look in the [Formatting](#formatting) section below, in order to see how we structure the files to make the magic happen.

Good luck, and happy coding!

P.s. if you're looking to improve your Open Source skills, and it's coming up to October, why not check out [Hacktoberfest](https://hacktoberfest.digitalocean.com/). Running throughout the whole of October, if you complete 4 pull requests, you can earn a nifty t-shirt, shipped all the way from San Francisco, completely free!

## Formatting

### New Video

In the [videos](videos/) directory you will find the 4 directories listed below:

- _National5Teaching
- _National5Music
- _HigherTeaching
- _HigherMusic

Each of theses represents a playlist on the AMWMB channel. In each of these directories, there is a list of files, here is an example:

- 001-video-title.md
- 002-video-title.md
- 003-video-title.md
- 004-video-title.md
- index.md

If you wish to help by adding a new video, create a new file with the format below:

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

### New Playlist

If you're ready for something a bit more advanced, and you've noticed that Mr B has created a new playlist on the channel, have a go at setting up the new playlist for all to see.

First, you will need to create a new directory within [videos](videos/).

This must be formatted as so:

> _PlaylistName

Please note the underscore at the beginning, and the use of UpperCamelCase for the name. Remember this, as you will need to use this exactly later.

Next, you will need to create a file inside the directory you just created.

> index.md

Inside this new file, you should copy and paste the following text:

```
---
layout: series-index
---
```

- layout
  - This should stay as series-index in all cases. If not, you should definetly know what you are doing.

Once you have the directory setup, you can start to add video files. To do this, view [How to Format New Videos](#new-video).

Finally, you will need to configure the [_config.yml](_config.yml) file to accept the new playlist.

Under `Collections:` you should add the following template:

```
[Playlist name]:
    title: "National 5 Teaching"
    order: 1
    output: true
    permalink: /videos/national5/teaching/:name
```

- [Playlist name]
  - This must be EXACTLY the same as you named the directory above, WITHOUT THE UNDERSCORE(_).
- title
  - This is a string for the title of the playlist as it should be displayed.
- order
  - This is the order that the playlists are displayed on the [videos](answermewithmrb.tk/videos) page. Bad things happen if it's the same as another playlist?
- output
  - This should be true, just trust me.
- permalink
  - This is the link for each video in the playlist. Generally, this should start with `/videos` followed by something else, this should be ended with `:name`, this will be the name of the file of the video.
  
  And you're done! It seems that you have completed one of the harder tasks in managing this website. If you haven't already, maybe it's time to start taking a look at the [code behind the site](#writing-code)...


## Writing code

Anyone who knows me, IRL, will know that I'm pretty strict when it comes to organising and presenting. CODE IS NO DIFFERENT. Follow some key tips below for how to layout your code nicely.

### Indentation

You know that button on your keyboard? Yeah the one that says TAB. TABS SHOULD ALWAYS BE USED WITH HTML. ALWAYS.

If you're looking for extra brownie points, try to set your tab size to 2 spaces. This makes the gaps not look weird.

### Variable & File names

If you're like a certain person I know, cough cough, sometimes you think it acceptable to use weird or convenient variable or file names whenever it suits you. IT IS NOT.

Always try to use names that are meaningful and will help you when you are debuging, or when you have finished your 1000000 line of code project and can't remember what `banana` variable does...

Also, think about the other people you are working with on GitHub, making things READABLE is a necessity. Speaking of readability...

### Comments

We all do it. Sometimes you get lost in the thrill of writing code, however, remember that on GitHub, other people need to be able to use your code.

When possible, try to add some comments to help people understand what you have been writing.

Here are some of the common comment formats:

```
<!-- This is an HTML comment -->

/* This is a CSS comment */

// This is a JS comment

{% comment %} This is a liquid comment, if you ever use one of these, it means you're doing something pretty integral for the site {% endcomment %}
```