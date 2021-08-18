# Ramen-Map-in-Taiwan

## 研究動機
```javascript
身為兩個喜歡吃拉麵的人，我們設計出這款拉麵地圖，希望可以幫助使用者選擇想吃的拉麵店。
我們透過讓使用者輸入縣市、星星數目、店家評論數，拉麵地圖會一步一步帶領使用者找到最想去的拉麵店。
在幫助使用者選擇店家的同時，拉麵地圖也蘊含我們熱愛拉麵的心意！
```

## PART1: 拉麵地圖

```javascript
[介紹] 採模擬方式step by step 帶領讀者找到心目中的拉麵店 ☺
```

```javascript
❶ 讀取我們的拉麵資料並印出數據內容

❷ 在地圖上標示出拉麵資料中所有樣本點的座標

❸ 使用者可以自由地輸入縣市，地圖會據使用者的輸入，顯示在此縣市中所有拉麵店的座標

❹ 在地圖上顯示框線，將區域中所有的拉麵店框住，讓使用者可以更明確地看出拉麵店的涵蓋範圍

❺ 使用者可以輸入最低標準的星號數目與希望獲取的店家數，系統會按照使用者的輸入，隨機選取店家並印出店家的地址

❻ 使用者根據前項結果提供的編號，選取最想前往的店家，系統會在地圖上顯示該拉麵店的座標！
```

## PART2: 拉麵地圖2.0

```javascript
[介紹] 除了區域及星星數，額外加上利用腹地畫出拉麵店的重點吸客範圍的功能。 
(星星越多的店家會吸引更遠距離的顧客造訪，或是顧客在附近遊玩時，前往用餐的可能性也會較高，同時，腹地重疊的部分代表是拉麵的精華地區！在範圍之內的使用者們可以說是非常的幸福，周圍有很多很棒的拉麵店！）
```

```javascript
[使用步驟]
在拉桿上選取星星數目的範圍--> 選取想去的縣市 --> 載入自己喜歡的配色
* 建議使用時可以用放大功能放大標籤區域，可清楚看見腹地覆蓋範圍 *
```


## PART3: 拉麵數據分析
```javascript
❶ 利用長條圖顯示各縣市拉麵店數目的分差異
分析: 此處我們在縣市中增加了covid-19，是由於在查詢拉麵店資料時，我們發現許多店家因為不敵疫情摧殘，永久停業，熱愛拉麵的我們感到非常惋惜，便希望能夠藉由這張圖，同時顯示出疫情帶來的巨大衝擊。

❷ 利用折線圖顯示拉麵店星星數與評論數之關聯
分析: 在此之前，我們以為星星數越多的店家評論數應該也傾向越多，然而結果卻發現，星星數相對較少的店家，評論數也不少，所以兩者之間並未呈現完全的現象關係，我們推論這樣的結果是由於，很棒的店家大家理當會樂意上網藉由評論對店家進行肯定；而不好的店家，人們也會希望透過評論讓店家進行改進，或讓其他客人能夠有客觀的資料能夠參考。

❸ 利用點狀圖顯示拉麵店星星數、評論數與所在縣市的關係
分析: 根據此圖可以看出，星星數越多的店家討論度也傾向越高，同時可以看出討論度高的店家主要還是分佈在台北市。

❹ 利用此圖顯示各縣市，各種拉麵種類店家的比例
分析: 此圖能夠明確地看出各縣市，各種口味的拉麵店佔比，例如台中市綜合口味的店家佔了最多，但無法看出各種口味店家實際的數量差異，我們認為此圖適合想要一目了然得知各種口味佔比的時候！

❺ 利用熱圖顯示各縣市、各種類拉麵店家的數目，顏色越淺代表在該縣市該種口味的拉麵店越多
分析: 根據此圖，不僅能夠看出台北市烏龍麵/蕎麥麵的店家佔比最高，還能同時看出此種類店家數目超過7家。
```

## 結論: 

```javascript
- idea 由來: 
在我們查詢拉麵的資料時，偶然看見網路上有別人做好的一個拉麵地圖，地圖上會標出各個拉麵店家的座標。
考慮到民眾在選擇想吃的店家時，除了店家位置還會考慮店家在網路上的評價與評分，我們將這個拉麵地圖進行優化，
讓使用者可以選擇區域、星星數以及評論數，藉此帶領使用者一步步找到最想去的拉麵店！

- 文中指令(以下選兩個特殊指令來介紹): 
1. addMarkers(map, lng=x, lat=y, popup = info)=> 在拿到指定的經緯度後，在map上以arrow標示出位置。
2. addRectangles(map,
    lng1= xleft+a, lat1=ydown+a,
    lng2= xright-a, lat2=yup-a,
    fillColor = "transparent"
    )=> 做完資料探索後， 取出適當的邊界值，在map上建立特殊框。
3. shiny's application=> 架網站
    
-  使用到的packages:
readxl、dplyr、magrittr、leaflet、ggplot2、grid、tidyverse、knitr、shiny
```

## Show
[Ramen-Map Site](https://lala0803.shinyapps.io/ramen-map/)
![](https://github.com/la83la/Ramen-map-in-Taiwan/blob/main/螢幕快照%202021-08-18%20上午9.34.47.png)
