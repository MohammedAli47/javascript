## Regular Expressions :
They are used in programming languages to match parts of strings using a regex ( pattern ).

>We make a regex like this : (/ regex /).

1- To search for a certain word in a string, we use the **.test() method**.

It only returns `true` or `false`.

Example :

```javascript
let name = "Mohamed Ali"; // string
let reg = /Ali/; // regex
let result = reg.test(name);
console.log(result) // true
```

>### Note :
> Using the test method makes a literal search, which means that `Ali` isn't the same as `ali`, `aLi` or `ALI`.

2- To search for multiple words, we use the `OR` operator ( `|` ) like this : `/Ahmed|Ali|Joe/`.

Example :

```javascript
let sent1 = "James has a pet cat.";
let sent2 = "There's a bird on the tree.";

let reg = /cat|dog|bird/;

let result1 = reg.test(sent1);
console.log(result1) // true

let result2 = reg.test(sent2);
console.log(result2) // true
```

3- To avoid literal searching, we use the ignore case flag ( `i` ) after the regex we use.

Example :

```javascript
let name = "Mohamed Ali";
let reg = /ali/i;
let result = reg.test(name);
console.log(result) // true
```

4- To extract words from a string, we use the **.match() method**.

It returns an array of the words found in the string ( Or `null` if there's no matches ).

Example :

```javascript
let name = "Mohamed Ali";
let reg = /Ali/;
let result = name.match(reg);
console.log(result) // ['Ali']
```

>### Note :
>match() is the opposite of test().

```javascript
'string'.match(/regex/);
/regex/.test('string');
```

>**match doesn't return repeated words in the array**.
```javascript
let x = "Hi Hi Hi Hi";
let y = /hi/i;
let result = x.match(y);
console.log(result); // ['Hi']
```

5- To return any repeated words, we use the ( `g` ) flag after the regex we use.

Example :

```javascript
let sent = "Twinkle, twinkle, little star";
let reg = /twinkle/ig;
let result = sent.match(reg);
console.log(result); // ['Twinkle', 'twinkle']
```
>### Note :
>We can use more than one flag in a regex.

6- To search for words with specific matching characters, we use the Wildcard character ( `.` ).

Example :

```javascript
let sent = "fun, bun, under";
let reg = /un./i;
reg.test(sent); // returns true
sent.match(reg); // returns ['fun', 'bun', 'under']
```

7- To search for more than one character, we put them in an array inside the regex.

Example :

```javascript
let sent = "fun, bun";
let reg = /[bf]un/;
reg.test(sent); // returns true
sent.match(reg); // returns ['fun', 'bun']
```

8- To search for a range of characters, we use the hyphen character ( `-` ).

Example :

```javascript
let sent = "fun, bun";
let reg = /[a-e]un/;
reg.test(sent); // returns true
sent.match(reg); // returns ['bun']
```

9- We can search for numbers as well in strings.

Example :

```javascript
let reg = /[a-z0-9]/; // searches for all letters and numbers
```

10- To exclude certain characters, we use the caret character ( `^` ) ( *inside an array* ).

Example :

```javascript
let sent = "fun, bun";
let reg = /[^b]un/; // [^b] is called a negated character set
reg.test(sent); // returns true
sent.match(reg); // returns ['fun']
```

11- To search for characters occurring more than once, we use the plus sign ( `+` ).

Example :

```javascript
let sent = "Mississippi";
let reg = /s+/g;
let result = sent.match(reg); // returns ['ss', 'ss']
```

12- To match characters that occur zero or more times, we use the asterisk or star ( `*` ).

Example :

```javascript
let sent1 = "goooal!";
let sent2 = "gut feeling";

let reg = /go*/;

sent1.match(reg); // returns ['gooo']
sent2.match(reg); // returns ['g']
```
>Up until now, we have been using `greedy matching`, which finds the longest sub-string to extract.

13- To use the other way of matching ( `lazy matching` ), we use the question mark character ( `?` ).

Example :

```javascript
let sent = "titanic";

let reg1 = /t[a-z]*i/; // ( greedy matching )
let reg2 = /t[a-z]*?i/; // ( lazy matching )

sent.match(reg1); // returns ['titani'] 
sent.match(reg2); // returns ['ti'] 
```

>### Note :
>The two regexes search  for a string with "t" at the beginning, "i" at the end and letters between them.

14- The caret character ( `^` ) ( *inside an array* ) to specify a certain beginning of a string.

Example :

```javascript
let name = "Mohamed Ali";
let reg1 = /^Mohamed/;
let reg2 = /^Ali/;
reg1.test(name); // returns true
reg2.test(name); // returns false
```

15-  The dollar sign character ( `$` ) to specify a certain ending of a string.

Example :

```javascript
let name = "Mohamed Ali";
let reg1 = /Ali$/;
let reg2 = /Mohamed$/;
reg1.test(name); // returns true
reg2.test(name); // returns false
```

16- The question mark character ( `?` ) is also used to make a character before it optional ( can exist or not ).

Example :

```javascript
let american = "color";
let british = "colour";
let reg= /colou?r/;
reg.test(american); // Returns true
reg.test(british); // Returns true
```

## Some popular shortcuts used in regexes :

1- ( `\w` ) is equal to [A-Za-z0-9_].

Example :

```javascript
let sent = "some_random_text1234";
let reg = /\w+/;
reg.test(sent); // Returns true
```

> Its opposite ( `\W` ) which is equal to [^A-Za-z0-9_].

```javascript
let sent = "some_random_text1234#";
let reg = /\W/;
sent.match(reg); // Returns ['#']
```

2- ( `\d` ) is equal to [0-9].

> Its opposite ( `\D` ) which is equal to [^0-9].

3- ( `\s` ) is equal to [ \r\t\f\n\v] ( All white spaces ).

> Its opposite ( `\S` ) which is equal to [^ \r\t\f\n\v].

4- Quantity specifiers ( `{}` ) which specify how many times a character is repeated.

Example :

```javascript
let reg1 = /a{3,5}/; // 'a' is repeated from 3 to 5 times
let reg2 = /a{3,}/; // 'a' is repeated at least 3 times
let reg3 = /a{3}/; // 'a' is repeated 3 times
```

Thanks for staying till the end 💖.