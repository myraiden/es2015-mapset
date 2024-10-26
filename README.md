# Maps and Sets Exercise
## Quick Question #1
What does the following code return?
```
new Set([1,1,2,2,3,4])
```

The preceeding code returns:
*Set(4) {1, 2, 3, 4}*
Which is a set where 1:1, 2:2, 3:3, 4:$

​
## Quick Question #2
What does the following code return?
```
[...new Set("referee")].join("");
```

The preceeding code returns:
*'ref'*
All repeating letters were removed in the join.

## Quick Questions #3
What does the Map m look like after running the following code?
```
let m = new Map();
m.set([1,2,3], true);
m.set([1,2,3], false);
```

The preceeding code returns:
*Map(2) {Array(3) => true, Array(3) => false}*
Which translates to the following:
*{[1,2,3] => true, [1,2,3] => false}*

## hasDuplicate
Write a function called hasDuplicate which accepts an array and returns true or false if that array contains a duplicate
```
hasDuplicate([1,3,2,1]) // true
hasDuplicate([1,5,-1,4]) // false
```

Student Function:
```
function hasDuplicate(arr){
    let setArr=new Set(arr);
    if(setArr.size!=arr.length){
      return true;
    }else{
      return false;
    } 
  }
```

## vowelCount
Write a function called vowelCount which accepts a string and returns a map where the keys are numbers and the values are the count of the vowels in the string.
```
vowelCount('awesome') // Map { 'a' => 1, 'e' => 2, 'o' => 1 }
vowelCount('Colt') // Map { 'o' => 1 }
```

StudentFunction:
```
function vowelCount(str){
    let vowels=new Set("aeiou");
    let strArray=[...str];
    let mapVowels=new Map();
    
    vowels.forEach(letter=>{
        let count=0;    
        strArray.forEach(char=>{
            if(char==letter){
                count+=1;
            }
        })
        if(count>0){
            mapVowels.set(`${letter}`,`${count}`);
        }
    })

    return mapVowels;
}
```
