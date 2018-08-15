---
title: 中研院 資訊所 暑期實習 week5
tags:
  - 暑期實習
  - 中研院
  - DEFCON
  - BFS
categories: 中研院
date: 2018-08-15 22:56:24
---

# 爆肝的一個禮拜
在這個禮拜一和老師 Meeting 後，整個架構又更完整、更清晰、需求與困難點都逐漸浮出。 晚上還有 DEFCON 集訓 ，肝臟快撐不住啦 !! 
# 更多的實作
開始把密碼學導入系統，考慮隱私保護，考慮可實作性，考慮 scalability，考慮各種東西，不斷把之前寫的 code 刪掉 -> 想到更好的辦法 ->  寫新的 code。 code base 和 smart contract 也都越來越肥。 

但有事情做的感覺還不賴，前幾個禮拜主要都是構想，開始實作之後才會發現想法和實現還是會有落差，像是時間複雜度，加密一筆資料很快，那加密幾百萬筆呢? 檔案傳輸的問題、Tamper Proof 的問題、不可竄改的問題、隱私保護的問題，要實作通通都要考慮到。

雖然只是要完成一個 Proof Of Concept 的系統，但當然也要有足夠好的架構可以說服其他人這個系統是能用在真實的環境的 ! 

道阻且長，需要更多的腦力激盪，更多的溝通、合作，完成這有趣的區塊鏈應用 !
# DEFCON 備戰 
這個禮拜晚上是 DEFCON 的賽期集訓，但因為身處偏僻的南港，要前往台科大參加集訓，實在是浪費金錢與時間，所以只到現場一天，其他時間就 remote 參加，線上討論了。

人果然是 deadline-driven 的動物，原本暑假開始就要逐步把 Attack Manager 完成的，但還是拖到賽前一個禮拜才開始真正動工。 Commit 數量圖![-w767](/images/15343443712931.jpg)
Infra 工作主要有幾個
- 網路方面
    - 現場網路架設
    - IPSEC VPN 
- Attack Manager
    - Frontend - Vue.js
    - Backend - Flask
    - Worker - Run Script
-  ELK 視覺化

我負責的是 Attack Manager 的 Backend ，用 Flask 實作 RESTful API ，剛好實習時也是用 Flask(但其實我 Node.js 更熟 xD)，就順便練練手。
最後寫了 647 行 ， only one file (好孩子不要學 ![-w560](/images/15343446126070.jpg)
之後也是刪刪改改，和其他 Team 、前端、Worker 溝通，改 Spec 是家常便飯 ，也是順利的做出可以 Run 的 Server 了 ~

再來就是在比賽時正式上線摟，請期待之後的 DEFCON 心得文。