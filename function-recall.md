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
