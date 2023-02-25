# ES6+ Practice Question Set 1

1. Write a function that takes a user's age and determines if they are old enough to vote (age 18 or older).

    ```jsx
    // Your ES6 code here
    
    console.log(isEligibleToVote(20)) // Eligible to vote
    console.log(isEligibleToVote(18)) // Eligible to vote
    console.log(isEligibleToVote(17)) // Not eligible to vote
    ```

1. Write a function that takes two numbers as input and determines which one is greater.

    ```jsx
    // Your ES6 code here
    
    console.log(isGreater(2, 5)) // 5 is greater than 2
    console.log(isGreater(10, 5)) // 10 is greater than 5
    ```

2. Write a function that takes a number as input and determines if it is positive or negative.

    ```jsx
    // Your ES6 code here
    
    console.log(checkNum(9)) // Positive Number
    console.log(checkNum(-8)) // Negative Number
    console.log(checkNum(22)) // Positive Number
    ```

3. Write a function that takes a number as input and determines if it is even or odd.

    ```jsx
    // Your ES6 code here
    
    console.log(isEvenOdd(5)) // Odd Number
    console.log(isEvenOdd(8)) // Even Number
    console.log(isEvenOdd(10)) // Even Number
    ```

4. Write a function that takes a string as input and determines if it contains the letter 'a' or ‘A’.

    ```jsx
    // Your ES6 code here
    
    console.log(checkForAlphabetA("Tanay")) // Includes a 
    console.log(checkForAlphabetA("Jeep")) // Does not include a 
    console.log(checkForAlphabetA("Jane")) // Includes a 
    ```

5. Write a function that takes a string as input and determines if it is longer than 5 characters.

    ```jsx
    // Your ES6 code here
    
    console.log(checkLength("Programming")) // more than 5 characters 
    console.log(checkLength("Jeep")) // less than 5 characters 
    ```

6. Write a function that takes a number as input and determines if it is between 1 and 10.

    ```jsx
    // Your ES6 Code here
    
    console.log(isBetweenOneAndTen(5)); // true
    console.log(isBetweenOneAndTen(11)); // false
    ```

7. Write a function that takes a string as input and determines if it contains the word "hello".

    ```jsx
    // Your ES6 code here
    
    console.log(isHelloPresent("Hello World")) // true
    console.log(isHelloPresent("World")) // false
    ```

8. Write a function that takes a number as input and determines if it is a multiple of 3.

    ```jsx
    // Your ES6 code here
    
    console.log(isMultipleOfThree(5)); // false
    console.log(isMultipleOfThree(9)); // true
    ```

9. Write a function which takes in a number as input and returns it after multiplying by 10.

    ```jsx
    // Your ES6 code here
    
    console.log(multiplyByTen(20)) // 200
    console.log(multiplyByTen(40)) // 400
    ```

10. Console individual values of the product object using object destructuring.

    ```jsx
    const product = {
      title: "iPhone",
      price: 5999,
      description: "The iPhone is a smartphone developed by Apple"
    }
    
    // Your ES6 code here
    
    console.log(title); // iPhone
    console.log(price); // 5999
    console.log(description); // The iPhone is a smartphone developed by Apple
    ```

1. Create an object book with properties title, author, and pages. Create a function getBookDetails that takes a book object as a parameter and returns if the book has more than 100 pages.

    ```jsx
    // Your ES6 code here
    
    console.log(getBookDetails(book)) // logs 'true' if the pages are above 100
    console.log(getBookDetails(book)) // logs 'false' if the pages are 100 or below
    ```

2. Create a function changeOccupation that takes an object person and a string newOccupation as parameters, and changes the occupation property of the person object to the newOccupation. Log the person object to the console before and after calling the function.

    ```jsx
    // Your ES6 code here
    
    console.log(person); // logs { name: 'Amit', age: 25, occupation: 'Software Engineer' } to the console
    changeOccupation(person, 'Product Manager');
    console.log(person); // logs { name: 'Amit', age: 25, occupation: 'Product Manager' } to the console
    ```

3. Given an array numbers containing the numbers 1, 2, and 3. Use array destructuring to log each number to the console.

    ```jsx
    const numbers = [1, 2, 3];
    // Your ES6 code here
    
    console.log(a); // logs 1 to the console
    console.log(b); // logs 2 to the console
    console.log(c); // logs 3 to the console
    ```

4. Convert the given function into ES6 with least amount of characters.

    ```jsx
     function defaultParamsFunc(a, b, c) {
        if (c === undefined) {
            c = 4;
        }
        return a * b * c;
     };
     console.log(defaultParamsFunc(3, 1)); // 12
     console.log(defaultParamsFunc(3, 10)); // 120
    ```
