# Fibonacci Sequence (Recursive Approach)

Below is the JavaScript code for generating the Fibonacci sequence using a recursive approach:

````javascript
function fib(n) {
    if (n <= 0) {
        return [];
    } else if (n === 1) {
        return [0];
    } else if (n === 2) {
        return [0, 1];
    } else {
        return fib(n - 1) + fib(n - 2);
    }
}

// Example usage
console.log(fib(0)); // Output: []
console.log(fib(1)); // Output: [0]
console.log(fib(2)); // Output: [0, 1]
console.log(fib(10)); // Output: 55
