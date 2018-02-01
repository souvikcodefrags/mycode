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

