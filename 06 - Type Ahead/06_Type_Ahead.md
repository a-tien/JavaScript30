# Type Ahead

## JS match()
當給定的兩個值有相符的時候會回傳1
```js
return place.city.match(regex) || place.state.match(regex);
```

## JS RegExp()
為了大小寫跟在字中的字元都可以偵測到所以用了正規語言的`g`->global(偵測字串中的字元)跟`i`->case-insensitive(大小寫都偵測)
```js
const regex = new RegExp(this.value, 'gi');
```

## JS replace()
```js
const cityName = place.city.replace(regex, `<span class="hl">${this.value}</span>`)
```
```html
<span class="name">
  <span class="hl">n</span>
  ew York, New YorK
</span>
```

## JS EventListener (input)
使用到了
`change`: 輸入完會觸發, 
`keyup`: 只要有輸入就會觸發
```js
searchInput.addEventListener('keyup',displayMatches)
searchInput.addEventListener('change',displayMatches)
```