# ES6+ Practice Question Set 4

**Instructions:** Avoid usage of in-built methods in javaScript. You can make use of basic methods such as .length, toLowerCase(), toUpperCase() if needed. Make use of for-loops and if-else statements wherever needed.

1. Write an ES6 function that accepts an array of integers and returns the maximum element in the array. Avoid using in-built methods.

    ```jsx
    // Your ES6 code here
    const getMaxElement = (arr) => {

    let max = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
        max = arr[i];
        }
    }
    return max;
    };

    let array = [4,78,8,3,6,0,12,34]
    console.log(getMaxElement(array)) // 78
    ```

2. Write an ES6 function that takes an array of numbers and returns the average of all the numbers. Avoid using in-built methods.

    ```jsx
    // Your ES6 code here
    const calculateAverage = (arr) => {

    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum / arr.length;
    };

    console.log(calculateAverage([1, 2, 3, 4, 5])); // 3
    ```

3. write an ES6 function that takes an array of numbers and converts even numbers to odd numbers by adding 1 to that number.

    ```jsx
    // Your ES6 code here
    const convertEvenToOdd = (arr) => {
    const result = Array(arr.length);
    for (let i = 0; i < arr.length; i++) {
        const num = arr[i];
        if (num % 2 === 0) {
        result[i] = num + 1;
        } else {
        result[i] = num;
        }
    }
    return result;
    };

    
    var numArr = [1, 2, 3, 4, 5, 6, 7, 8, 9];
    console.log(convertEvenToOdd(numArr));
    // [1, 3, 3, 5, 5, 7, 7, 9, 9]
    ```

1. write an ES6 function that takes an array of words and returns an array with all its elements whose length is greater than 5.

    ```jsx
    // Your ES6 code here
    const filterWords = (words) => {

    let result = [];
    let resultIndex = 0;
    for (let i = 0; i < words.length; i++) {
        const word = words[i];
        if (word.length > 5) {
        result[resultIndex] = word;
        resultIndex++;
        }
    }
    return result;
    };

    var words = ["eat", "sleep", "code", "repeat", "neog", "community"];
    console.log(filterWords(words)) // ["repeat", "community"]
    ```

2. Write an ES6 function that takes an array of strings and returns a new array with each string capitalized.

    ```jsx
    // Your ES6 code here
    const capitalizeWords = (arr) => {

    // Use the map() method to iterate over the array and capitalize each string
    const capitalizedArr = arr.map((str) => {
        return str.toUpperCase();
    });
    
    return capitalizedArr;
    };
    console.log(capitalizeWords(["eat", "sleep", "code", "repeat"]))
    // ["EAT", "SLEEP", "CODE", "REPEAT"]
    ```

1. Write an ES6 function that takes an array of objects and a property name and returns a new array with only the values of that property. Avoid using in-built methods.

    ```jsx
    // Your ES6 code here
    const getValues = (arr, prop) => {
    let values = [];
    for (let i = 0; i < arr.length; i++) {
        let obj = arr[i];
        let value = obj[prop];
        values[i] = value;
    }
    return values;
    };

    console.log(
      getValues(
        [
          { name: "John", age: 21 },
          { name: "Mary", age: 22 },
          { name: "Peter", age: 23 },
        ],
        "name"
      )
    ); // ["John", "Mary", "Peter"]
    ```

2. Write an ES6 function that takes the users' details and returns the data with team ID. Avoid using in-built methods.

    ```jsx
    // Your ES6 code here
    
    const userData = { firstName : "John", lastName: "Dee" }
    console.log(podAndTeamAllocation(userData))
    // {firstName: 'John', lastName: 'Dee', teamId: 667543}
    ```

3. Write an ES6 function which checks if a student already has a team. If team is not given then add them to team “A” and return the object else do nothing and return the same object. Avoid using in-built methods.

    ```jsx
    // Your ES6 code here
    function checkForTeam(student) {

    // Check if the student has a `team` property
    if (student.team === undefined) {
       
        student['team'] = 'A'; // If not, add a `team` property with the value 'A'
    }
    
    // Return the updated student object
    return student;
    }

    console.log(checkForTeam({firstName: 'Penn', lastName: 'Ma'}))
    // {firstName: 'Penn', lastName: 'Ma', team: A}
    
    console.log(checkForTeam({firstName: 'John', lastName: 'Dee', team:'B'}))
    // {firstName: 'John', lastName: 'Dee', team: B}
    
    console.log(checkForTeam({firstName: 'Priya', lastName: 'Raj'}))
    // {firstName: 'Priya', lastName: 'Raj', team: A}
    ```

4. Destructure the following code to get the desired outputs. Avoid using in-built methods.

    ```jsx
    const book = { 
      title: 'JavaScript: The Definitive Guide',  
      authors: [{name: 'David Flanagan', age: 49 }, { name: 'Yukihiro Matsumoto', age: 57 }],  
      publisher: {name: 'O\'Reilly Media', location: 'CA'}
    };
    
    // Your ES6 code here
    
    console.log(title); // JavaScript: The Definitive Guide
    console.log(author1); // David Flanagan 
    console.log(author2); // Yukihiro Matsumoto
    console.log(publisherName); // O'Reilly Media
    ```

    solution
    ```jsx
    const book = { 
      title: 'JavaScript: The Definitive Guide',  
      authors: [{name: 'David Flanagan', age: 49 }, { name: 'Yukihiro Matsumoto', age: 57 }],  
      publisher: {name: 'O\'Reilly Media', location: 'CA'}
    };

    const { title, authors: [{ name: author1 }, { name: author2 }], publisher: { name: publisherName } } = book;

    
    console.log(title); // JavaScript: The Definitive Guide
    console.log(author1); // David Flanagan
    console.log(author2); // Yukihiro Matsumoto
    console.log(publisherName); // O'Reilly Media


    ```

5. Write an ES6 function that takes an array of objects and returns the sum of all ages.

    ```jsx
    // Your ES6 code here
    const sumOfAges = (array) => {

    let sum = 0;
    for (let i = 0; i < array.length; i++) {
        sum += array[i].age;
    }
    return sum;
    };
    var array = [
     {
      name: "Jay",
      age: 60
     },
     {
      name: "Gloria",
      age: 36
     },
     {
      name: "Manny",
      age: 16
     },
     {
      name: "Joe",
      age: 9
     }
    ];
    
    console.log(sumOfAges(array)); // 121
    ```
