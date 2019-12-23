# Software Studio 2018 Spring Assignment 01 Web Canvas

## Web Canvas
<img src="example01.gif" width="700px" height="500px"></img>

## Todo
1. **Fork the repo ,remove fork relationship and change project visibility to public.**
2. Create your own web page with HTML5 canvas element where we can draw somethings.
3. Beautify appearance (CSS).
4. Design user interaction widgets and control tools for custom setting or editing (JavaScript).
5. **Commit to "your" project repository and deploy to Gitlab page.**
6. **Describing the functions of your canvas in REABME.md**

## Scoring (Check detailed requirments via iLMS)

| **Item**                                         | **Score** |
| :----------------------------------------------: | :-------: |
| Basic components                                 | 60%       |
| Advance tools                                    | 35%       |
| Appearance (subjective)                          | 5%        |
| Other useful widgets (**describe on README.md**) | 1~10%     |

## Reminder
* Do not make any change to our root project repository.
* Deploy your web page to Gitlab page, and ensure it works correctly.
    * **Your main page should be named as ```index.html```**
    * **URL should be : https://[studentID].gitlab.io/AS_01_WebCanvas**
* You should also upload all source code to iLMS.
    * .html or .htm, .css, .js, etc.
    * source files
* **Deadline: 2018/04/05 23:59 (commit time)**
    * Delay will get 0 point (no reason)
    * Copy will get 0 point
    * "屍體" and 404 is not allowed

---

## Put your report below here
### 基本功能
#### 畫筆、橡皮擦
1. 大家應該都寫得差不多ＸＤ就不多做贅述了
#### 選顏色
1. 使用jscolor然後讀取字串，在最前面加上'#'並丟入畫筆顏色
#### cursor
1. 我的cursor使用的圖片跟功能表的圖片一樣
2. 在選工具的function內設定cursor，並將圖片丟進去即可
#### 工具列
1. 就是在html裡面load圖片上去，並新增onclick，呼叫選擇工具的function
2. 選擇工具的function是用switch的方式寫成的，當我選定什麼tool就會呼叫那個tool所需的function
#### 線條、圓圈、三角形、正方形
1. 其實寫法跟畫筆差不多，但需要多考慮一點就是他會隨著你的游標移動，所以要一直重新load
2. 因此我寫了async/await，確保我load完後再蓋上前一層的圖
3. 直到我教滑鼠放開才會將圖push上去
#### 打字、改變字體/大小
1. 首先要使用createElement在canvas上新增一個input
2. 我寫了按下Enter鍵之後，外框會不見，並且一次只能新增一個
3. 改變字體以及大小就是在html裡面寫了select選單，再把值丟進ctx.font裡即可改變
#### restart
1. 我用了偷吃步的方法，就是重新把canvas畫成白色
#### upload/download
1. download使用了createElement，然後將圖片名稱預設成mysketch.png
2. upload在html裡面要用file這個東西
#### undo/redo
1. 其實概念跟畫圖很像，但是每一步都要push進去array

### 額外功能
#### 不同畫筆
1. 我新增了彩虹畫筆、暈染畫筆、還有網狀畫筆
2. 我是用hue來寫，然後一直++，直到hue=360時，下一步將hue=0，如此一來就會一直重複那個色相環
3. 暈染畫筆就是新增shadowBlur就可以了
4. 網狀畫筆是我上網查的ＸＤ
#### bucket
1. 簡而言之就是將畫布塗滿顏色！
#### 工具列變色
1. 使用一個funtion，當我每次hover到或是click時，就改變btn顏色

###點我的頭像有彩蛋ㄛ！
