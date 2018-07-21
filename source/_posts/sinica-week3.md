---
title: 中研院 資訊所 暑期實習 week3 - FLOLAC 結束 !
tags:
  - 暑期實習
  - 中研院
  - FLOLAC
  - Functional Programming
  - Lambda Calculus
  - Logic
  - Pi Calculus
mathjax: true
date: 2018-07-21 23:32:16
---

# FLOLAC 結束啦 ~~

## Functional Programming - Type Class & Monad
這次上課主要就是講Type Class 和傳說中的 Monad ，但因為只有三小時，只能淺淺的帶過。
### Type Class
很容易跟 OO (object oriented) 裡的 class 做聯想，用起來也有點像 ，但穆老師叫我們忘記 OO 來學習。
[Type & TypeClass In Haskell 介紹](http://learnyouahaskell.com/types-and-typeclasses)
### Monad
[圖解 Monad by 阮一峰](http://www.ruanyifeng.com/blog/2015/07/monad.html)
用起來跟 js 的 promise 的有點像
[JavaScript promises are just like monads](https://swizec.com/blog/javascript-promises-monads/swizec/7814)


## Logic - Agda
Agda 火力展示 & 傳教 
柯向上老師用 [Aquamacs](http://aquamacs.org/) 配合 LaTeX，飛快的打出各種數學符號 ($\forall,\exists, \land,\lor$) ，真的是潮到出水，飛快的打出各種數學證明，展現了 dependent type programming 的威力。
附上 gist [FLOLAC18.agda](https://gist.github.com/josh-hs-ko/3a0ea16a225ca4efbd01428c06b8fdba)，趕快來膜拜 <(_ _)> 。
## $\lambda$ Calculus
已經上到有點恍惚了 QQ
Church Encoding 有點抽象，利用 function 來模擬 type ，像 $ True = \lambda xy.x \space False=\lambda xy.y$ 這種東西。
## $\pi$ Calculus & Session Type & Scribble
這次邀請到  Imperial College London  的 Prof. Nobuko Yoshida 和 Dr. Rumyana Neykova  來上這門課。
### $\pi$ Calculus
這部分由 Prof. Yoshida 教學 ， 除了日式英文有點需要時間才能聽懂，其餘皆無可挑剔。講的深入淺出，是全部裡面我覺得吸收的最好的一門。
和 $\lambda$ Calculus 很像 ，也有 Free name / variable ，引入了 channel 的概念，試圖把 Process 間的 Communication 用形式的方式表達出來。
### Session Type
這部份由 Dr. Neykova 來教學，主要的精神是把 Process 之間的 Communication 都加上 Type，這樣就可以確保不會因為 type error 造成通訊失敗 (EX: A 要 int , B 給 string)等情況。
### Scribble
Dr. Neykova 還介紹了一個寫 Protocol 的工具 [Scribble](http://www.scribble.org/)，而之後的演講也提到利用 Scribble 寫出的 .scr file 配合 compiler 結合 IDE ，達到 code auto completion ，非常厲害 ~~
## 期末測驗
在兩個禮拜緊湊的課程之後，還沒有好好消化吸收，馬上就迎來恐怖的 Exam，也只能硬著頭皮上了 ~~ ( 雖然只是個旁聽生 XD 
考試的形式是4個科目個有一份考卷，所以要怎麼分配時間就是一個課題。 而時間只有三個小時，我最後只有把 $\pi$ Calculus寫完，其他的都大概完成 $80\%$而已。
課程慣例，考完有 Pizza 和 炸雞 ， 賺 !
## 心得
總體來說是非常值得參加的課程，雖然沒有拿到學分 (後來才發現交大資工網頁好像有宣傳 XD)，但認識到了一個嶄新的領域。看了幾間大學的Lab 和課程，發現這領域幾乎沒有任何相關的，目前只有看到穆老師在台大資管開的程式語言(老師以前有在交大開，現在沒了 嗚嗚)，看來研究這部分的都集中在中研院了 XD
雖然上完覺得自己的數學廢到掉渣 (資工開的數學課根本就是___)，但也知道了新的寫程式方法、新的計算模型，入了邪教(x ，收獲滿滿。
### 新的方向
目前在交大做的畢業專題題目是「Automatic Exploit Generation」，使用到 [angr](http://angr.io/) 做為 Symbolic/Concolic Exection Engine ，而 angr 底層又用到 SMT Solver [Z3](https://github.com/Z3Prover/z3)，雖然今年沒有教到 SMT Solver ( 在奇數年 QQ )，但有種東西都串在一起的感覺，希望之後能往這方面精進，而不只是用用別人寫好的工具罷了。

