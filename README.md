
####Javascript Stringify Values of Array of Objects

```javascript
/**
* stringify values of object inside array of objects
* @param {array} array of objects
* @returns {Array} array of object with all values as string
*/
const StringifyValue = (array) => {
    return array.map(obj => {
        for (var key in obj) {
            if (obj.hasOwnProperty(key)) {
                if (typeof obj[key] != 'string') { obj[key] = JSON.stringify(obj[key]); }
            }
        }
        return obj;
    });
}
```
