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

