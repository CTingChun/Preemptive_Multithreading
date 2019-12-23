# Operating System 2019 Spring Checkpoint 02

## Preemptive Multithreading
For this programming project checkpoint, you are to write a preemptive multithreading
package and a test case based on the single-buffer producer-consumer example.
Preemptive multithreading means the code for each thread does not need to explicitly do a
thread-yield in order to switch to another thread, if any. Of course, it can also do ThreadYield() if it wants.
Depending on your implementation, you may or may not use a separate thread for the
thread manager. If so, then you may want to define your MAXTHREADS accordingly. All
other API should be the same. Actually, the ThreadYield() function should be available
for preemptive threads, too, because even though the OS can always preempt a thread, a
thread should still be able to voluntarily give up control.

## Todo
1. **Turn in the source files for preemptive multithreading to be compiled using SDCC and targets EdSim51.**
2. testpreempt.c , which contains the startup code and sets up the producer-consumer example.
3. preemptive.c , preemptive.h , which contains the cooperative multithreading code.

## Scoring (Check detailed requirments via iLMS)

| **Item**                                         | **Score** |
| :----------------------------------------------: | :-------: |
| testpreempt.c                                    | 25%       |
| preemptive.c                                     | 55%       |
| Typescript for compilation                        | 2%        |
| Screenshots and explanation                      | 18%       |


## Report below here
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
