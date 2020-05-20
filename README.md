# codewars
Having fun getting a little sharper with Javascript here :)

##

##

##

##

## Sum of Digits / Digital Root
https://www.codewars.com/kata/541c8630095125aba6000c00

> In this kata, you must create a digital root function.
> 
> A digital root is the recursive sum of all the digits in a number. Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. This is only applicable to the natural numbers.
> 
> Here's how it works:
> 
> digital_root(16)
> => 1 + 6
> => 7
> 
> digital_root(942)
> => 9 + 4 + 2
> => 15 ...
> => 1 + 5
> => 6
> 
> digital_root(132189)
> => 1 + 3 + 2 + 1 + 8 + 9
> => 24 ...
> => 2 + 4
> => 6
> 
> digital_root(493193)
> => 4 + 9 + 3 + 1 + 9 + 3
> => 29 ...
> => 2 + 9
> => 11 ...
> => 1 + 1
> => 2

### Solution
```
function digital_root(n) {
  let currentNumbers = n
  let sum = 0
  console.log("num before loop", currentNumbers)

  while (currentNumbers >= 10) {
        sum = 0
        currentNumbers.toString().split('').forEach(num => {
          sum += parseInt(num)
        })
        currentNumbers = sum
  }
  console.log("num after loop", currentNumbers)
  return currentNumbers
}
```
