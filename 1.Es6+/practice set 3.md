# ES6+ Practice Question Set 3

1. Create a function that takes an array of strings as an argument and returns a string that includes the number of items in the array and the first and last items.

    ```jsx
    
    // Your ES6 code here
    const formatArray = (arr) => {
    const length = arr.length;
    const firstItem = arr[0];
    const lastItem = arr[length - 1];
    return `The array has ${length} items, and the first item is "${firstItem}", and the last item is "${lastItem}".`;
    };
    
    const items = ['apple', 'banana', 'orange'];
    const message = formatArray(items);
    console.log(message);
    // The array has 3 items, and the first item is "apple", and the last item is "orange".
    ```
    ```jsx
    const formatArray = (arr) => {

    if (arr.length === 0) {
        return "The array is empty.";
        } else if (arr.length === 1) {
            return `The array has 1 item, and it is "${arr[0]}".`;
        } else {
            return `The array has ${arr.length} items, and the first item is "${arr[0]}", and the last item is "${arr[arr.length - 1]}".`;
        }
    }


    ```

2. Create a function that takes a product object as an argument and returns a string that includes the product name, price, and a message based on whether it is in stock or not.

    ```jsx
    // Your ES6 code here
    const formatProduct = (product) => {
    const { name, price, inStock } = product;
    const stockMessage = inStock ? "is in stock" : "is not in stock";
    return `${name} costs INR ${price} and ${stockMessage}.`;
    };
    const product = {
      name: 'Socks',
      price: 249,
      inStock: true,
    };
    
    const message = formatProduct(product);
    console.log(message);
    // Socks costs INR 249 and is in stock.
    ```

3. Write a function findPerson that takes an array of person objects and a name as parameters and returns the object with the matching name, or null if not found.

    ```jsx
    // Your ES6 code here 
    const findPerson = (people, name) => {
    return people.find(person => person.name === name) || null;
    };
    console.log(findPerson([{ name: 'Amay', age: 25 }, { name: 'Akhil', age: 25 }], "Akhil"))
    ```
    ```jsx
    // Using for loop 
    const findPerson = (people, name) => {

    for (let i = 0; i < people.length; i++) {
        if (people[i].name === name) {
        return people[i];
        }
    }
    return null;
    };

    console.log(findPerson([{ name: 'Amay', age: 25 }, { name: 'Akhil', age: 25 }], "Akhil"));
    // Output: { name: 'Akhil', age: 25 }
    ```


4. Write a function that uses destructuring to extract the first two elements from an array, and returns them in an object with keys 'first' and 'second'.

    ```jsx
    // Your ES6 code here
    const pickFirstAndSecond = (arr) => {

    const [first, second] = arr;
    return { first, second };
    };

    console.log(pickFirstAndSecond(["orange", "banana", "apple"]))
    // {first: 'orange', second: 'banana'}
    
    console.log(pickFirstAndSecond(["red", "blue", "green"]))
    // {first: 'red', second: 'blue'}
    ```

5. Convert the following code to ES6+ syntax with minimum number of characters.

    ```jsx
    function startsWithA(str) {
      if(str.charAt(0) === 'A') {
      return true;
     } else {
      return false
     }
    }
    
    console.log(startsWithA("Akshita"))
    // true
    console.log(startsWithA("Jeena"))
    // false
    ```

    **solution**

    ```jsx

    const startsWithA = str => str[0] === 'A';

    console.log(startsWithA("Akshita"))
    // true
    console.log(startsWithA("Jeena"))
    // false
    ```

6. Write an ES6 function to return only the first character of the given array.

    ```jsx
    // Your ES6 code here
    const printFirstCharacter = arr => arr[0];
    console.log(printFirstCharacter([1, 2, 3, 5, 8]))
    // 1
    ```

7. Write a function to return the last 5 characters as an array from the given array.

    ```jsx
    // Your ES6 code here
    const printLastFive = arr => arr.slice(-5);

    console.log(printLastFive([0, 1, 1, 2, 3, 5, 8]))
    // [1, 2, 3, 5, 8]
    ```

    ```jsx
    // Without using in-built function
    const printLastFive = arr => {
    const result = [];
    for (let i = arr.length - 5; i < arr.length; i++) {
        if (i >= 0) {
        result.push(arr[i]);
        }
    }
    return result;
    };

    console.log(printLastFive([0, 1, 1, 2, 3, 5, 8])); // [1, 2, 3, 5, 8]
    ```

8. Write an ES6 function to return the second element of the given array by multiplying 20 to it.

    ```jsx
    // Your ES6 code here
    const printSecondCharacter = arr => {
    return arr[1] * 20;
    };

    console.log(printSecondCharacter([1, 2, 3, 5, 8]))
    // 40
    ```

9. Write an ES6 function to return the second element of the given array by adding “Hello” before it.

    ```jsx
    // Your ES6 code here
    const sayHello = arr => {
    return `Hello ${arr[1]}`;
    };

    console.log(sayHello(["Akshay", "Sweta", "Prerana", "Vinay"]))
    // Hello Sweta
    
    console.log(sayHello(["Kanika", "Rakesh", "Prerana", "Puja"]))
    // Hello Rakesh
    ```

10. Write an ES6 function to return sum of all numbers at even indices of the given array.

    ```jsx
    // Your ES6 code here
    const sumOfEvenIndices = (arr) => {
    let sum = 0;
    for (let i = 0; i < arr.length; i += 2) {
        sum += arr[i];
    }
    return sum;
    };
    
    console.log(sumOfEvenIndices([2, 4, 3, 7, 1, 5])) // 6
    console.log(sumOfEvenIndices([12, 14, 3, 27, 15, 25])) // 30
    ```

11. Write an ES6 function to return the sum of only first 2 elements of the array .

    ```jsx
    // Your ES6 code here
    function sumFirstTwoElements(arr) {
    return arr[0] + arr[1];
    }
    
    console.log(sumFirstTwoElements([10, 4, 3, 7, 1, 5])) // 14
    console.log(sumFirstTwoElements([12, 14, 3, 27, 15])) // 26
    ```

12. Write an ES6 function to return the first element which is a multiple of 5 in the given array.

    ```jsx
    // Your ES6 code here
    function printMultipleOfFive(arr) {
    for (let i = 0; i < arr.length; i++) {
        if (arr[i] % 5 === 0) {
        return arr[i];
        }
    }
    return null;//no element is multiple of 5
    }

    console.log(printMultipleOfFive([7, 4, 10, 7, 5, 3])) // 10
    console.log(printMultipleOfFive([7, 5, 10, 7, 15, 3])) // 5
    ```

13. Create a function which takes in the given object and returns another object only with the properties postalCode and city in it.

    ```jsx
    // Your ES6 code here
    const getAddress = ({postalCode, city}) => ({postalCode, city});

    const userData = {
      name: 'Jane Doy',
      postalCode: '12134',
      city: 'Germany',
    }
    
    console.log(getAddress(userData));
    // {postalCode: '12134', city: 'Germany'}
    ```

14. Create a function which takes in the given object and returns a sentence which indicates name of the person and where the person lives.

    ```jsx
    // Your ES6 code here
    const printData = ({ name, country }) => `${name} lives in ${country}`;
    
    const userData1 = {
      name: 'Gaurav',
      postalCode: '12134',
      country: 'Japan',
    }
    console.log(printData(userData1)); // Gaurav lives in Japan
    
    const userData2 = {
      name: 'Pritam',
      postalCode: '560223',
      country: 'India',
    }
    console.log(printData(userData2)); // Pritam lives in India
    ```

15. Create a function which takes a product object and returns a sentence about the product using ES6 features.
    ```jsx
    const productData = {

    name: 'IQoo Smartphone',
    price: 48000,
    quantity: 10,
    description: 'A Gaming smartphone with all the latest features.',
    };

    const printProductData = (product) => {
    const {name, price, quantity, description} = product;
    return `${name} is available at a price of INR ${price}. We have only ${quantity} units in stock. Description: ${description}`;
    };

    console.log(printProductData(productData));

    ```