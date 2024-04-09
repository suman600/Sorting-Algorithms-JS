# Fibonacci Sequence

Below is the JavaScript code for generating the Fibonacci sequence up to the nth number:

```javascript
function fibonacci(n) {
  // Return an empty array for non-positive inputs
  if (n <= 0) return [];
  
  // Return [0] for n = 1, as the Fibonacci sequence starts with 0
  if (n === 1) return [0];
  
  // Initialize the Fibonacci sequence array with the first two numbers
  const fibSequence = [0, 1];
  
  // Generate the Fibonacci sequence up to the nth number
  for (let i = 2; i < n; i++) {
    // Calculate the next Fibonacci number
    const nextFib = fibSequence[i - 1] + fibSequence[i - 2];
    // Add the next Fibonacci number to the sequence
    fibSequence.push(nextFib);
  }
  
  // Return the Fibonacci sequence up to the nth number
  return fibSequence;
}

// Example usage
const n = 10; // Generate the first 10 Fibonacci numbers
const result = fibonacci(n);
console.log(result); // Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
