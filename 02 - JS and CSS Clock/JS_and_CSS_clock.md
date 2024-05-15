# JavaScript30 Day2
## CSS transform
- `transform-origin: 100%`: 旋轉的原點，在這裡設為100%在正中央
- `transform: rotate(90deg)`: 因為預設的線角度為向左的平面，想要讓他在朝向上方所以將預設旋轉角度設為90
## CSS transition
- `transition: all 0.05s`: 讓全部都有動態，然後執行時間為0.05s
- `transition-timing-function: cubic-bezier()`: 可以自己設定動態的點
## JS setInterval
定義: 固定延遲一個時間後才去執行程式且不斷循環。

> scope.setInterval(code, delay);
- `setInterval(function(), 1000)`: 在這裡1000是指每秒

跟setTimeout()的不同在，setTimeout()為執行「一次」而setInterval()為「不斷循環」([參考](https://kuro.tw/posts/2019/02/23/%E8%AB%87%E8%AB%87-JavaScript-%E7%9A%84-setTimeout-%E8%88%87-setInterval/))

## JS style
可以用
``secondHand.style.transform = `rotate(${secondsDegrees}deg)` ``:這裡的secondHand是class名稱