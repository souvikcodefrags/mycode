# mycode
just for my code fragments

Today I gave code test at Agilysis. One of the question was, 
#### count the frequency of characters in a given string. 
Here is my solution (the one I wrote in the test was horrible!):
```javascript
function charFrequency(str){
  FreqCount=[] 
  Array.from(str).forEach( (letter) => {
    FreqCount[letter]?FreqCount[letter]++:FreqCount[letter] = 1
  })
  console.log(FreqCount)
}
//charFrequency('strong arm mishmash or staggering high treason');
charFrequency('startstomototowardswarofwords');
```
#### Alternate Solution: Character occurence count
```javascript
var str = "I want to count the number of occurances of each char in this string";
var counts = {};
var ch, index, len, count;

for (index = 0, len = str.length; index < len; ++index) {
  ch = str.charAt(index);
  
  // 'count' will be `undefined` if we don't know this character yet
  // otherwise, 'count' will have the current occurence count of that character
  count = counts[ch]; 
  
  // if 'count is truthy, increase the current count by 1
  // otherwise, if 'count' is falsie, then add the character as property with 1 count
  counts[ch] = count ? count + 1 : 1; 
}
```

#### Check if a number is binary without converting it to string:

```javascript
function isBin(num){
  var isBin=true
  Array.from(''+num).forEach((elem)=>{
    +elem===0?null:+elem===1?null:isBin=false
  })
  return isBin
}
console.log(isBin(39101))
```
*Weird thing was when I input 001100100, the answer is false. I checked, the nuber is getting converted to 294976 somehow, no idea why. Same result when I just type 001100100 in the console and press enter*

#### A function which convert words of a sentence to Title Case except for articles and prepositions (if they are not at the begining of the sentence)
```javascript
function transform(value) {
    if (!value) return null;
    let words = value.split(' ');
    let prpeositions = ['as', 'at', 'around', 'about', 
      'by', 'down', 'during', 'for', 'from','in', 'on', 'of', 'out', 
      'over', 'to', 'the', 'like']
    words.forEach((word,i) => {
      word =  (i>0 && prpeositions.indexOf(word.toLowerCase())!== -1 )?word.toLowerCase():
        word.substr(0,1).toUpperCase()+word.substr(1).toLowerCase()
    }) 
    return words.join(' ')
  }
  
 console.log(transform('the return of the planet of the apes')) 
 ```
#### How do you find the missing numbers in a given sorted integer array of m to n?
```javascript
var foundMissing =(start, end, iarr) =>{
  for (var i=start; i<=end; i++){
    if(iarr.indexOf(i) ===-1 )
    console.log(i)
  }  
}
// Call the function
foundMissing(201, 210, [201,202, 205, 209]);
//output: 203/ 204/ 206/ 207/ 208/ 210
```

