# Find The Lowest Value in an Array

To find the lowest value in an array, you can use the following JavaScript function:

```javascript
function findLowestValue(arr) {
    if (arr.length === 0) {
        return undefined; // If the array is empty, return undefined
    }
    
    let lowest = arr[0]; // Initialize the lowest value with the first element of the array
    
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < lowest) {
            lowest = arr[i]; // Update lowest if a smaller value is found
        }
    }
    
    return lowest;
}

// Example usage
const array = [3, 1, 7, -2, 5];
const lowestValue = findLowestValue(array);
console.log("Lowest value:", lowestValue); // Output: -2
