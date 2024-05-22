# Format a JavaScript Date to YYYY MM DD

```
const date = new Date();
const year = date.getFullYear() * 1e4; // 1e4 gives us the the other digits to be filled later, so 20210000.
const month = (date.getMonth() + 1) * 100; // months are numbered 0-11 in JavaScript, * 100 to move two digits to the left. 20210011 => 20211100
const day = date.getDate(); // 20211100 => 20211124
const result = year + month + day + '' // `+ ''` to convert to string from number, 20211124 => "20211124"

// in one line
date.getFullYear() * 1e4 + (date.getMonth() + 1) * 100 + date.getDate() + ''; // "20211124"
```

https://masteringjs.io/tutorials/fundamentals/date-tostring-format-yyyy-mm-dd
