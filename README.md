# Cipher
[Live Link](https://ivthefourth.github.io/cipher/)

    &c]zn9V¡^MCF"B0X¢][!qE+BYx?5z:Y7-LG<Q3)crRZ5!(,?8!~c%kyJ6y¡#c'+:$cv9;'0D
    
## Details
This is a simple program that takes in a string of text and encodes it as a different string of text. The character set for the input is restricted to [100 unique characters](#valid-input-characters), and any invalid characters sent to the input will be converted to spaces before encoding.    

To encode the input, spaces are added at the end of the string until the string length is evenly divisible by 10 (if necessary), each character is converted to a number 0-99, an affine cipher is applied to each character (mod 100), another affine cipher is applied to blocks of 10 characters (mod 10^20), these blocks are split into two digit numbers (00-99), and finally each of these numbers is converted back into a character for the final output.

The "keys" used for the two ciphers are randomly generated, converted to letters, and appended to the beginning of the encoded string. To decipher, the program can take an encoded string as input, and use these keys to perform the inverse operations needed to return the original string (maybe with some extra spaces at the end). 

## Valid Input Characters
* Horizontal Tab
* Line Feed (carriage return converts to LF)
* ASCII characters 32 (Space) through 126 (~)
* ¡, ¢, £


## Dependencies
* [bignumber.js](https://github.com/MikeMcl/bignumber.js/)
* [jQuery](https://github.com/jquery/jquery)

