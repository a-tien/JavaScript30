# Fun with HTML5 Canvas

## 2D Canvas
```js
const canvas = document.querySelector('#draw');
const ctx = canvas.getContext('2d');
```
> 預設Canvas大小
```js
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;
```

## line設定
```js
ctx.lineJoin = 'round'; //轉角會比較圓潤
ctx.lineCap = 'round';  //線頭線尾圓潤
ctx.lineWidth = 100;    // 線寬
ctx.strokeStyle = `hsl(${hue}, 100%, 50%)`; // 線條顏色
```

## 線的開始到結束
```js
ctx.beginPath(); // start
ctx.moveTo(lastX, lastY); // start point
ctx.lineTo(e.offsetX, e.offsetY); // end point
ctx.stroke(); // complete the line
```




