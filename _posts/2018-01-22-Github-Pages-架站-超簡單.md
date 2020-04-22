---
title: "史上最簡單 Github Pages 架站法"
date: 2018-01-22T00:00:00-00:00
categories:
  - Web
tags:
  - Github
  - GitHub Pages
---

### 本篇文章適用的人
* 想在Github Pages建立部落格的人
* 不熟悉也不想使用指令輸入器的人
* Windows使用者
* 從來沒聽過Jekyll、Bash、gem等的人

### 我發生了什麼事
我手上的兩台電腦，一台桌上型電腦，一台筆記型電腦，都是Windows系統。在我看過Github Pages所建立的網站後，十分興奮地著手建立我自己的部落格。  

首先在Github Pages的解說中，也建議使用[Jekyll](http://jekyllcn.com/)，接著進入Jekyll網站後，隨著它的教學我越陷越深，越來越多我不了解的東西，灌了越來越多的工具包含Ruby、ubuntu等，並且十常出現許多相容性的問題。  

當時我的想法是，這不是號稱很簡單的架站系統，怎麼變得如此複雜？而且說實在我跟隨著許多文章的步驟卻不清楚他們的目的是什麼。後來我發現，原來這些動作都只為了一個目的：  
* 本機預覽網站


這些工具，能讓你在發布網站前能預覽自己的網站，但對我而言，投入的時間與精力，已超越它的收穫了。因此後來我毅然決然放棄。  

所以，如果你跟我一樣，只是想要簡單的架站，不在乎本機預覽的功能，其實你可以直接跳過這些步驟，依然能有個漂亮的Github Pages部落格。


### 該如何有個Github Pages
---
#### 三大步驟
1. 註冊[Github](https://github.com/join?source=header-home)會員
2. 選擇[Jekyll](http://jekyllthemes.org/)樣板（不需安裝任何東西）
3. 設定

沒錯事實上只需要這三步，就能完成你的Github Pages的部落格，就是這麼簡單。

接下來，我從第二步驟開始解說吧，註冊會員這種東西，就交給聰明的各位處理了。
<!-- more -->

### 選擇樣板
---
這一個步驟非常簡單，你只要去[Jekyll樣板](http://jekyllthemes.org/)網站，選個漂亮的樣板，接著將樣板Fork至自己的Github裡面就好了。

如果是打包好的zip擋，也是將他們完整上傳至自己建立好的分支即可。

如果你不是很確定這怎麼做，請參考以下步驟：

* 選好樣板後，進入該樣板的github頁面（點選樣板頁的homepage）

![template]({{ site.baseurl }}/assets/images/2018/01/2018012202.png)

* 進入以後，將該樣板fork至自己的github

![fork]({{ site.baseurl }}/assets/images/2018/01/2018012203.png)

* 在自己github會看見剛建立的專案（在github上稱為repository）
Alomahuang/hanuman 斜線前面是你的github名稱 斜線後面則是剛剛樣板repo的名稱

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012204.png)

#### 基本上這就完成了，接下來就是設定的問題了。

如果你是使用下載方式的，你的步驟則是在自己github頁面先建立一個repository，命名的話建議取Blog或是BlogSite之類的，因為你的網址與這個有關，以我的例子來說，我Blog的網址就是：alomahuang.github.io/**Blog**/。

---
### 設定
設定主要是要調整setting，以及對repo裡的config做修改。

#### 調整setting
在這裡，最重要的是改名字，因為這將會影響你的網址。

* 在建立好的repo裡面點選設定（setting）

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012205.png)

* 將名字改成你想要的（我的名字原本是Type-on-Strap，我將它改為Blog）

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012206.png)

#### 調整default branch

一般來說有兩個主要使用的branch：master, gh-pages。以我們不使用本機端預覽的模式，其實使用哪一個皆無所謂。
不過我還是將我的預設分支設定為gh-pages分支，方法如下。

兩個地方需要做設定：

* 第一個是Settings->Branches

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012207.png)

* 第二個是Settings->Options（請拉到下面）

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012208.png)


### 修改config
---
最後一步也是最重要的一步，就是修改你的_config.yml檔案，這是攸關勝負的一戰不可忽略！

* 在正確的分支下（你預設為default的分支）選擇_config.yml擋

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012209.png)

* 按下編輯按鈕（右上方）

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012210.png)

#### 主要修改內容
* baseurl
將裡面的內容取代為你的repo的名字，以我的例子來說就是Blog，記得前面可能要加斜線。
```
baseurl: "/Blog"
```
* url
將url改成你的網址（通常是 https://你的帳號.github.io)
```
url: "https://alomahuang.github.io"
```
最重要的就這兩個啦，其他個人化項目請自行設定。

* 最後commit（記得標題要寫才能commit）

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012211.png)

#### 原則上完成啦！網址可以去Settings->Options下面確認喔。

![myrepo]({{ site.baseurl }}/assets/images/2018/01/2018012212.png)



