# CheckBox

## CheckBox checked
> 設定打勾的方式
```js
const checkboxes = document.querySelectorAll('.inbox input[type="checkbox"]')
// checkboxes.forEach(checkbox) = <input type="checkbox">
checkbox.checked = true //check!
```

## KeyboardEvent: shiftKey
>keyboard event可以判斷是否有按著shift鍵

判斷`e.shiftKey`的真偽值

** forEach要記得加分號(;)