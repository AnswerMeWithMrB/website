# Answer Me With Mr B - Website
Welcome! Did you know, Physics is true ya!

Here we have a Work In Progress website for the YouTube channel [Answer Me With Mr B](https://www.youtube.com/channel/UCv7XjzuzmAKm458IqFehCPQ).

If you wish to help out, view the [Contributing instructions](#contributing).

- [Contributing](#contributing)
- [The Future](#the-future)

# Contributing

Glad you're willing to help out!

Have a look at the links below to begin contributing.

- [How to Github](#how-to-github).
- [Formatting](#formatting)
  - [New Video](#new-video)
  - [New Playlist](#new-playlist)
- [How It Works](#how-it-works)
- [Writing Code](#writing-code)


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
description: [Video description]
videoId: [Video id]
layout: video
---

[Extra content]
```

Here is what each of these means:

- order
  - This is the order that the video comes in the playlist
- level
  - This is the level that the video is aimed at (National 5 / Higher)
- title
  - This is the title that the video has on youtube (ignore number)
- description
  - This is the description that the video has on youtube.
- videoId
  - This is the id that the video is given by youtube. You can find it in the url eg:
    - youtube.com/watch?v=[videoId]
- layout
  - This is the layout that tell the site how to display the page. Leave this alone when adding a new video.
    - This will be removed and placed in a default config location in a later version.
    
- [Extra content]
  - Anything below the `---` line will be displayed on the page.
  - This can be formatted as html.
  
  
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


## How It Works

### Domain

The domain for the site, [answermewithmrb.tk](http://answermewithmrb.tk), is provided by [Freenom](https://www.freenom.com/).

This means that the domain is free, however it must be renewed every year. Please leave an issue if you have a query regarding this.

### Hosting

The site is hosted using GitHub Pages, this means that it is provided free of charge.

Read on below to find out about GitHub pages.

### GitHub Pages

GitHub Pages is a free service offered by GitHub in order to host static websites.

Find out more [here](https://pages.github.com/).

GitHub Pages was chosen as it offers WONDERFUL integration with Jekyll, read on below to find out more...

### Jekyll

[Jekyll](https://jekyllrb.com/), is what powers GitHub pages.

For our purposes, it is what allows the video pages to be rendered from just the data .md files.

If you're looking for something more challenging to do, have a look at the [Jekyll Docs](https://jekyllrb.com/docs/) and try to make a new page.

[ToDo] How about finding a way to display the most recent video on the home page. **WARNING - quite advanced!**

### Liquid

Liquid is a fancy way of inserting information into pages.

This is how Jekyll inputs the data from the .md files.

> {{ content }}

This is an example of liquid syntax.

There is way too much to explain here, but between the Jekyll docs and the liquid docs, I'm sure you can figure it out.

- [Jekyll Liquid Docs](https://jekyllrb.com/docs/liquid/)
- [Official Liquid Docs](https://shopify.github.io/liquid/)

### Files in the repo

There are many files that can be found in the repo above, here are some explanations of some of them.

- .gitignore
  - Github uses this to see which files it should ignore when pushing new commits. When developing on GitHub Desktop, this will be used to not push your built `_site` files to the repo.
- 404.html
  - This is the page which is displayed when the url doesn't match any other page on the site. Physics joke included, of course.
- CNAME
  - This file is used by GitHub pages in order to setup the custom domain: [answermewithmrb.tk](https://answermewithmrb.tk)
- Gemfile
  - The Gemfile holds details about the Ruby dependencies required by the site. This includes [Jekyll](#jekyll).
- Gemfile.lock
  - Similar to `Gemfile`.
- README.md
  - You're reading it right now.
- _config.yml
  - This is where the [Jekyll](#jekyll) configuration for the site is stored.

## Writing Code

Anyone who knows me IRL, will know that I'm a stickler when it comes to organising and presenting. Ignore the handwriting. CODE IS NO DIFFERENT. Follow some key tips below for how to layout your code nicely.

### Indentation

You know that button on your keyboard? Yeah the one that says tab, or those two funky arrows. TABS SHOULD ALWAYS BE USED WITH HTML AND CSS AND JS AND EVERY CODING GOOD LANGAUAGE. ALWAYS.

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

# The Future

There are many places that the AMWMB site could go, below are just a few ideas that you could many persue.

## Astronomy

There's endless possiblity when it comes to web developement. And one thing we can also manage, is to create more pages.

Maybe branching AMWMB into the extra curricular could encourage more people into the realm of Physics.

## Activities

At the moment, there is the ability to add a quiz to the bottom of any video page. I would love for this functionality to be expanded.

Making a small game or animation for each video could be a really cool idea in order to make the video more interactive.

## Your Ideas

Have a cool idea? I'm all ears! Head over to the issues tab at the top of the page and write out a message. Once Mr B gives the go ahead, we'll get on it!

But in the meantime, how about YOU be the one to implement your idea. Take a look at [How to GitHub](#how-to-github), and how we format the pages on the site: [Formatting](#formatting).