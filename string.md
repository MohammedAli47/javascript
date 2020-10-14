# String Methods :

### 1- String.fromCharCode(num1, num2, ..., numN) :

Transforms the sequence of UTF-16 units into a String of length N.
___
### 2- String.fromCodePoint(num1, num2, ..., numN) :

Transforms the sequence of code points into a String of length N.
___
### 3- String.prototype.charAt(index) :

Returns the character at the index passed into it. Index defaults to 0.
___
### 4- String.prototype.charCodeAt(index) :

Returns a number representing the UTF-16 code unit value of the character at the index passed into it. Index defaults to 0.
___
### 5- String.prototype.codePointAt(index) :

Return a number representing the code point value of the character at the given index.
___
### 6- String.prototype.concat(str1, str2, ..., strN) :

Return a new string of all the combined strings.
___
### 7- String.prototype.includes(searchingString, position) :

Returns `true` if the string contains the searchingString and `false` if it doesn't.

>position ( Optional ) : Determines where to start searching. Defaults to 0.
___
### 8- String.prototype.indexOf(searchValue, fromIndex) :

Returns the index of the first occurrence of the searchValue.

>fromIndex ( Optional ) : Determines where to start searching. Defaults to 0.

For fromIndex values lower than 0, or greater than str.length, the search starts at index 0 and str.length, respectively.

**Example :**

>'hello world'.indexOf('o', -5) returns 4.
>
>'hello world'.indexOf('o', 11) returns -1.
___
### 9- String.prototype.lastIndexOf(searchValue, fromIndex) :

Same as indexOf() but searches from right to left.
___
### 10- String.prototype.match(regex) :

Retrieves the result of matching a string against a regular expression.
___
### 11- String.prototype.matchAll(regex) :

Returns an iterator of all results matching a string against a regular expression, including capturing groups.
___
### 12- String.prototype.normalize(form) :

Returns the Unicode Normalization Form of the string.

**Forms :**

>"NFC" : Canonical Decomposition, followed by Canonical Composition.
>
>"NFD" : Canonical Decomposition.
>
>"NFKC" : Compatibility Decomposition, followed by Canonical >Composition.
>
>"NFKD" : Compatibility Decomposition.
___
### 13- String.prototype.padEnd(targetLength, padString) :

Pads the current string with a given string (repeated, if needed) so that the resulting string reaches a given length.

The padding is applied from the end of the current string.
___
### 14- String.prototype.padStart(targetLength, padString) :

The same as `padEnd()` but the padding is applied from the end.
___
### 15- String.prototype.repeat(count) :

Constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.
___
### 16- String.prototype.replace(regexp|subString, newSubString|function) :

Replaces the matches of the first argument with the second.
___
### 17- String.prototype.replaceAll(regexp|subString, newSubString|function) :

Same as `replace()` but for all matches or sub-strings.
___
### 18- String.prototype.search(regex) :

Performs a search for all matches of the regex.
___
### 19- String.prototype.slice(beginIndex, endIndex) :

Extracts a section of a string and returns it as a new string.
___
### 20- String.prototype.split(separator, limit) :

Divides a string into an ordered array of sub-strings.
___
### 21- String.prototype.endsWith(searchingString, length) :

Returns `true` if the string ends with the searchingString and `false` if it doesn't.

>length ( Optional ) : Determines the length of the string. Defaults to the original length.
___
### 22- String.prototype.startsWith(searchingString, position) :

Same as `endsWith()` but for the beginning.
___
### 23- String.prototype.toLowerCase( ) :

Returns the calling string value converted to lower case.
___
### 24- String.prototype.toUpperCase( ) :

Returns the calling string value converted to upper case.
___
### 25- String.prototype.toString( ) :

Returns a string representing the specified object.
___
### 26- String.prototype.substring(indexStart, indexEnd) :

Returns a sub-string of the characters found between the indices.
___
### 27- String.prototype.trim( ) :

Removes whitespace from both ends of a string.
___
### 28- String.prototype.trimEnd( ) :

Removes whitespace from the end of a string.
___
### 29- String.prototype.trimStart( ) :

Removes whitespace from the beginning of a string.
___
### 30- String.prototype.valueOf( ) :

Returns the primitive value of a String object.
___
