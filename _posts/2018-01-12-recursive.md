---
Layout:
Title:  Recursion
Date:   2018-01-12
---
# Recursion

Recursion is a function calls itself. 


## Example


One example is the calculation of factorials. The factorial of a number n is calculated by multiplying 1 * 2 * 3 *... n. The following example shows how to calculate factorials iteratively,that is, by using a while loop in which the result is calculated. 

        function factorial(num){  
            // If the number is less than 0, reject it.  
            if (num < 0) {  
                return -1;  
            }  
            // If the number is 0, its factorial is 1.  
            else if (num == 0) {  
                return 1;  
            }  
            var tmp = num;  
            while (num-- > 2) {  
                tmp *= num;  
            }  
            return tmp;  
        }  

        var result = factorial(8);  
        console.log(result);// Output: 40320  
  
You can make the example recursive very simply. Instead of using a while loop to calculate the value, you can simply call factorial again, passing in the next lowest value. The recursion stops when the value is 1. 

        function factorial(num){  
            // If the number is less than 0, reject it.  
            if (num < 0) {  
                return -1;  
            }  
            // If the number is 0, its factorial is 1.  
            else if (num == 0) {  
                return 1;  
            }  
            // Otherwise, call this recursive procedure again.  
            else {  
                return (num * factorial(num - 1));  
            }  
        }  

        var result = factorial(8);  
        console.log(result);// Output: 40320  