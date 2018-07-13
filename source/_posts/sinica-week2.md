---
title: 中研院 資訊所 暑期實習 week2 - FLOLAC week1 !
tags:
  - 暑期實習
  - 中研院
  - FLOLAC
  - Functional Programming
  - Lambda Calculus
  - Logic
mathjax: true
date: 2018-07-13 20:40:16
---

# A Week Of BRAINSTORM !
這禮拜在王柏堯老師的建議下，跑去台大旁聽中研院在台大開的暑期課程 FLOLAC ，中文名稱是 「邏輯、語言與計算」暑期研習營，總共兩週10 天的課。
課程網址: http://flolac.iis.sinica.edu.tw/flolac18/index.html
# 過完第一個禮拜的感想
真是燒腦的一個禮拜，畢竟交大沒有「Functional Programming」這堂課，現在連「Programming Language」這堂課也沒了（以前好像有)，只剩下「Formal Language」。 因此對於理論計算機科學 （ Theoretical Computer Science ) 非常的陌生，正規也就自動機畫來畫去，Turing Machine 也就淺嚐輒止，交大(或者是台灣普遍的大學)資工系幾乎全都往 Engineering 偏了，理論的課更多是開在研究所，但大學沒接觸過又怎麼會往這方向研究呢 ? 諷刺的是交大資工的英文還是「Computer Science」。
FLOLAC 也是讓我開了眼界，雖然不一定會往這方向走，但知道自己使用的高階程式語言是別人在默默耕耘的結果，不禁肅然起敬阿 !!
# 課程介紹
> 「邏輯、語言與計算」暑期研習營希望培養學員獨立進行基礎計算科學研究之能力。從第二年起，本研習營在兩大主題 — 程式語言與形式驗證之間輪替。今年（偶數年）之主題為程式語言，正式學分班課程名稱為「程式語言理論與型態系統」。

> 本課程將講授程式語言與形式驗證領域之入門理論與知識，包含邏輯、λ calculus、函數編程 (functional programming)、依值型別(dependent type)等等，希望培養學生以形式邏輯進行清晰思考的能力，了解邏輯與程式語言、型別系統的密切關係，以及型別系統在程式語言中扮演的角色，使學生能以歸納、遞迴方式理解並解決程式設計問題，能運用軟體工具輔助邏輯推理並證明程式之正確性，並具備在程式語言相關領域進行研究的能力。
![-w977](/images/15314843874468.jpg)

# 心得
Functional Programming (FP) 改變了我對程式設計的思維。比起 傳統 Imperative Programming , FP的一大概念即是「程式即證明」，而背後又有一大堆理論。而 FP 的計算模型是 **$\lambda$ (lambda) Calculus** ，和 Turing Machine 有一樣的計算能力，但 rule 比較少，也比 Turing Machine 比較早被提出來。 這次上課是使用 Haskell 這個語言來實作程式，寫起來真的和寫程式證明差不多，目前上到的大部分都是利用 induction (數學歸納法)，而之後講到的 fold ， fold fusion theorem 這部份就有點困難了，還需要利用假日好好仔細消化這周的進度。

這週還上了 logic 和 $\lambda$ Calculus 。 Logic 主要是各種 proposition (命題) 的 derivation ， $\lambda$ Calculus 也差不多，兩門課相輔相乘，提供了 Functional Programming 的理論基礎。

雖然是來旁聽的沒有學分，但聽說期末考考過能拿到修業證書，還是來努力讀一下，希望這兩個禮拜不只是聽聽而已。
