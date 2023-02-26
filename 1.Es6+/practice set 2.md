# ES6+ Practice Question Set 2

1. Create an object person with two properties, "name" and "age" and then updates the "age" property to a new value. Initial age should be 30.

    ```jsx
    // Your code here
    const person = {
    name: "Arpit",
    age: 30
    };

    person.age =35;
    console.log(person.age); // Output: 35
    ```

2. Write a function that takes an object car and returns true if the car is a sports car (i.e. has a horsepower property greater than or equal to 300)

    ```jsx
    //Your ES6 code here
    const isSportsCar = (car) => {
    return car.horsepower >= 300;
    }
    
    const car1 = { make: 'Porsche', model: '911', horsepower: 450 };
    const car2 = { make: 'Toyota', model: 'Camry', horsepower: 200 };
    console.log(isSportsCar(car1)); // true
    console.log(isSportsCar(car2)); // false
    ```

3. Write a function that takes an object person and a number num as arguments and returns true if the person's age plus num is greater than 21. Otherwise, it should return false.

    ```jsx
    // Your ES6 code here
    const isEligible = (person, num) => {
    return (person.age + num) > 21;
    };
    const person1 = { name: 'Ajay', age: 20 };

    console.log(isEligible(person1, 1)); // false
    console.log(isEligible(person1, 2)); // true
    ```

4. Write a function that takes an object blog and returns true if the blog has more than 1000 views (i.e. has a views property greater than 1000)

    ```jsx
    
    // Your ES6 code here
    const getViews = (blog) => {
      return blog.views > 1000;
    }

    
    const blog1 = {title: 'How to Learn JavaScript', author: 'John Doe', views: 1430};
    const blog2 = {title: '10 Reasons to Start a Blog', author: 'Jane Smith', views: 500};

    console.log(getViews(blog1)); // true
    console.log(getViews(blog2)); // false
    ```

5. Swap the values of two variables using array destructuring.

    ```jsx
    let a = 1;
    let b = 2;
    // Your ES6 Code here
    [a, b] = [b, a];
    console.log(a) // 2
    console.log(b) // 1
    ```

6. Convert this function into ES6 with least amount of characters.

    ```jsx
    function add(a = 30, b = 0) {
       return a + b;
     }
    
    console.log(add(2, 3));
    ```

    solution:

    ```jsx
    const add = (a = 30, b = 0) => a + b;
    console.log(add(2, 3)); // 5
    ```


7. Write an ES6 function combineObjects with least amount of characters which merges two objects into one.

    ```jsx
    // Your ES6 function here
    const combineObjects = (obj1, obj2) => ({ ...obj1, ...obj2 });
    
    const obj1 = {a: 1, b: 2};
    const obj2 = {c: 3, d: 4};
    const combinedObj = combineObjects(obj1, obj2);
    console.log(combinedObj);
    // Expected Output: {a: 1, b: 2, c: 3, d: 4}
    ```

8. Convert the function getData, into an ES6 function with last amount of characters.

    Hint: Destructuring

    ```jsx
    function getData(person) {
        const name = person.name;
      const address = person.address.city
        console.log(name); // John Doe
        console.log(address); // New York
    }
    
    const person = {
      name: 'John Doe',
      address: {
        city: 'New York',
        state: 'NY',
      },
    };
    getData(person);
    ```
    solution 

    ```jsx
    const getData = ({name, address: {city}}) => {
    console.log(name);
    console.log(city);
    };

    const person = {
    name: 'John Doe',
    address: {
        city: 'New York',
        state: 'NY',
    },
    };

    getData(person);
    ```

9. Write a function that takes a string as input and returns the string in all uppercase letters.

    ```jsx
    // Youe ES6 code here
    const stringToUpperCase = (str) => {
    const uppercase = { a: 'A', b: 'B', c: 'C', d: 'D', e: 'E', f: 'F', g: 'G', h: 'H', i: 'I', j: 'J', k: 'K', l: 'L', m: 'M', n: 'N', o: 'O', p: 'P', q: 'Q', r: 'R', s: 'S', t: 'T', u: 'U', v: 'V', w: 'W', x: 'X', y: 'Y', z: 'Z' };

    let result = '';

    for (let i = 0; i < str.length; i++) {
    const lowercaseChar = str[i];
    const uppercaseChar = uppercase[lowercaseChar]|| lowercaseChar;
    result += uppercaseChar ;
    }

     return result;
    }

    console.log(stringToUpperCase("hello")); // "HELLO"
    ```

10. Write a function that takes two strings as input and concatenates them together.

    ```jsx
    // Your ES6 code here
    
    console.log(concatenateStrings("hello", "world")); // "helloworld"
    ```

11. Write a function that takes an array and returns the last element in the array.

    ```jsx
    // Your ES6 code here
    
    console.log(lastElement([1, 2, 3, 4, 5])); // 5
    ```

12. Write a function that takes an array and returns the first element of the array.

    ```jsx
    // Your ES6 code here
    
    console.log(firstElement([1, 2, 3, 4, 5])); // 1
    ```

13. Write a function that takes an array and a number and returns the sum of first element and the number.

    ```jsx
    // Your ES6 code here
    
    console.log(sumFirstElement([1, 2, 3], 5)); // 6
    ```

14. Write a function that takes an array and returns the sum of first and last element.

    ```jsx
    // Your ES6 code here
    
    console.log(sumFirstAndLast([1, 2, 3, 4, 8])); // 9
    ```

15. Write a function that takes an object representing a person's information (name, age, occupation) and returns a template literal that includes the person's name and age in a sentence.
