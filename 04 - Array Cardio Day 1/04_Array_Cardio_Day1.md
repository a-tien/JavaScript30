# JS Array Cardio

## filter
當return為True的時候會將元素存到陣列裡
```JavaScript
const fifteen = inventors.filter((inventor) => {
    if(inventor.year >= 1500 && inventor.year < 1600) {
      return true;
    }
  }) 
```

也等於
```JavaScript
const fifteen = inventors.filter((inventor) => inventor.year >= 1500 && inventor.year < 1600)
```

## map
會將return的元素存到陣列裡
```JavaScript
const fullName = inventors.map((inventor) => `${inventor.first} ${inventor.last}`)
```

## sort
由小到大的順序
```JavaScript
const arr = [5, 9, 1, 3, 2, 6];

arr.sort(function(a, b) { // a為第二個元素, b為第一個
  if(a > b) {
    return 1;
  } else {
    return -1
  }
});
// output: [1, 2, 3, 5, 6, 9]
```
```JavaScript
const sortDate = inventors.sort((a, b) => a.year > b.year ? 1 : -1)
```


## reduce
與map, filter不同之處: 回傳一個值，而非陣列
```JavaScript
const data = ['car', 'car', 'truck', 'truck', 'bike', 'walk', 'car', 'van', 'bike', 'walk', 'car', 'van', 'car', 'truck' ];
const transportation = data.reduce((obj, item) => {
  if (!obj[item]) {
    obj[item] = 0;
  }
  obj[item]++;
  return obj;
}, {});
```
函式後面的值{}為obj的預設值, item為data的元素

參考
https://ithelp.ithome.com.tw/articles/10225733