- Declaration: `let Map = new Map();`
#### Usage:
- `for (let num of arr) { frequencyMap.set(num, (frequencyMap.get(num) || 0) + 1); }`

---
##### A program to find min and max frequency in an array  
 ```function findFrequency(arr) {
    let frequencyMap = new Map();
    
    // Populate frequency map
    for (let num of arr) {
        frequencyMap.set(num, (frequencyMap.get(num) || 0) + 1);
    }

    let frequencies = Array.from(frequencyMap.values());
    let maxFrequency = Math.max(...frequencies);
    let minFrequency = Math.min(...frequencies);

    // Find elements with highest and lowest frequencies
    let elementsWithMaxFrequency = [];
    let elementsWithMinFrequency = [];

    for (let [key, value] of frequencyMap) {
        if (value === maxFrequency) {
            elementsWithMaxFrequency.push(key);
        }
        if (value === minFrequency) {
            elementsWithMinFrequency.push(key);
        }
    }

    return {
        maxFrequency: maxFrequency,
        minFrequency: minFrequency,
        elementsWithMaxFrequency: elementsWithMaxFrequency,
        elementsWithMinFrequency: elementsWithMinFrequency
    };
}

let arr = [3, 4, 5, 6, 2, 4, 1, 1, 5, 6, 6];
let result = findFrequency(arr);

console.log("Highest frequency:", result.maxFrequency);
console.log("Elements with highest frequency:", result.elementsWithMaxFrequency);
console.log("Lowest frequency:", result.minFrequency);
console.log("Elements with lowest frequency:", result.elementsWithMinFrequency);

```
>We are spreading our frequencies in Math.max(...frequencies) to get the highest frequency