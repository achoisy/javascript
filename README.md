# Javascript Cheat Sheet ES6

Cheat sheet collection of ES6 helpers and other usefull javascript stuff

#### Table of Contents
##### 1. Regular Array Helpers : *returns array or array element*
1.  [The 'forEach' Helper](#forEach)
1. [The 'map' Helper](#map)
1. [The 'filter' Helper](#filter)
1. [The 'find' Helper](#find)

##### 2. Condensing Array Helpers : *returns boolean or value*
1. [The 'every' Helper](#every)
1. [The 'some' Helper](#some)
1. [The 'reduce' Helper](#reduce)
#

### 1. Regular Array Helpers
<a name="forEach"></a>
#### 1.1. The 'forEach' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
The ```forEach()``` method executes a provided function once for each array element. 
```javascript
const posts = [
    { id: 23, title: 'Daily JS News' },
    { id: 52, title: 'Code Refactor City' },
    { id: 105, title: 'The Brightest Ruby' }
];

posts.forEach((post) => {
    console.log(post.title);
});

// expected output:
//      Daily JS News
//      Code Refactor City
//      The Brightest Ruby
```

<a name="map"></a>
#### 1.2. The 'map' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map)
The ```map()``` method creates a new array with the results of calling a provided function on every element in the calling array.
```javascript
const images = [
    { height: '34px', width: '39px' },
    { height: '54px', width: '19px' },
    { height: '83px', width: '75px' },
];

const heights = images.map( (image) => {
    return image.height; // "return' is mandatory !!
});

console.log(heights);
// expected output: heights = ['34px','54px','83px'] 
```

<a name="filter"></a>
#### 1.3. The 'filter' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/filter)
The ```filter()``` method creates a new array with all elements that pass the test implemented by the provided function.

```javascript
const numbers = [15, 25, 35, 45, 55, 65, 75, 85, 95];

const filteredNumbers = numbers.filter((number) => {
    return number > 50; // "return' is mandatory !!
});

console.log(filteredNumbers);
// expected output: [55,65,75,85,95]
```

<a name="find"></a>
#### 1.4. the 'find' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/find)
The ```find()``` method returns the value of the first element in the array that satisfies the provided testing function. Otherwise *undefined* is returned.
```javascript
const users = [
    { id: 1, admin: false },
    { id: 2, admin: false },
    { id: 3, admin: true},
    { id: 4, admin: true},
];

const admin = users.find(user => user.admin);

console.log(admin);
// expected output: { id: 3, admin: true}
```
#
### 2. Condensing Array Helpers
<a name="every"></a>
#### 2.1. The 'every' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/every)
The ```every()``` method tests whether all elements in the array pass the test implemented by the provided function.
```javascript
const users = [
    { id: 21, hasSubmitted: true },
    { id: 62, hasSubmitted: false },
    { id: 4, hasSubmitted: true },
];

const hasSubmitted = users.every(user => user.hasSubmitted);

console.log(hasSubmitted);
// expected output: 'false'
```

<a name="some"></a>
#### 2.2. The 'some' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/some)
The ```some()``` method tests whether at least one element in the array passes the test implemented by the provided function.
```javascript
const requests = [
    { url: '/photos', status: 'complete' },
    { url: '/albums', status: 'pending' },
    { url: '/users', status: 'failed' },
];
const inProgress= requests.some(request => request.status === 'pending');

console.log(inProgress);
// expected output: 'true'
```

<a name="reduce"></a>
#### 2.3. The 'reduce' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)
The ```reduce()``` method applies a function against an accumulator and each element in the array (from left to right) to reduce it to a single value.
```javascript
const desks = [
    { type: 'sitting' },
    { type: 'standing' },
    { type: 'sitting' },
    { type: 'sitting' },
    { type: 'standing' }
];

const deskTypes = desks.reduce(function(previous, desk) {
    if (desk.type === 'sitting') {previous.sitting++}
    if (desk.type === 'standing') {previous.standing++}
    return previous;
}, { sitting: 0, standing: 0 });

console.log(deskTypes);
// expected output: {"sitting":3,"standing":2}
```


(c) Alexandre Choisy
