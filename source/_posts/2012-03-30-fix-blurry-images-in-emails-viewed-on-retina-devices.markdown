---
layout: post
title: "Fix blurry images in emails viewed on retina devices"
date: 2012-03-30 12:16
comments: true
categories: mobile email retina
---

This is a super simple and easy fix for the blurry image problem you may have 
noticed when reading emails on your retina capable device. Images and logos appear
all blurry and nobody likes that.

{% img /images/2012-30-03/email/email.png Non-retina version %}
{% img /images/2012-30-03/email/email@2x.png Retina version %}

The trick is to create a 2x version of your image, but to set the width and height
values to the smaller version. For non-retina devices, you will get a higher res
image that is resampled down, which should look good in most cases. For retina capable
devices, the image is resampled up to its original higher resolution, but still remains
crisp.

I recommend doing this for just important images in your email, like your logo and
other icons that may have text in them, like share buttons, etc. Using this technique
on complex photos may result in less than desirable anti aliasing effects.