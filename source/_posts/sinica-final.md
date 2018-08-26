---
title: 中研院 資訊所 暑期實習 總結
categories: 中研院
tag:
  - 暑期實習
  - 中研院
  - Blockchain
  - Ethereum
  - IPFS
date: 2018-08-26 18:28:24
tags:
---

# 實習心得總結
因為後面幾個禮拜都在寫 code，也沒啥心得好寫，剛好中研院要求要寫心得，我就在這篇文一起寫吧，賺!
# Proof Of Concept
最後做出了一個 Prototype ， 基本上就是把之前那篇 paper 「[Decentralizing Privacy: Using Blockchain to Protect Personal Data](https://ieeexplore.ieee.org/document/7163223/)」的架構給實作出來。還撰寫了一個簡易的前端可以輕易的操作智能合約。
## 前端
使用 React 當做前端的 Framework ， 使用 [web3.js](https://github.com/ethereum/web3.js/) 和 Ethereum 溝通、[Metamask](https://metamask.io/)管理 User 的 Ethereum Account、 [js-ipfs-api](https://github.com/ipfs/js-ipfs-api)和 IPFS 溝通。

好險在來實習之前我就已經有用 React 寫過複雜網頁 ([Formosa OJ - 交大的 Online judge](https://oj.nctu.me/))，就把code 直接拿過來改成符合系統的需求，所以 UX 基本沒有什麼問題，時間都花在 UI 還有和 Ethereum、IPFS 溝通上。 

## Ethereum
基本上就是寫好 Smart Contract deploy 上去就好了，依靠Blockchain 幫我們達到 Decentralized 、 Integrity 、 Non-repudiation。

但 Ethereum 有個缺點就是每個 block 是有大小上限的而且不大，所以要寫大量資料上去的話，只能分成好幾個 block ，然後一個 block 被挖到又要幾十秒，花費的時間太高，沒辦法忍受。 

## IPFS
為了解決寫入大量資料的問題、同時保持前面提到的幾個性質(Decentralized 、 Integrity)，所以決定使用分散式的檔案系統來解決，當成 off-chain storage。

### Ethereum Swarm vs IPFS
其實 Ethereum 自己也有提出一個和 IPFS 的東西，叫做 「 swarm 」(大家都好喜歡用 swarm 阿)。這邊有Ethereum官方寫的比較 [IPFS & SWARM](https://github.com/ethereum/go-ethereum/wiki/IPFS-&-SWARM)。

因為我只是要 storage ，所以我選擇了 IPFS ，且 IPFS 文件、教學、各種語言的 Binding API 也比較多。

### 使用 IPFS
有了 IPFS 之後，就不用擔心資料量太大的問題，只要把資料寫到 IPFS 上，再把IPFS URL(是文件的 uuid，基於文件內容算出來的，不用擔心URL指到的檔案被竄改)記錄在 smart contract上，也就同等於把資料記在 Blockchain 上了。

### 額外的努力
因為多了 IPFS，所以變成每個節點除了Ethereum node 外，都還需要 IPFS node，增加了建置的成本、時間。 但也因此有了更多的可能性，不然寫大量資料到 Ethereum 上不但要大量時間、還要大量的手續費(gas)，根本無法在 production 環境實用，最後也只能淪為玩具。  

# 累積的重要
整個系統從零到現在，大概花了三個星期吧，但全是因為在實習前，我就完過這些東西了，不然一個沒有基礎的人可能要花好幾倍的時間。

所以平常一些看起來沒有什麼用的能力，真的是不知道什麼時候會派上用場呀 ! 所以到處嘗試一不同的技術也是很重要的，不知什麼時候點連成了線，一個系統就被你做出來了 XD


# 心得
大學的前幾個暑假幾乎都在忙演算法競賽，社團的暑訓、比賽的準備練習之類的，而今年也決定退役，好好準備開始搞研究，但閒暇之餘還是參加 CTF、解解演算法題目。實作能力已經有了足夠的鍛鍊，但研究能力還是有所欠缺。 以除了大學裡面的畢業專題，決定暑假來中研院實習，看看一個研究機構裡，PI、博後們是如何做研究的，希望可以學習、效法，增進自己的研究能力。

從讀 paper、討論想法、找出要解決的問題、要如何解決、評估解決方法等，每一項都是非常重要的過程。 這次的研究主題是「區塊鏈於隱私透明化上之應用」，重點是要保障用戶的隱私，但同時要公開透明，說起來沒什麼，但真的要實現就有不少問題需要去解決了。 因為區塊鏈是公開透明且任何人都可以查看的，但同時又要保障用戶隱私、不會洩漏多餘的資料，這時就需要密碼學的幫忙。 好在我在學校修了不少密碼學相關的課(密碼學概論、橢圓曲線密碼學等)，對於如何把相關的加密、雜湊算法結合進我們系統都不會太過困難。

這次我們的系統是參考一篇 MIT 發的 paper 「Decentralizing Privacy: Using Blockchain to Protect Personal Data」，但系統的設計不只是只有紙上談兵，看看 paper 而已，因為 paper 往往會省略很多細節是我們實作時才會遇到的，例如: 使用者體驗、Workflow等都要考慮。這次實作時也有碰到原先設計的演算法效率太低，但經過小小的修改，結果演算法、資料結構相關的知識，成功的把演算法的時間複雜度壓了一個 log，也是沒有白費打了這麼久的競賽呀 XD，要用時還是派的上用場的。

最後經過每個禮拜的討論、功能需求、系統架構也逐漸的清晰明瞭，中間也不斷的溝通、改架構，而寫 code 是裡面比較容易的部份。 最後也成功的實作出了一個可以用的系統，且有個簡單的網頁 UI 可以 demo。

除了實作系統、寫 code 以外，撰寫說明文件也是很重要的，之後系統會交給其他人繼續撰寫、維護，所以需要有良好的文件可以幫助之後要開發這個系統的人員可以快速了解系統的架構、用到的套件等等。 

這次實習除了在中研院做 project，也有到台大上中研院開的「邏輯、語言與計算」暑期研習營 (FLOLAC)，上了很多現在台灣的大學資工系不會教的東西，也因此發掘了很多以往所沒接觸過的領域。雖然只有短短兩個禮拜共十天，課程也不容易，但卻學到很多東西。也感嘆台灣的資工系現在連「程式語言」這種對計算機科學根基很重要的課程都不開了。

總體來說，這次的實習非常的充實，扣掉中間去美國參加 DEFCON 一個禮拜，每天都有很多事可以做，為了完成一個特定目標，四處去找 paper 、 tutorial 、別人心得來讀，而加以統整內化，之後用在自己的系統之中，站在巨人的肩膀之上，更前進一步，或許這就是研究的意義吧 ! 
