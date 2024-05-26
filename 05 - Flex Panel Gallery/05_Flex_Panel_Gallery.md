# Flex Panel Gallery
## JS toggle
因為想要點擊第一次時有效果，第二次消除效果，這個時候用toggle的話剛好可以達到一樣的效果
```JS
const panels = document.querySelectorAll('.panel');
function toggleOpen() {
  this.classList.toggle('open');
}
```
- 點擊第一次時: 因為沒有open的元素，所以class變'.panel open'
- 點擊第二次時: 有open的元素，所以class變回'.panel'

## CSS flex
`flex`為下面三個的簡寫
- `flex-grow`: 分配空間伸展比例，1為均分
- `flex-shrink`: 分配空間壓縮比例
- `flex-basis`: 子元素的基本大小

- flex-grow: 無單位數字
`flex: 2`

- flex-basis: 寬度/高度
```CSS
flex: 10em;
flex: 30px;
flex: min-content;
```

- 雙值: flex-grow | flex-basis
`flex: 1 30px;`

- 雙值: flex-grow | flex-shrink
`flex: 2 2;`

- 三值: flex-grow | flex-shrink | flex-basis
flex: 2 2 10%;

## CSS child
`:nth-child(n)`: 第n個child
`:first-child`: 第一個child
`:last-child`: 最後一個child
`> *`: 全部的child

參考
https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-grow