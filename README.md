# Javascript Cheat Sheet ES6 
Cheat sheet collection of ES6 helpers and other usefull javascript stuff

## Table of Contents
1. Regular Array Helpers : *returns array or array element*
[The 'forEach' Helper](#forEach)
  [The 'map' Helper](#map)
  [The 'filter' Helper](#filter)
  [The 'find' Helper](#find)

2. Condensing Array Helpers : *returns boolean or value*
##### 1.5 [The 'every' Helper](#every)
##### 1.5 [The 'some' Helper](#some)
##### 1.5 [The 'reduce' Helper](#reduce)


<a name="forEach"></a>
### 1.1 The 'forEach' Helper [forEach]
Iterates the array without any way to stop
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


