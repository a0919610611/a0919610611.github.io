---
title: 用 Terminal 上 PTT 裝逼，自動登入 + 自定熱鍵
tags:
    - PTT
    - terminal
    - expect
---
# 你還在用 PCMAN , Welly 上 PTT 嘛 ?
雖然現在 PTT 可以使用瀏覽器觀看了，但生為一個 geek ，怎麼可以用跑在 browser 的 javascript 來看 PTT 呢 ？
當然是使用 Native App 的方式呀 ~
但 Linux 沒有 R QQ (雖然我現在都用 MAC XDDDDD)
但還有更能裝逼的方法，就是使用 Terminal ( 終端機 ) 來上 PTT ，來張圖片吧 ![-w1085](/images/15312945333373.jpg)

看～ 這是不是整個逼格都出來了 ？ 
# 那 ... 要怎麼做呢 ？
1. 打開你的 Terminal ( MAC / Linux ) ，Windows 可以使用 Ubuntu On Windows
2. 有兩種方法可以上 PTT ，推薦使用 ssh 的方法，比較安全

    ```bash
    telent ptt.cc 23
    ssh bbsu@ptt.cc
    ```
3. 再來就可以像平常一樣使用 PTT 摟

# 好難用喔 ~
第一次使用這種方法，一定會覺得好難用喔 ~ 筆者當初也是從 Windows 跳到 MAC ，在沒有 PCMAN 的情況下，使用 termianl ，但 PCMAN 有許多功能在 terminal 上都沒辦法用了，像是自動登入、自定義熱鍵等，用起來沒有以前那麼順暢，八卦版都逛不下去了呢 QQ
# Expect Script
後來得知 有 Expect Script 這個好用的東西，那是拿來做啥的呢 ? [WIKI - Expect](https://en.wikipedia.org/wiki/Expect)
簡單來說就是能利用 expect 這隻程式當做中間人幫我們和其他程式互動，而就可利用這個特性，完成 PTT 的自動化操作。
