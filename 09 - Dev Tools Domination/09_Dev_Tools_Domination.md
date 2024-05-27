# Dev Tools

```js
// Regular
console.log('hi');

// Interpolated
console.log('Hello %s!', '🌏') // Hello 🌏

// Styled
console.log('%c Style text', 'font-size:30px; text-shadow: 5px 5px blue; background: yellow;')

// warning!
console.warn('Warning!!!!!!!!')

// Error :|
console.error('Error!!!!!!!!')

// Info
console.info('This is information');

// Testing
const p = document.querySelector('p');

console.assert(p.classList.contains('ouch'), 'This is wrong!!!');

// clearing
console.clear()

// Viewing DOM Elements
console.log(p);
console.dir(p);

// Grouping together
// from console.group() to console.groupEnd()
dogs.forEach(dog => {
    console.group(`${dog.name}`);
    console.log(`This is ${dog.name}`);
    console.log(`${dog.name} is ${dog.age} years old`);
    console.groupEnd(`${dog.name}`);
})

// counting
console.count('qq') //qq: 1
console.count('pp') //pp: 1
console.count('qq') //qq: 2
console.count('pp') //pp: 2
console.count('pp') //pp: 3
console.count('qq') //qq: 3
console.count('qq') //qq: 4

// timing
// from console.time() to console.timeEnd()
console.time('fetching data')
fetch('https://api.github.com/users/a-tien')
    .then(data => data.json())
    .then(data => {
        console.timeEnd('fetching data');
        console.log(data);
    })
// fetching data: 646.559814453125 ms
```