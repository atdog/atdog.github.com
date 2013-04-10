---
layout: post
title: "audio conversion"
date: 2013-04-10 17:12
comments: true
categories: Tools
---

- Convert AAC to MP3 format

        ffmpeg -i input.m4a -acodec mp3 -ac 2 -ab 128 output.mp3

- Batch convert
    
        for i in *.m4a; do
            ffmpeg -i "$i" -acodec mp3 -ac 2 -ab 128 "${i%m4a}mp3"
        done
