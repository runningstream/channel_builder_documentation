---
title: "Encoding"
date: 2021-10-31T21:40:50-05:00
draft: false
---

A common cause of videos not playing on your streaming device is incorect encoding...

## What is Encoding?

Encoding is how video or audio, moving pictures and sound, are converted into the 1s and 0s computers use to store data.  You can imagine this is a little tricky...  There are many different encodings out there!  This is why the problem is so common - because there are so many different ways to encode things, something like a Roku will only implement a few.

## What Encodings Work?  How do I Change Encodings?

The Roku supports a bunch...  So if you have a video file that's not supported by it you can change encodings to make a new video that's compatible.  YouTube videos seem to generally be encoded wrong.

One tool that makes changing encodings quick and easy is `ffmpeg` - [downloadable here](https://www.ffmpeg.org/).  If you're on Linux, you can probably just install `ffmpeg` from your distribution.

With it installed, you can use this command to change to `h264` encoding, which works well with Roku:

`ffmpeg -i input_file.mp4 -c:v h264 output_file.m4v`

You can use your webbrowser to convert files too - [ffmpeg browser demo](https://ffmpegwasm.netlify.app/#demo).  Setting "Choose a sample config" to `x264 (mp4)` (the default) seems to produce acceptable results.  Then click the red "upload a video/audio file" button, and wait.  A large chunk of code downloads, then converts your video inside your browser, never leaving your computer.  When conversion is complete it will display as a video - use the controls inside the video to download it.  This is a slow process and may crash your browser if you don't have enough RAM.
