# JavaScript30 Day1

在Day1用到了
- eventTarget
- addEventListener
- querySelector
- Audio Method
- classList
- CSS transition
- 箭頭函式
- forEach
花了很多時間去學，但希望可以學會之後可以越來越快上手!!

```javascript
window.addEventListener('key', function(e){
        console.log(e)
    })
```

#### addEventListener
在這裡會用到keyCode，每個Event得到的值皆不同

```javascript
window.addEventListener('keydown', function(e){
        const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`)
        console.log(audio)
    })
```
利用指定的方式`audio[data-key="${e.keyCode}"]`找出對應keycode的audio值，會發現除了指定的按鍵其他會輸出null，所以用遇到Null回傳的方式跳出函式`if(!audio) return;`
#### querySelector
* 取id元素時:
document.querySelector('#title');
* 取class元素時:
document.querySelector('.title');
* 取標籤時:
document.querySelector('div');

#### Audio Method
今天用到play(), currentTime,其他audio用法可以看[W3S](https://www.w3schools.com/jsref/dom_obj_audio.asp)
####  Audio Play
在這裡用到了[audio.play()](https://www.w3schools.com/jsref/met_audio_play.asp)
```javascript
const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`)
// console.log => <audio data-key="70" src="sounds/openhat.wav"></audio>
audio.play();
```

#### Audio CurrentTime
實作方法也可以參考W3S，簡單來說就是決定聲音的起始時間點，所以可以放在play之前
`audio.currenTime = 0;`

#### JS classList
> 在JS中可以增加、移除
```javascript
//增加"red" class
tag.classList.add('red')
tag.addClass('red')
//移除"red" class
tag.classList.remove('red') 
//自動偵測是否帶有該class並做切換"red" class
tag.classList.toggle('red') 
//是否有包含"red" class 若有回傳"true" 反之，false。
tag.classList.contains('red')
```
#### CSS transition
```css
div {
  transition: width 2s, height 4s;
}
div {
  transition: all .07s ease;
}
```
#### 箭頭函式([參考網站](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript/Reference/Functions/Arrow_functions))
```
(參數1, 參數2, …, 參數N) => { 陳述式; }

(參數1, 參數2, …, 參數N) => 表示式;
// 等相同(參數1, 參數2, …, 參數N) => { return 表示式; }

// 只有一個參數時,括號才能不加:
(單一參數) => { 陳述式; }
單一參數 => { 陳述式; }

//若無參數，就一定要加括號:
() => { statements }
```
實作:

#### forEach
[這篇](https://realdennis.medium.com/array-%E5%8E%9F%E5%9E%8B%E7%9A%84-foreach-%E6%9C%89%E5%A4%9A%E5%A5%BD%E7%94%A8-%E5%AD%B8%E6%9C%83%E9%AB%98%E9%9A%8E%E5%87%BD%E6%95%B8%E4%B9%8B%E5%BE%8C%E9%83%BD%E4%B8%8D%E6%83%B3%E5%AF%AB-javascript-%E4%BB%A5%E5%A4%96%E7%9A%84%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80%E4%BA%86-dc4b594a045a)寫得很詳細!!還在消化中
**常見迴圈**
```javascript
for( let i = 0 ; i < arr.length ; i++ ){
 console.log(arr[i]);
}
```
**同樣結果用forEach**
```javascript
arr.forEach(item => console.log(item))
```
在callback會傳入三個參數給callback
- item
- index
- array

```javascript
const callback = (item,index) => {
 if(index%2===0) return;
 console.log(item);
}
[0,1,2,3,4,5,6,7].forEach(callback)
```


參考:
https://ithelp.ithome.com.tw/articles/10211605
https://medium.com/@egg8833/%E5%9C%A8js%E4%B8%AD%E8%BC%95%E9%AC%86%E5%A2%9E%E5%8A%A0-%E7%A7%BB%E9%99%A4class%E7%9A%84%E6%96%B9%E6%B3%95-classlist-eb3a686f8d4


