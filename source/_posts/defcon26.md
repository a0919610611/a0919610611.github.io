---
title: DEFCON 參加心得
tags:
  - DEFCON
  - BFS
  - 資安
categories: 資安
date: 2018-08-19 19:27:12
---

# 賽前準備
實際把 Attack Manager 上線給其他 Team 用，找到不少 Bug 和 UI 可改善的地方，直到開賽前都還在修呢 XD

準備簽證 ESTA 、役男出境、護照、換洗衣物就出國啦 ~~ 

基本上都是團體行動，也不需要特別準備什麼 XD
# 飛機 ~
這次來回都是搭聯航(United Airlines)，在舊金山轉機再飛到拉斯維加斯。美國實在是太遙遠了，飛機坐了十幾個小時。
![IMG_0612](/images/IMG_0612.jpg)
第一次看日出居然是在飛機上! ![IMG_0607](/images/IMG_0607.jpg)  
到達舊金山 ~ ![IMG_0609](/images/IMG_0609.jpg)
到達拉斯維加斯 ~ ![IMG_0613](/images/IMG_0613.jpg)
# 飯店 & Buffet
這次是住在 Caesar Palace ，真的是有夠大，裡面有飯店、精品店、餐廳、速食、賭場，真的是應有盡有。

房間也是蠻大的，但房間的食物＆水通通都要錢阿 !!! Las Vegas 真的是什麼都要錢 !! 比較雷的點就是沒有 牙膏、牙刷，聽說其他比較高級的房間有，這不是必需品嘛 ORZ 

開賽前吃的食物，都是在 Caesar Palace 四處吃吃，牛排、漢堡等，一餐平均都 15鎂 up，在台灣都可以去吃到飽啦 ! 且入境隨俗，每餐吃完都會給服務員小費，和台灣不太一樣，美國幾乎就是真的有一個固定的服務生負責你這一桌，感覺還蠻不錯的 !
## 打完比賽吃的 Buffet
![IMG_0633](/images/IMG_0633.jpg)
![IMG_0634](/images/IMG_0634.jpg)

# DEFCON 開始 !
DEFCON 總共有四天，第一天開始就有 talk ， CTF第二天才開始打。
但第一天的重頭戲不是 talk ，是紀念 T-shirt 啊啊啊啊啊 !!! 紀念 T 穿出去，走路都有風呢 ! 所以真的可以說是大排長龍，排滿兩大房間、一條走廊，我以為我們已經來排的夠早了，但排的時候已經只能在走廊了 !! 
可以排到時，最想要的幾件衣服都賣光了(正面印著大大的 DEFCON)，因此買了其他件，花了35鎂，這可是先要花 280鎂的門票才能進來排隊呢，實在是價值不菲的一件衣服啊 !
買光衣服也沒聽 talk，就回房間繼續幫 Attack manger 增加 feature，給大家 test，並早早睡覺，明天早上，正式開打 !!
# CTF 開打 ! 
身為 Infra 的一員，必須到現場確保網路、Server、Attack Manager 可以正常運作。
規則也是當天才知道，真是有夠刺激 XD
這次比賽結合了 Attack & Defense 和 King of the hill (KOH)，KOH只有前五名可以拿到分數。

## 規則
https://www.oooverflow.io/obey/

## King Of The Hill
三天各有一題 KOH ，第一天的是組語填空「reverse」，Exploit Team 是用 script 輔助，最後也有一小段時間衝到前五名賺點分數，賽後聽說應該繼續 reverse engineering ，裡面有漏洞，難怪題目叫 reverse XD

第二天是「doublethink」，題目的意思是讓能一段shellcode 能在越多 ISA (Instruction Set Architecture)執行越好，有這麼多種架構。![-w722](/images/15346737339262.jpg)
HITCON 在賽中一直以第一名碾壓大家，賽後才知道是有漏洞可以利用 race condition來作弊 XD 我們最後也手動串了5個且拿了一點分數，聽主辦方說是沒作弊最高的(?)

最後一天的是「propaganda」，要我們做 binary patching，印出特定的字串，用到的 bytes 越少，分數越高。最後一天只有四個小時，也沒有做出來。

## Attack & Defense
第一天下午才放出了 A&D 的題目，之後就分別被 PPP 和 DEFKOROOT 分別 first blood了，真是恐怖如斯！ 

而今年封包不像以往是每過幾個round就釋放出來，變成大家都靠 replay 賺分的情況。今年則是題目被打的差不多、或到「steady state」才把封包放出來，所以今年更考驗 找洞、撰寫 exploit 的速度和 patch的能力。

第二天有封包出來之後，Packet Team 也力馬利用自動化工具做出了 replay exploit script ，上傳到 attack manager ，我們才「正式開打」!

而這一天比較有趣的是有 web題叫做「 bew 」，A&D很少有非 binary題，所以還真是少見，但這題跟 Web Assembly有關XD 因為可能設計有問題，我們有偷到別人leak出來的flag，也寫了script 偷到一堆分數 XD 也是讓我們之後能12名的關鍵

到了最後的第三天，我們在第13名，HITCON在第3名，而今天是沒有scoreboard的，且只有四個小時，只能撐到最後了 ! 

原本「bew」這題有偷別人的 exploit 再生出自己的 exploit，但手速輸給其他人，這題就被人攻佔、再也打不進去了 QQ

在前一天大家熬夜在「poool」這題生出了exploit 和 patch 之後，也成了今天的功臣，至少都能打下一半以上的隊伍，之後再搭配 packet 組的 replay exploit 幾乎可以打到 2/3 ，也讓我們可以持續得分，穩住名次。

中間的小插曲，一題跑太多 exploit script，沒有仔細確認 script 對哪些 team有效，就給他全部灑下去，然後就被因為太多連線數被警告了 XD 

總體來說三個組都各司其職，溝通搭配沒發生什麼太重大的問題，可喜可賀 !

而主辦方這次因為第一次主辦發生了不少問題。
- git server 上 patch 有問題，之後回歸 HTTP
- admin interface 意外露出來，好險沒外洩題目
- 第二天計分版有錯誤，第三天修正了
- 第二天延後兩小時開賽 XD
- 有一題和密法學有關的題目，因為流量實在太大，被提早關掉了 XD，其實應該是現場飯店網路太雷了 ...
- etc...

但辦 CTF 不是件容易的事，尤其是「Attack & Defense」，跟我們一樣是「初生之犢」，很期待他們之後的表現 !!



# 最後成績
![defcon_result](/images/defcon_result.jpg)
恭喜 HITCON 拿到季軍第三名 ! 而我們初次參賽也拿到 12名，實在是非常不錯的成績 ! 

DEFKOROOT 從第一天就碾壓，冠軍也不是很意外，傳統強隊 PPP 更是不用多說，中國的 A\*0\*E也是不容小覷 !

比較讓人意外的是 Shellphish 居然掉到最後一名，可能是因為他們的主力都變成今年主辦 OOO 的成員了。

最後閉幕典禮現場擠爆了，只能在房間看轉播 QQ
# 感謝隊友、教授、助理、教育部、企業
助理熬夜(凌晨1點到4點)幫我們排DEFCON的票，比賽期間幫我們買早、中、晚餐還有宵夜。

教授們幫我們擋住上面的壓力，讓我們可以只要專心在比賽上面。

教育部(AIS3)和各個企業(趨勢科技、中華電信、中華資安、資褓儲存)出了經費，讓我們有免費機票、食宿，還有零用金可以自行運用。

感到「資安即國安」不是說說而已，教育部也辦了「AIS3」、「台灣好厲駭」等訓練活動，看出是有在重視這一塊，畢竟是小國，軟實力培養還是CP值比較高的。

聽聞韓國的 BOB(Best of the Best)計畫經費無上限，近幾年也在各項大賽橫掃，電競方面也是很強，看來韓國政府更是努力增強軟實力，這是台灣可以效法的。

還有感謝iThome 的採訪，幫我們拍了不少照片 XD 
分享一下 [【大話資安】HITCON CTF戰隊領隊李倫銓：這一年，我們一起打過的CTF](https://www.facebook.com/ithomeonline/videos/1673247822801622/)，有講到這次的比賽、和CTF的介紹。

最後當然是要感謝BFS戰隊的隊友們，比賽這三天充分的分工，現場的Infra Team、封包的 Packet Analysis Team ，攻擊的 Exploit Team，缺一不可，讓我們初次挑戰CTF的最高殿堂 - DEFCON CTF，在精挑細選的24隊中還能拿到第12名。

# 曬戰利品 ~~
![IMG_0645](/images/IMG_0645.jpg) San francisco 15 鎂 、Las Vegas 10鎂、左上 DEFCON記念 T-shirt 35鎂(門票要280鎂呢 XD)
![IMG_0649](/images/IMG_0649.jpg)
鑰匙圈一個 3鎂
![IMG_0646](/images/IMG_0646.jpg)
拯救我脖子的枕頭 19鎂 ，去程沒有枕頭，下飛機脖子真的快斷啦 !!
