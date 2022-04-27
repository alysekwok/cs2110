# lecture content for quiz 1

## datatypes

### how to convert 

**decimal to binary**
keep on dividing by 2, stop when quotient reaches 2
**octal to binary**
1. split each digit up
2. convert each digit to 3 bit binary
3. combine each binary number
**hexadecimal to binary**
1. split each digit up
2. convert each digit to 4 bit binary
3. combine each binary number


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
- happens when there's not enough bitsto store output of addition
- check carry in and out of leading digit (most significant digit is on the left)
- adding and positive and negative integer will not have a problem
- adding two positve integers may cause overflow when we get a carry in to the sign
- adding two negtive integers may cause overflow if there is no carry in and out

### bitwise operators
- NOT (symbol: ~)
- OR (symbol: |)
- AND (symbol: &)
- XOR (symbol: ^)

### masking
- to SET a bit means to make it 1
- to CLEAR a bit means to make it 0
ways to mask:
- extract specified bits
- clear specified bits
- set the specified bits
- flip the specified bits


### shifting
- left shifting (<<)
- right shifting (>>, signed), (<<<, unsigned)
these operations are equivalent to multiplying/dividing by 2 (whenever you mve a digit over by one spot, you multiply/divide it by 2)

### IEEE-754 floating point numbers
formula: (-1)^S * 1.M * 2^(E-127)
sign (1 bit), exponent (8 bits), mantissa (23 bits)
to compare IEEE-754 numbers:
- treat like a 32 bit signed number
edge cases (add table in later)

## transistors, gates, kmaps

### transistors
2 types of transistors: p-type and n-type
p-type:
- connected to power
- normally "closed" and represents a 1 signal
- has bubble

n-type:
- connected to ground
- normally "open" and represents a 0 signal

**demorgan's law**
conte bubble theorem





