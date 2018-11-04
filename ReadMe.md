前言
------
在架站前兩、三天(18~20日)我正在嘗試使用Java進行爬蟲，從0開始摸索一直到學會了基本用法後，直接把所學全部運用在挑戰將[學校](https://www.nqu.edu.tw/)網站的公告抓取下來，再搭配自己突發其想的Filter功能，實現了搜尋處室以及標題內容。

20日下午突然想到隔一天需要考英文單字，於是我利用了一個下午的時間做了英漢字典的爬蟲程式，我只需要將單字表放入就能跑出我要的翻譯，做完的當下真的很想和人分享，但苦於自己平常都沒有經營的blog，於是就有了這個網站。

Jekyll + Github Pages 
---------------------
眾所周知**Jekyll**和**Github**最匹配，也由此選定架站的第一人選。  
Jekyll是很強大的**STATIC SITE GENERATOR**，但也因為只是Static所以網頁只能是靜態網頁...  
再加上Jekyll是由Ruby而生，但我沒有學過Ruby，應該說我不會任何Back-end語言，所以只能放在Github Pages裡。

Jekyll Plugins
--------------
Jekyll有許多的Plugins可以使用，並且也可以自己寫插件，但是有些插件是不被允許在Github上的。  
因此我使用了第三方編譯網站[Codeship](https://codeship.com/)繞開Github。

#### 網站使用的Plugins
* Jekyll-Archives
* Jekyll-sitemap

#### CodeShip
利用Codeship來處理Jekyll-Archives的編譯，先Push到Master後再由Codeship端Pull下來，經過一系列的編譯再Push到gh-pages這個branch裡。  
然而不知道為什麼若將網站預設資源設定gh-pages，網站不會自動編譯，必須先設定Master再轉gh-pages他才會建立...
