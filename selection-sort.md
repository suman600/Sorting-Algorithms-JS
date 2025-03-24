# Selection Sort Implementation in JavaScript

This is a JavaScript implementation of the Selection Sort algorithm. Selection Sort is a simple sorting algorithm that repeatedly selects the minimum element from the unsorted portion of the array and moves it to the beginning, thereby sorting the array.

## Usage

1. Clone the repository or copy the `selectionSort` function from `selectionSort.js` into your project.

2. Use the `selectionSort` function to sort an array of numbers. Example:

    ```javascript
    let sortArr = selectionSort([4, 1, 9, 2, 3, 6]);
    console.log(sortArr); // Output: [1, 2, 3, 4, 6, 9]
    ```

## Function Description

The `selectionSort` function takes an array of numbers as input and returns the sorted array using the Selection Sort algorithm.

```javascript
function selectionSort(arr){
  let swapped;
  do {
    swapped = false;
    for(let i = 0; i < arr.length - 1; i++) {
      let minIndex = i;
      for(let j = i + 1; j < arr.length; j++) {
        if(arr[j] < arr[minIndex]) {
          minIndex = j;
          swapped = true;
        }
      }
      if(minIndex !== i) {
        let temp = arr[i];
        arr[i] = arr[minIndex];
        arr[minIndex] = temp;
      }
    }    
  } while(swapped);
  return arr;
}
