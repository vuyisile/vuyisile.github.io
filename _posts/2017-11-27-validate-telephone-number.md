---
Layout:
Title:
Date:
---

# The U.S Tel-number Validator.

## Overview.

The **validateTelNum** function, in this task I was required to create an algorithm that checks for valid American telephone number pattern. 
According to research, the United States of America has a system where they use a collection of numbers as a telephone number which consists of 10 digits in its telephone number systems or 11 digits (which includes their code number as the beginning number).
The code number is used for international telecommunication. It is always the first digit in the sequence of the numbers and is always 1 for the U.S.


## Instructions.

    Return true if the passed string is a valid US phone number.

    The user may fill out the form field any way they choose as long as it is a valid US number. 
    The following are examples of valid formats for US numbers (refer to the tests below for other variants):

        555-555-5555
        (555)555-5555
        (555) 555-5555
        555 555 5555
        5555555555
        1 555 555 5555
        1 (555) 555-5555
        1 (555)555-5555
    

    For this challenge you will be presented with a string such as 800-692-7753 or 8oo-six427676;laskdjf. 
    Your job is to validate or reject the US phone number based on any combination of the formats provided above. 
    The area code is required. If the country code is provided, you must confirm that the country code is 1. 
    Return true if the string is a valid US phone number; otherwise return false.



## Given code.

        function telephoneCheck(str) {
            return str;
        }


## My approach.

For this challlenge I used a javascript built in regex tester (**.test()**)that checks if my regular expression is a **true/valid** and/or **false/invalid** pattern from my string of telephone numbers.
To solve this problem I had to check all the valid telephone patterns and used the simplest way I thought could work which was creating a valid regex for each telephone number pattern and assigned each in its variable, then I combined them to be one regex using the pipe(**'|'**) as my **'or'** in my new variable called **allValid** and tested allValid using **.test()**.

        function telephoneCheck(str) {
            var valid1 = /^1 (\([0-9]{3}\))[-| ]([0-9]{3})[-| ]([0-9]{4})$/;
            var valid2 = /^(\([0-9]{3}\))[-| ]([0-9]{3})[-| ]([0-9]{4})$/;
            var valid3 = /^([0-9]{3})[-| ]([0-9]{3})[-| ]([0-9]{4})$/;
            var valid4 = /^([0-9]{10})$/;
            var valid5 = /^1 ([0-9]{3})[-| ]([0-9]{3})[-| ]([0-9]{4})$/;
            var valid6 = /^1([0-9]{3})[-| ]([0-9]{3})[-| ]([0-9]{4})$/;
            
            var allValid = /^([0-9]{10})$|^1 (\([0-9]{3}\))[-| ]([0-9]{3})[-| ]([0-9]{4})$|
            ^(\([0-9]{3}\))[-| ]([0-9]{3})[-| ]([0-9]{4})$|^([0-9]{3})[-| ]([0-9]{3})[-| ]([0-9]{4})$|
            ^1 ([0-9]{3})[-| ]([0-9]{3})[-| ]([0-9]{4})$/;

       
            return allValid.test(str);
        }

After completing that I had to refactor the regex in to something small because it looked long and messy, so i created a new variable called **finalValid** which holds my new regular expression that works for all the patterns.
Personally I found it difficult to combine the regex, even though it took me a lot of time, I used the online regex tester to create the general pattern (which maid life a bit easy).

        function telephoneCheck(str) {
            var finalValid =  /^(1\s|1)*((\(\d{3}\))|\d{3})(\-|\s)*(\d{3})(\-|\s)*(\d{4})$/;
            return finalValid.test(str);
        }


## Conclusion.

What I learned from this challenge is that, simplicity is the key to success, because looking at this problem, it helped me to understand how regular expressions work.

