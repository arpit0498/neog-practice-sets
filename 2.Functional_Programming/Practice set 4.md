# Functional Programming Set 4

**Instructions:**

- Make use of **.reduce()** method in this set.
- You can make use of basic methods such as .length, toLowerCase(), toUpperCase() if needed.
- Do NOT use for-loops.

1. Given an array, write an ES6 function that returns the total length of all the strings in an array.

    ```jsx
    const strings = ["apple", "banana", "cherry", "date", "blueberry"];
    // Your code here
    const totalLength = (arr) => {

    return arr.reduce((total, str) => total + str.length, 0);
    };
    console.log(totalLength(strings));
    // Output: 30
    ```

2. Write an ES6 function sumSquares that takes an array of numbers and returns the sum of the squares of all the numbers in the array

    ```jsx
    const numbers = [1, 2, 3, 4, 5];
    // Your code here
    const sumSquares = (arr) => {

    return arr.reduce((total, num) => total + Math.pow(num, 2), 0);
    };
    console.log(sumSquares(numbers));
     // Output: 55 
    ```

3. Write an ES6 function that calculates and returns the total value of all items in an array of objects.

    ```jsx
    const items = [
      { name: "Item 1", price: 10 },
      { name: "Item 2", price: 20 },
      { name: "Item 3", price: 30 }
    ];
    // Your code here
    const totalValue = (arr) => {

    return arr.reduce((total, item) => total + item.price, 0);
    };
    console.log(totalValue(items)); 
    // Output: 60
    ```

4. Write an ES6 function that takes an array of strings as input and concatenates them into a single string.

    ```jsx
    // Your code here
    const concatStrings = (arr) => {

    return arr.reduce((total, str) => total + str, "");
    };
    console.log(concatStrings(['this', 'is', 'fun'])); // Output: 'thisisfun'
    ```

5. Write an ES6 function to multiply and return all the elements of a given array.

    ```jsx
    const numbers = [1, 2, 3, 4, 5];
    // Your code here
    const product = (arr) => {

    return arr.reduce((total, num) => total * num, 1);
    };
    console.log(product(numbers));
    // Output: 120
    ```

6. Write an ES6 function that takes an array of strings and returns the longest string.

    ```jsx
    const strings = ["neogcamp", "Haule Haule", "code", "Batman", "Awesome"];
    // Your code here
    const longestString = (strings) => {

    return strings.reduce((longest, current) => {
        return current.length > longest.length ? current : longest;
    }, '');
    };
    console.log(longestString(strings)); 
    // Output: 'Haule Haule'
    ```

7. Write an ES6 function that takes an array of objects with name and age property, and returns the name of the oldest person.

    ```jsx
    const people = [
       {name: 'Jeena', age: 25}, 
       {name: 'Priya', age: 30}, 
       {name: 'Naina', age: 45}
    ]
    // Your code here
    const oldestPersonName = (people) => {

    const oldest = people.reduce((prev, current) => {
        return prev.age > current.age ? prev : current;
    });
    return oldest.name;
    };
    console.log(oldestPersonName(people)); 
    // Output: 'Naina'
    ```

8. Write an ES6 function that takes an array of objects representing people with properties name and age, and returns an object with the average age of all the people.

    ```jsx
    const people = [
      { name: 'Alice', age: 25 },
      { name: 'Bob', age: 30 },
      { name: 'Charlie', age: 35 },
      { name: 'David', age: 40 }
    ];
    // Your code here
    
    console.log(getAverageAge(people));
    // Output: { averageAge: 32.5 }
    ```

9. Write an ES6 function that takes an array of objects representing products with properties name, price, and quantity, and returns an object with the most expensive product.

    ```jsx
    const products = [
      { name: "Bread", price: 10, quantity: 2 },
      { name: "Clips", price: 20, quantity: 5 },
      { name: "Knife", price: 30, quantity: 1 },
      { name: "Slipper", price: 40, quantity: 3 }
    ];
    // Your code here
    
    console.log(findMostExpensiveProduct(products)); 
    // { name: "Slipper", price: 40, quantity: 3 }
    ```

10. Write an ES6 function that takes an array of strings and returns an object with the count of each string.
