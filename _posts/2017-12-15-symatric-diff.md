---
Layout:
Title:
Date:
---

# Symatric Difference

## Overview

    In mathematics, the symmetric difference, also known as the disjunctive union, of two sets 
    is the set of elements which are in either of the sets and not in their intersection. 
    The symmetric difference of the sets A and B is commonly denoted by

        A △ B , {\displaystyle A\,\triangle \,B,} {\displaystyle A\,\triangle \,B,}

    or

        A ⊖ B , {\displaystyle A\ominus B,} A\ominus B,

    or

        A ⊕ B . {\displaystyle A\oplus B.} A\oplus B.

    For example, the symmetric difference of the sets { 1 , 2 , 3 } {\displaystyle \{1,2,3\}} \{1,2,3\} 
    and { 3 , 4 } {\displaystyle \{3,4\}} \{3,4\} is { 1 , 2 , 4 } {\displaystyle \{1,2,4\}} \{1,2,4\}.


## Instructions

    Create a function that takes two or more arrays and returns an array of the symmetric difference (△ or ⊕) of the provided arrays.

    Given two sets (for example set A = {1, 2, 3} and set B = {2, 3, 4}), 
    the mathematical term "symmetric difference" of two sets is the set of elements which are in either of the two sets, 
    but not in both (A △ B = C = {1, 4}). For every additional symmetric difference you take (say on a set D = {2, 3}),
    you should get the set with elements which are in either of the two the sets but not both (C △ D = {1, 4} △ {2, 3} = {1, 2, 3, 4}).




# My Approach:

## Code:

    function getSymmetricDiffOfTwo(firstArr, secondArr) {
        var symmetricDiff = [];
        var sorted = firstArr.concat(secondArr).sort(function (a, b) { return a - b; });
        for (var index = 0; index < sorted.length; index++) {
            if (sorted[index] !== sorted[index + 1] && sorted[index] !== sorted[index - 1]) {
                symmetricDiff.push(sorted[index]);
            }
        }
        return symmetricDiff;
    }

    function removeDuplicates(arr) {
        var noRepeats = [];
        for (var i = 0; i < arr.length; i++) {
            if (noRepeats.indexOf(arr[i]) === -1) {
                noRepeats.push(arr[i]);
            }
        }
        return noRepeats;
    }

    function sym(args) {
        args = Array.from(arguments);
        var noDuplicates = [];
        args.forEach(function (element) {
            noDuplicates.push(removeDuplicates(element));
        });
        return noDuplicates.reduce(function (acc, val) {
            return getSymmetricDiffOfTwo(acc, val);
        }, []);
    }
    console.log(sym([3, 3, 3, 2, 5], [2, 1, 5, 7], [3, 4, 6, 6], [1, 2, 3], [5, 3, 9, 8], [1]));




