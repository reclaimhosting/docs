---
title: 'Media'
taxonomy:
    category:
        - docs
---

Upon occasion, you may want to include media (images, audio, video) in your site's posts and pages. There are generally two approaches to handling media in WordPress.

###Uploading

You can upload the files into your site's Media Gallery and then link to them in your posts/pages. 

![image1](https://farm2.staticflickr.com/1478/23893304324_39f649dc13_z.jpg)

This works very well for images, and when you take this approach for images you have the added benefit of being able to make use of WordPress' built in (albeit rudimentary) editing tools. Also, when you upload images to WordPress, it automatically creates different sizes that you can use, as needed.

![photo2](https://farm2.staticflickr.com/1631/24153792439_bcb846365d.jpg)

This approach works less well for video. In order to have your media files actually show up in a "player" (with controls for stopping, pausing, etc.) you'll need to install a plugin. Otherwise, you'll only be able to include links to the files. How people view them will depend a bit on the setup on their own computer and in their own browser. They may, for example, have to download the media file and then open it in another program on their computer.

###Embedding

You can embed media from other sites easily in WordPress. Embedding an image just means providing a URL to it's location elsewhere on the Web. Instead of uploading it to the server, WordPress grabs that image from the external source and displays it on your post/page. However, with this approach you lose your editing capabilities as well as the resizing feature.

![photo3](https://farm2.staticflickr.com/1604/24414250222_4560574ee2_z.jpg)

Embedding audio and video from external sources becomes easier with every version of WordPress it seems. These days, you can embed video and audio from many external services (YouTube, Vimeo, SoundCloud, complete list here) by simply placing the full URL of the audio/video location on it's own line in your post/page. [There is a complete list](http://codex.wordpress.org/Embeds#Okay.2C_So_What_Sites_Can_I_Embed_From.3F) of supported external services, and you can [learn more about embedding from external sources](http://codex.wordpress.org/Embeds) at the WordPress site.

Our general advice is to use externally hosted media whenever it makes sense and works. This is **usually** the case when you need to use audio or video; without plugins, well-presented audio and video in WordPress is tricky. For images, if you need to do basic editing and/or require different sizes of images, upload them to your site. Otherwise, consider referencing them from another location (your Flickr account, for example).