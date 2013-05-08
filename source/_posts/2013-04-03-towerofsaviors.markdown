---
layout: post
title: "TowerOfSaviors"
date: 2013-04-03 14:42
comments: true
categories: Game
---

神魔之塔外掛 - 更新 for 2.5 version

教學文捏

請先下載：

[CheatProxy][CheatProxy](完整功能)
or
[CheatProxyLite][CheatProxyLite](僅提供檢視關卡掉落卡片功能)

下載解壓縮之後，將會有如下圖
![ExtractFolder][ExtractFolder]

請先確定JAVA已正確安裝，.jar 檔並`不會`被解壓縮

請依序執行、設定，如下圖

1. 執行 burpsuite.jar，並如下設定
    <br>    
    切換至Proxy選項
    ![bp1][bp1]
    <br>    
    設定 "Intercept is off"
    ![bp2][bp2]
    <br>    
    切換至Options選項
    ![bp3][bp3]
    <br>    
    設定 "Running" 為勾選
    ![bp4][bp4]
    ![bp5][bp5]

2. 執行 tower.jar
    <br>    
    點選Start
    <br>    
    ![tw1][tw1]
    <br>    
    記住紅色框框，IP以及local port
    <br>    
    ![tw2][tw2]

3. 設定 HTTP proxy 
    <br>
    iPhone
    <br>
    點選設定，Wifi
    <br>
    ![ip1][ip1]
    <br>
    點選最右邊小箭頭，進行代理伺服器設定
    <br>
    ![ip2][ip2]
    <br>
    將前面步驟所記錄的IP以及local port填上
    <br>
    ![ip3][ip3]
    <br>
    Android
    <br>
    點選設定，Wifi
    <br>
    ![ss1][ss1]
    <br>
    長案已連接的Wifi
    <br>
    ![ss2][ss2]
    <br>
    點選更改網路設定
    <br>
    ![ss3][ss3]
    <br>
    勾選顯示進階設定
    <br>
    ![ss4][ss4]
    <br>
    將代理伺服器調成手動
    將前面步驟所記錄的IP以及local port填上
    <br>
    ![ss5][ss5]
    <br>

4. 重啓 神魔之塔
    <br>
    ![g1][g1]

5. FAQ
    - Q: 用此代理我可以修改卡片嘛？
        - A: 使用此代理並不會真正擁有卡片，當代理關閉時，卡片會回復成原有的樣子喔。
    - Q: "Loot" 是用來顯示什麼的？
        - A: "Loot" 會顯示進入關卡時會掉落的卡片，若想刷卡沒有自己要的卡片就可以關掉重開囉！
    - Q: 可以讓多個人同時使用代理嘛?
        - A: 代理可同時多人登入，但僅限區網內。
    - Q: 多人使用會不會有什麼問題？
        - A: 多人登入唯有"Loot" 記錄會被洗掉，一旦有使用者開啟關卡進行戰鬥，"Loot" 欄位就會清空重新顯示。
    - Q: 為什麼戰鬥結束後，獲得的卡片都不見了，背包一直都是一樣的卡片呢?
        - A: 利用此代理的牌組進行戰鬥，所獲得的卡片、金錢、經驗、點數會儲存下來，但除非關閉代理否則獲得的卡片暫時不會顯示。
    - Q: 所以背包空間不會影響遊戲進行囉？
        - A: 是的，除非關閉此代理，才有可能會出現背包空間不足的警示喔。
    - Q: 用此代理我的Twitter和微博帳號為什麼登入畫面都是白色的阿？
        - A: 阿阿阿，因為我還沒有找到問題所在，請先關閉iFile限制，讓程式正常寫入，已經登入過的話，「"Twitter"綁定的帳號」是可以正常運作的喔！
    - Q: 那我可以不要換卡，只用看卡的功能嘛？
        - A: 有有有，我最近加上功能了，有個"Change Card"的勾選框，打勾就會換成328張卡片，不打勾就會按照自己原本的牌組囉，不過我還幫大家自動改掉背包、隊伍空間，所以至少過程中是不用困擾隊伍怎麼分配，也不用花魔法石買空間啦！
        - A: 提供另外一個方案，可以下載Lite版本，裡面只有顯示掉落卡片的功能，並不會修改任何資料(背包、隊伍空間、卡片)喔！
    - Q: 這樣還有什麼好玩的阿？
        - A: 卡組總共有328張，雖然各種神卡都有了，但其實4封之後不再適用神卡無腦輾壓，很吃卡組的配合以及轉珠技術阿，不然其實給你神卡你也過不了五封，官方還是想要你一直死一直買魔法石來復活阿！！這只是提供大家可以更多元的玩遊戲，而不會因為想要的卡抽不到導致卡牌組就玩不下去。

[CheatProxy]: https://mega.co.nz/#!H0YjFSzJ!EjClgTunfQova4j7ACmMIktwHrxJ6FR_e-vJKV26dE8
[CheatProxyLite]: https://mega.co.nz/#!3pYykIAS!EFmI7C73rtNOW4UlAGZ9_QzdPVdrCphGQgcy6Q9Rx1w
[ExtractFolder]: /images/ExtractFolder.png "Extract folder"
[bp1]: /images/bp1.png "bp"
[bp2]: /images/bp2.png "bp"
[bp3]: /images/bp3.png "bp"
[bp4]: /images/bp4.png "bp"
[bp5]: /images/bp5.png "bp"
[tw1]: /images/tw1.png "tw"
[tw2]: /images/tw2.png "tw"
[ip1]: /images/ip1.png "ip"
[ip2]: /images/ip2.png "ip"
[ip3]: /images/ip3.png "ip"
[g1]: /images/g1.png "g"
[ss1]: /images/ss1.png "ss"
[ss2]: /images/ss2.png "ss"
[ss3]: /images/ss3.png "ss"
[ss4]: /images/ss4.png "ss"
[ss5]: /images/ss5.png "ss"
