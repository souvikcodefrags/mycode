# mycode
just for my code fragments

Today I gave code test at Agilysis. One of the question was, count the frequency of characters in a given string. Here is my solution (the one I wrote in the test was horrible!):
```
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

Another one: check if a number is binary without converting it to string:

```
function isBin(num){
  var isBin=true
  Array.from(''+num).forEach((elem)=>{
    +elem===0?null:+elem===1?null:isBin=false
  })
  return isBin
}
console.log(isBin(39101))
```
Weird thing was when I input 001100100, the answer is false. I checked, the nuber is getting converted to 294976 somehow, no idea why. Same result when I just type 001100100 in the console and press enter.

A function which convert words of a sentence to Title Case except for articles and prepositions (if they are not at the begining of the sentence)
```
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

