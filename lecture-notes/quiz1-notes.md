# lecture content for quiz 1

## datatypes

### how to convert 
#### decimal to binary
keep on dividing by 2
#### octal to binary


### unsigned integers v.s. signed integers

conversion game for practice: https://games.penjee.com/binary-numbers-game/
ways to deal with signed numbers: 
- signed magnitude: easy to understand, but is not so good with hardware
- 1's complement: used in early computers, to make a number negative you just flip the bits
- 2's complement: what is mainly used in computers today (more detail below)

#### 2's complement
useful properties of 2's complement:
- only one 0
- addition works from rgular binary arithmetic (if you don't wrap)
- first bit still indicates positive/negative (if you use 0 as positive)
- no need for subtraction, but complement and add

to negate a number: flip the bits and add 1 -- take boolean NOT of EACH bit and add 1

to convert to decimal: flip the bits, add 1, convert to decimal, the number is negative of that number

practice with arithmetic of these numbers!!

dealing with overflow
- check carry in and out of leading digit (most significant digit is on the left)
- adding and positive and negative integer will not have a problem
- adding two positve integers may cause overflow when we get a carry in to the sign
- adding two negtive integers may cause overflow if there is no carry in and out

sign extension
