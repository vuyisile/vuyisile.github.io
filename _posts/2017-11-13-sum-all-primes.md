---
Layout:
Title: sum all primes
Date: 2017-11-13
---
# Overview

According to research, a prime number (or a prime) is a natural number greater than 1 that has no positive divisors other than 1 and itself. 
A natural number greater than 1 that is not a prime number is called a composite number. 
For example, 5 is prime because 1 and 5 are its only positive integer factors, whereas 6 is composite because it has the divisors 2 and 3 in addition to 1 and 6.

Solving this problem was very tricky, because first I had to thing of a way to find a number that has only two factors (1 and its self) and add it to variable that is equals 0 accoding to the given limit which is my input.


# Problem Statement

Sum all the prime numbers up to and including the provided number.A prime number is defined as a number greater than one and having only two divisors, one and itself. For example, 2 is a prime number because it's only divisible by one and two.The provided number may not be a prime.


# My approach

My first attempt was very dodgy and worked for only prime numbers that are between 5 and 100, and I Honestly found it very difficult to include primes that are left out, so I searched for hints to solve this problem, and I found that in most algorithms the used the Sieve of Eratosthenes. Sieve of Eratosthenes is an ancient algorithm for finding all prime numbers up to any given limit. That’s exactly part of what I am supposed to do here. Before doing anything, I had to figure out what my algorithm was supposed to achieve:

   -   The solution should sum all the prime numbers up to and including the provided argument. However, it has to consider that the provided num might not be a prime number.

   -   The solution had to check whether or not a number was a prime or not. This meant conditional statements, and some form of looping.

   -   Once all the primes were found, they had to be summed up into one number which would then be returned.

### Solution

#### check weather the is a prime or not.

I created a function (called checkIfPrime) that accepts a number to determine whether or not it is prime. I then looped from two all the way up until the input (num),which is the limit minus one because my input has to be divisible by itself and one. If the remainder of the value with the current loop value is zero then it is not prime so break out and false. 

There after, i used if statements to check the weather the value for checkIfPrime(num) is true or false, so that I return the final answer in code form this is how it looks:

            <!-- if (num === 1){
                return 0;
            }else if(isPrime(num) === false{
            
                return sumPrimes(num - 1);
            }else if(isPrime(num) === true){
            
                return num + sumPrimes(num - 1);
            }
            } -->


In conclusion, if (num === 1){return 0;} because 1 is not a prime, so return nothing, also stops the recursive calls,if(isPrime(num) === false): Check if your number is not prime and return sumPrimes(num - 1),for non primes check the next number down from the maximum number, do not add anything to the answer or else, Check if your number is prime for primes add that number to the next number in the sequence through a recursive call to our sumPrimes function therefore return num + sumPrimes(num - 1).
