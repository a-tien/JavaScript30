# Array Cardio

> 使用到的資料
```js
const people = [
    { name: 'Wes', year: 1988 },
    { name: 'Kait', year: 1986 },
    { name: 'Irv', year: 1970 },
    { name: 'Lux', year: 2015 }
];

const comments = [
    { text: 'Love this!', id: 523423 },
    { text: 'Super good', id: 823423 },
    { text: 'You are the best', id: 2039842 },
    { text: 'Ramen is my fav food ever', id: 123523 },
    { text: 'Nice Nice Nice!', id: 542328 }
];
```

## JS Array.property.some()
> 判斷是否有至少一個人大於十九歲
```JS
const someAge = people.some(person => (new Date()).getFullYear() - person.year >= 19);
// Output: True
```
## JS Array.property.every()
> 判斷是否全部人都大於十九歲
```JS
const everyAge = people.every(person => (new Date()).getFullYear() - person.year >= 19);
// Output: False
```
## JS Array.property.find()
> 尋找ID為823423的人的資訊
```JS
const findID = comments.find(comment => comment.id === 823423);
// Output: {text: 'Super good', id: 823423}
```
## JS Array.property.findIndex()
> 尋找ID為823423的人的Index
```JS
    const index = comments.findIndex(comment => comment.id === 823423);
// Output: 1
```
## JS Array.property.splice()
> 用Index分割陣列
```JS
const newComments = [
  ...comments.splice(0, index),
  ...comments.splice(index + 1),
]
```
