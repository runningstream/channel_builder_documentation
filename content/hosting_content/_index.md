---
title: "Hosting Content"
date: 2021-08-29T14:29:29-05:00
description: "How to host content to play via Running Stream, your personal streaming channel"
weight: 1
draft: false
---

The purpose of Running Stream is to make your content available on your streaming device.  In order to do that, your videos have to be available on the Internet.

Making content available via the Internet is called "hosting content".  There are several ways you can do this, and you'll want to choose a good easy way for you.

## Hosting Options

We will add more descriptions of options here over time, because many more options exist beyond the ones documented below.

From easiest to toughest, some reasonable hosting options include the following:

* Google Drive
* Web Hosting Service
* Amazon Web Services S3
* Self-Run Webserver

## Google Drive

Google Drive is a service run by Google that provides a simple-to-use office tools suite (word processing, presentation visual aids, and spreadsheets) and file storage/sharing platform.  Google Drive provides a significant amount of free storage space.  Many of you will already use Google Drive, and there is a trick to permit videos stored there to be streamed.

Please note that Google Drive is no longer connected easily with Google Photos.  There is no known streaming solution for Google Photos, however you can download videos from Photos and upload them to Drive then stream them from drive.

To get the Media URL for a video stored on Google Drive, do the following:

1. Open Google Drive, login, and browse to the video you wish to stream
2. Right click on the video, then click "Get Link"
3. Below the address of your new link, there's a dropdown menu that says "Restricted" by default - click it, then select "Anyone with the link"
4. The link in the box will look something like `https://drive.google.com/file/d/1_3zeAMvtsBx9ho-703XQpmC4am56gNDq/view?usp=sharing`.  Copy only the part after the `/d/` and before the `/view?...`.  In this example, you'd copy the `1_3zeAMvtsBx9ho-703XQpmC4am56gNDq`.
5. The data you copied is the video's "ID"
6. Put that video ID at the end of this Media URL, right after the `id=` part: `https://drive.google.com/uc?export=open&id=`
7. Click "Done" back in the Google Drive sharing form

You can now stream your video with that Media URL.  Here are some example Media URLs built using this technique:

* `https://drive.google.com/uc?export=open&id=1_3zeAMvtsBx9ho-703XQpmC4am56gNDq`
* `https://drive.google.com/uc?export=open&id=1sluvO7qWPNnwCr086dcLYm6kt_Uk3Gvx`

Both are videos of mountain streams.

## Web Hosting Service

Many companies exist which will host a website for you.  Sign up for one, and store your videos there.  This option provides lots of flexibility, including the ability to limit video access to specific Internet addresses.  The process to post a video will differ by webservice.

Creating a website is moderately complex task, but many tutorials exist to help.

## Amazon Web Services S3

Amazon Web Services (AWS) provides a service called S3, which stands for Simple Storage Service.  With S3 you can store files and make them available to the public, or keep them private.  S3 makes it simple to store files and make them accessible on the Internet.

Signing up for AWS, setting up an S3 bucket, making it public, and retrieving the content URL are moderately complex tasks, but many tutorials exist to help.

## Self-Run Webserver

One of the more complex techniques for making your videos available for streaming is to run a webserver on your home computer.  Common webservers include Apache and Nginx.

Running your own webserver from your home is moderately complex, but many tutorials exist to help.

Keeping your webserver secure, preventing your personal files from being exposed to the Internet, and preventing attackers from leveraging your webserver, are all important tasks.  These are the true challenge with running your own webserver.  All can be overcome - however this option does bring the most risk to your security.

If you are an enthusiast or hobbyist though, we highly recommend you try this route.  Becoming familiar with Linux is a good start.
