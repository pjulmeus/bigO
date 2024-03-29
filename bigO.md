Simplify the following big O expressions as much as possible:

O(n + 10) - O(n)
O(100 * n) - O(n)
O(25) - O(1)
O(n^2 + n^3) - 0(n^3)
O(n + n + n + n) - O(n)
O(1000 * log(n) + n) - 0(log(n))
O(1000 * n * log(n) + n) - 00(log(n))
O(2^n + n^2)- 0(n^2)
O(5 + 3 + 1) - 0(1)
O(n + n^(1/2) + n^2 + n * log(n)^10)- 0(log(n)^10)

Determine the time complexities for each of the following functions. If you’re not sure what these functions do, copy and paste them into the console and experiment with different inputs!

function logUpTo(n) {
  for (let i = 1; i <= n; i++) {
    console.log(i);
  }
}
Time Complexity: O(n)

function logAtLeast10(n) {
  for (let i = 1; i <= Math.max(n, 10); i++) {
    console.log(n);
  }
}
Time Complexity: 0(1)

function logAtMost10(n) {
  for (let i = 1; i <= Math.min(n, 10); i++) {
    console.log(1);
  }
}
Time Complexity: O(1)

function onlyElementsAtEvenIndex(array) {
  let newArray = [];
  for (let i = 0; i < array.length; i++) {
    if (i % 2 === 0) {
      newArray.push(array[i]);
    }
  }
  return newArray;
}
Time Complexity: 0(n)

function subtotals(array) {
  let subtotalArray = [];
  for (let i = 0; i < array.length; i++) {
    let subtotal = 0;
    for (let j = 0; j <= i; j++) {
      subtotal += array[j];
    }
    subtotalArray.push(subtotal);
  }
  return subtotalArray;
}
Time Complexity: o(n2)

function vowelCount(str) {
  let vowelCount = {};
  const vowels = "aeiouAEIOU";

  for (let char of str) {
    if(vowels.includes(char)) {
      if(char in vowelCount) {
        vowelCount[char] += 1;
      } else {
        vowelCount[char] = 1;
      }
    }
  }

  return vowelCount;
}
Time Complexity: O(n)

Part 3 - short answer
Answer the following questions

True or false: n^2 + n is O(n^2). True
True or false: n^2 * n is O(n^3). True
True or false: n^2 + n is O(n). False
What’s the time complexity of the .indexOf array method? o(n)
What’s the time complexity of the .includes array method? O(n)
What’s the time complexity of the .forEach array method? O(n)
What’s the time complexity of the .sort array method? O(n log n)
What’s the time complexity of the .unshift array method? O(1)
What’s the time complexity of the .push array method? O(n)
What’s the time complexity of the .splice array method? O(1)
What’s the time complexity of the .pop array method? O(n)
What’s the time complexity of the Object.keys() function? O(n)
BONUS

What’s the space complexity of the Object.keys() function?