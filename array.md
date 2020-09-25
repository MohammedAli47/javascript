# Array Methods :

### 1- Array.prototype.concat(arr1, arr2, ..., arrX) :

Joins two or more arrays and returns a copy of the new array.

**Doesn't mutate**.
___
### 2- Array.prototype.entries( ) :

Returns an array iterator object with key/value pairs.

**Doesn't mutate**.
___
### 3- Array.prototype.every(func, thisValue) :

Takes a function as a callback and applies it to every item in the array.

If at least one item returns `false`, `every()` returns `false`.

If all items return `true`, `every()` returns `true`.

>thisValue ( Optional ) : specifies the function's `this` value. If it's not passed, `this` is returned as `undefined`.

**Doesn't mutate**.
___
### 4- Array.prototype.fill(value, start, end) :

Fills the specified static value inside the array 

>start ( Optional ) : The index to start filling from.
>
>end ( Optional ) : The index to end filling at.

**Mutates**.
___
### 5- Array.prototype.filter(func, thisValue) :

Returns an array of elements that returned `true` when passed into the function.

>thisValue ( Optional ) : Same as `every()`.

**Doesn't mutate**.
___
### 6- Array.prototype.find(func, thisValue) :

Returns the first element that returned `true` when passed into the function. 

>thisValue ( Optional ) : Same as `every()`.

**Doesn't mutate**.
___
### 7- Array.prototype.findIndex(func, thisValue) :

Returns the index of the first element that returned `true` when passed into the function.

>thisValue ( Optional ) : Same as `every()`.

**Doesn't mutate**.
___
### 8- Array.prototype.forEach(func, thisValue) :

Calls the function once for each element inside the element.

Returns `undefined`.

>thisValue ( Optional ) : Same as `every()`.

**Doesn't mutate**.
___
### 9- Array.prototype.from(object, mapFunction, thisValue) :

Makes an array from the object passed in.

>mapFunction ( Optional ) : A function called on each item in the array.
>
>thisValue ( Optional ) : Same as `every()` but with the mapFunction.

**Doesn't mutate**.
___
### 10- Array.prototype.includes(element, start) :

Searches for the element and returns `true` if it is found, otherwise it returns `false`.

>start ( Optional ) : Specifies where to start the search.

**Doesn't mutate**.
___
### 11- Array.prototype.indexOf(element, start) :

Searches for the element and returns its index if it is found, otherwise it returns (-1).

The search is from left to right.

>start ( Optional ) : Specifies where to start the search.

**Doesn't mutate**.
___
### 12- Array.prototype.isArray(object) :

Returns `true` if the object is an array, otherwise it returns `false`.

**Doesn't mutate**.
___
### 13- Array.prototype.join(separator) :

Returns the array as a string separated by a specified separator ( A string or a regex ). The default value of it is ",".

>separator ( Optional ) : The separator to be used.

**Doesn't mutate**.
___
### 14- Array.prototype.keys( ) :

Returns an array iterator object with the array keys.

**Doesn't mutate**.
___
### 15- Array.prototype.lastIndexOf(element, start) :

Searches for the element and returns its index if it is found, otherwise it returns (-1).

The search is from right to left.

>start ( Optional ) : Specifies where to start the search.

**Doesn't mutate**.
___
### 16- Array.prototype.map(func, thisValue) :

Creates a new array with the results of calling the function for each array element .

>thisValue ( Optional ) : Same as `every()`.

**Doesn't mutate**.
___
### 17- Array.prototype.pop( ) :

Removes the last element in the array.

**Mutates**.
___
### 18- Array.prototype.shift( ) :

Removes the first element in the array.

**Mutates**.
___
### 19- Array.prototype.push(item1, item2, ...itemX) :

Adds elements to the end of the array.

**Mutates**.
___
### 20- Array.prototype.unshift(item1, item2, ...itemX) :

Adds elements to the beginning of the array.

**Mutates**.
___
### 21- Array.prototype.reduce(callback(accumulator, currentValue), initialValue) :

Reduces the array to a single value.

>accumulator : Stores callback values.
>
>currentValue : The current element being processed.
>
>initialValue : A value to use as the initial value to the accumulator. If it's not provided, the first element in the array will be the initial accumulator value.

**Doesn't mutate**.
___
### 22- Array.prototype.reduceRight(callback(accumulator, currentValue), initialValue) :

Like reduce but starts from right to left.

**Doesn't mutate**.
___
### 23- Array.prototype.reverse( ) :

Reverses the array

**Mutates**.
___
### 24- Array.prototype.slice(start, end) :

Returns an array of the selected elements from the index of start until the index of end ( but not including it ).

**Doesn't mutate**.
___
### 25- Array.prototype.splice(index, howMany, item1, ....., itemX) :

Adds/Removes items from the array and returns the items it removed.

>index : from where to start removing/adding.
>
>howMany ( Optional ) : The number of items to remove.
>
>items ( Optional ) : The items to add.

**Mutates**.
___
### 26- Array.prototype.toString( ) :

Converts the array to a string that contains its items separated by commas.

**Doesn't mutate**.
___
### 27- Array.prototype.every(func, thisValue) :

Takes a function as a callback and applies it to every item in the array.

If at least one item returns `true`, `some()` returns `true`.

If all items return `false`, `some()` returns `false`.

>thisValue ( Optional ) : specifies the function's `this` value. If it's not passed, `this` is returned as `undefined`.

**Doesn't mutate**.
___
### 28- Array.prototype.sort(compareFunction) :

Sorts the items of the array alphabetically.

If the items are numbers, we use the compareFunction and make it like this :

```javascript
Array.sort((a, b) => a - b);
```

**Mutates**.
___