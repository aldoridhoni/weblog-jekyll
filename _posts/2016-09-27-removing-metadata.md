---
layout: post
title: Removing Metadata
date: 2016-09-27 00:00:00
categories: 'How-To'
---

Image is a great way to communicate ideas. With the advancing of smartphone and digital cameras, more picture is taken and uploaded to the web.
With it come the data embedded in the image we upload. For example data about :   
- Time and place of picture taken   
- Camera info and settings   
- Location   
- Thumbnail   
- Processing Application   


![photo with metadata](/public/images/2016/09/27/metadata.png)

It's better to remove the metadata. Using program called jhead.

```terminal
$ jhead -exifmap IMG_20151227_144151.jpg | sort | head n20

Aperture     : f/2.7
Camera make  : LGE
Camera model : Nexus 4
Date/Time    : 2015:12:27 14:41:52
Exposure time: 0.050 s  (1/20)
File date    : 2015:12:27 14:41:52
File name    : IMG_20151227_144151.jpg
File size    : 1482440 bytes
Flash used   : No
Focal length :  4.6mm
GPS Latitude : ? ?
GPS Longitude: ? ?
ISO equiv.   : 1100
JPEG Quality : 85
Map: 00000  4d 4d 00 2a 00 00 00 08 00 0c
...
```

```terminal
$ jhead -purejpg IMG_20151227_144151.jpg
Modified: IMG_20151227_144151.jpg
```

```terminal
$ jhead -exifmap IMG_20151227_144151.jpg
File date    : 2015:12:27 14:41:52
File name    : IMG_20151227_144151.jpg
File size    : 1474874 bytes
JPEG Quality : 85
Resolution   : 3264 x 2448
```

The final image has removed information about the camera info and settings.
