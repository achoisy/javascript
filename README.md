# Javascript Cheat Sheet ES6

Cheat sheet collection of ES6 helpers and other usefull javascript stuff

#### Table of Contents
1. Regular Array Helpers : *returns array or array element*
* [The 'forEach' Helper](#forEach)
* [The 'map' Helper](#map)
* [The 'filter' Helper](#filter)
* [The 'find' Helper](#find)

2. Condensing Array Helpers : *returns boolean or value*
* [The 'every' Helper](#every)
* [The 'some' Helper](#some)
* [The 'reduce' Helper](#reduce)
#
#### 1.1. The 'forEach' Helper [:link:](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/forEach)
The ```forEach()``` method executes a provided function once for each array element. 
```javascript
function handlePosts() {
const posts = [
{ id: 23, title: 'Daily JS News' },
{ id: 52, title: 'Code Refactor City' },
{ id: 105, title: 'The Brightest Ruby' }
];
posts.forEach(function (post){
savePost(post);
});
}
// Execute the function for each elements of array
```
#### 1.2. The 'map' Helper
Iterates

