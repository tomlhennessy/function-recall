# Functions

## Echo
```javascript
function echo(string) {
  let upper = string.toUpperCase();
  let lower = string.toLowerCase();
  console.log(upper + " ... " + string + " ... " + lower);
}
```

## Vowel Counter
```javascript
function countVowels(word) {
  let vowels = 'aeiou';
  let count = 0;

  for (let i = 0; i < word.length; i++) {
      if (vowels.includes(word[i])) {
          count++;
      }
  }
  return count;
};
```

## Sum Array
```javascript
function sumArray(array) {
    let sum = 0;

    for (let i = 0; i < array.length; i++) {
        sum += array[i];
    }
    return sum;
}
```

## Pig Latin
```javascript
function pigLatinWord(word) {
    let vowels = 'aeiou';

    for (let i = 0; i < word.length; i++) {
        if (vowels.includes(word[i])) {
            if (i === 0) {
                return word + "yay";
            }
        } else {
            return word.slice(i) + word.slice(0, i) + "ay";
        }
    }
    return word;
}
```

## My Index Of
```javascript
let myIndexOf = function(arr, target) {
    for (let i = 0; i < arr.length; i++) {
        let el = arr[i];
        if (target === el) {
            return i;
        }
    }
    return -1;
}
```

## Two Sum Recall
```javascript
let twoSum = function (arr, target) {
    for (let i = 0; i < arr.length; i++) {
        let num1 = arr[i];

        for (let j = i + 1; j < arr.length; j++) {
            let num2 = arr[j];

            if (num1 + num2 === target) {
                return true;
            }
        }
    }
    return false;
}
```

## Fizz Buzz
```javascript
let fizzBuzz = function(max) {
    let nums = [];

    for (let i = 1; i < max; i++) {
        if ((i % 3 === 0 || i % 5 === 0) && !(i % 3 === 0 && i % 5 === 0))) {
            nums.push(i);
        }
    }
    return nums;
}
```

## Remove Last Vowel
```javascript
let removeLastVowel = function(word) {
    let vowels = 'aeiou';

    for (let i = word.length - 1; i >= 0; i--) {
        let char = word[i];
        if (vowels.includes(char)) {
            return word.slice(0, i) + word.slice(i + 1);
        }
    }
    return word;
}
```

## Least Common Multiple
```javascript
let leastCommonMultiple = function(num1, num2) {
    for (let i = 1; i <= (num1 * num2); i++) {
        if (i % num1 === 0 && i % num2 === 0) {
            return i;
        }
    }
}
```

## Choose Primes
```javascript
isPrime = function(num) {
    if (num < 2) return false;

    for (let i = 2; i < num; i++) {
        if (num % i === 0) {
            return false;
        }
    }
    return true;
}

let choosePrimes = function(nums) {
    let primes = [];

    for (let i = 0; i < nums.length; i++) {
        let num = nums[i];
        if (isPrime(num)) {
            primes.push(num);
        }
    }
    return primes;
}
```

## Uncompress Recall
```javascript
let uncompress = function(str) {
    let newStr = '';

    for (let i = 0; i < str.length; i += 2) {
        let char = str[i];
        let num = Number(str[i + 1]);

        for (let times = 0; times < num; times += 1) {
            newStr + char;
        }
    }
    return newStr;
}
```

## Hipsterfy
```javascript
let removeLastVowel = function(word) {
    let vowels = 'aeiou';

    for (let i = word.length - 1; i >= 0; i--) {
        let char = word[i];
        if (vowels.includes(char)) {
            return word.slice(0, i) + word.slice(i + 1);
        }
    }
    return word;
}

let hipsterfy = function(sentence) {
    let newWords = [];
    let words = sentence.split(' ');

    for (let i = 0; i < words.length; i++) {
        let word = words[i];
        newWords.push(removeLastVowel(word));
    }
    return newWords.join(' ');
}
```

## Repeating Translate
```javascript
let translateWord = function(word) {
    let vowels = 'aeiou';
    let lastChar = word[word.length - 1];
    if (vowels.includes(lastChar)) {
        return word + word;
    }

    let i = word.length - 1;
    while (i >= 0) {
        if (vowels.includes[word[i]]) {
            return word + word.slice(i);
        }
        i--;
    }
}

let repeatingTranslate = function(sentence) {
    let words = sentence.split(' ');
    let newWords = [];

    for (let i = 0; i < words.length; i++) {
        let word = words[i];
        if (word.length < 3) {
            newWords.push(word);
        } else {
            newWords.push(translateWord(word));
        }
    }
    return newWords.join(' ');
}
```
