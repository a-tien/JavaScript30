# CSS Variables & JS
## CSS Variables

### 建立變數: 利用兩個減號`--`
> 放在`:root`裡面便可以變成全域變數
```CSS
:root {
  --base: #ffc600;
  --spacing: 10px;
  --blur: 10px;
}
```

### 套用變數: 利用`var()`
```CSS
img {
  padding: var(--spacing);
  background: var(--base);
  filter: blur(var(--blur));
}
```


## JS style.setProperty()
```JavaScript
document.documentElement.style.setProperty(`--${this.name}`, this.value + suffix);
```
假設輸入為
`style.setProperty('padding', '15px');`
也等同於cssPropertyName
`style.padding = '15px';`

## JS this.dataset
存有所有data的元素，在這裡的`this.dataset.sizing`指的是`data-sizing`，所以可以以`data-[自己命名]`來增加dataset的元素

參考
https://ithelp.ithome.com.tw/articles/10199771?sc=pt