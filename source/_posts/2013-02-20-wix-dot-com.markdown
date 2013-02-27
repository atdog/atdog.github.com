---
layout: post
title: "Wix.com"
date: 2013-02-27 12:41
comments: true
categories: Security
---

[Wix.com][Wix.com] 最近似乎在Facebook竄紅起來，

![wixcom][wixcom]

Wix主打提供使用者快速建立web site的功能，

使用者僅需要用滑鼠做些基本的操作、或是會點flash，而不需有任何HTML的腦袋，

就可以完成一樣不錯的作品，

不過這邊要跟大家介紹一些Wix.com的小秘密，

由於過度依賴這類網站很容易導致資安問題，

---

現在的網路世界中，為了方便性，這樣的網站實在不少，

以[Wix.com][Wix.com] 來說，

`26,756,521 sites created!`

從建立至今由使用者所建立的網站個數，

雖然使用者建立的網站，以靜態網頁為主，

不太會被攻擊者攻擊，大不了就DDOS，被攻擊過後，網站本身依舊活的好好的，

反之，假設攻擊者攻陷的是[Wix.com][Wix.com] ，

26,756,521個Sites就是死的。

---
<br>
最後如下...

![wixbackdoor][wixbackdoor]

你確定你的Host端(Wix.com)，Security做的足夠嘛？

---
<br>
題外話，

如果大家想知道一個網站是不是由Wix所建立，

很簡單，

在HTML原始碼中，可以看到Wix.com的js、images的link，

甚至該Site的Wix.com的UID都可以在裡面找到，

(有UID就可以做login bruteforce，甚至能做Cookie的偽造)

這樣就可以快速的找到該Wix.com的使用者相關訊息了!


[Wix.com]: http://www.wix.com
[wixbackdoor]: /images/wix-backdoor.png "Wix backdoor"
[wixcom]: /images/wixcom.png "Wix com"
