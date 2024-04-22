# Bubble Sort Implementation in JavaScript

This is a simple implementation of the Bubble Sort algorithm in JavaScript. Bubble Sort is a basic sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order. The pass through the list is repeated until the list is sorted.

## Usage

1. Clone the repository or copy the `bubbleSort` function from `bubbleSort.js` into your project.

2. Use the `bubbleSort` function to sort an array of numbers. Example:

    ```javascript
    let sortArr = bubbleSort([8, 1, 20, 4, 9]);
    console.log(sortArr); // Output: [1, 4, 8, 9, 20]
    ```

## Function Description

The `bubbleSort` function takes an array of numbers as input and returns the sorted array using the Bubble Sort algorithm.

```javascript
function bubbleSort(arr) {
    let swapped;
    do {
        swapped = false;
        for (let i = 0; i < arr.length - 1; i++) {
            if (arr[i] > arr[i + 1]) {
                let temp = arr[i];
                arr[i] = arr[i + 1];
                arr[i + 1] = temp;
                swapped = true;
            }
        }
    } while (swapped);
    return arr;
}
