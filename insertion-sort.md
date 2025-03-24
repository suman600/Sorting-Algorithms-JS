# Insertion Sort Implementation in JavaScript

This is a JavaScript implementation of the Insertion Sort algorithm. Insertion Sort is a simple sorting algorithm that builds the final sorted array one item at a time. It repeatedly takes the next element from the unsorted part and inserts it into its correct position in the sorted part.

## Usage

1. Clone the repository or copy the `insertionSort` function from `insertionSort.js` into your project.

2. Use the `insertionSort` function to sort an array of numbers. Example:

    ```javascript
    let arr = [3, 8, 5, 9, 4, 2];
    let sortedArr = insertionSort(arr);
    console.log(sortedArr);
    ```

## Function Description

The `insertionSort` function takes an array of numbers as input (defaults to `[3, 8, 5, 9, 4, 2]` if not provided) and returns the sorted array using the Insertion Sort algorithm.

```javascript
function insertionSort(arr = [3, 8, 5, 9, 4, 2]) {
    let n = arr.length;
  
    for (let i = 1; i < n; i++) {
        let temp = arr[i];
        let j = i - 1;
        while (j >= 0 && arr[j] > temp) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = temp;
    }
  
    return arr;
}
