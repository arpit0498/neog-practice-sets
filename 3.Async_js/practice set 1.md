# Async JS Practice Set 1

  **Instructions:**

    1. Specific instructions have been written for each question present in this set.
    2. Don’t use async-await in this set.
    3. Please follow ES6 norms for writing your functions.
    4. You can make use of some methods such as .length, toLowerCase(), toUpperCase() and .join() if needed.
    5. An example has been provided for fetch call related questions for your understanding.

1. Write a function ‘delayedGreeting’ that consoles a greeting message after a delay of 2 seconds using setTimeout. You can practice this question in any JS editor or your browser console.

    ```jsx
    // Your Code here
    function delayedGreeting() {

  setTimeout(function() {
    console.log("Hello, welcome to my portfolio!");
  }, 2000);
  }

    delayedGreeting();
    // Hello, welcome to my portfolio!
    ```

2. Write a function ‘delayedAddition’ that takes in two numbers and consoles their sum after a delay of 4 seconds using setTimeout. You can practice this question in any JS editor or your browser console.

    ```jsx
    // Your code here
    function delayedAddition(a, b) {

      setTimeout(function() {
        console.log(a + b);
      }, 4000);
    }

    delayedAddition(2, 3); 
    // 5
    ```

3. Write a function ‘delayAlert’ that takes in a message ‘Hello, world!’ and a delay time in milliseconds, and displays the message in an alert box after the specified delay time using setTimeout. You can practice this question in any JS editor or your browser console.

    ```jsx
    // Your Code here
    function delayedAlert(message, delayTime) {

    setTimeout(function() {
      alert(message);
    }, delayTime);
   }

    delayedAlert('Hello, world!', 2000);
    // Should display an alert box with the message, Hello, world!
    ```

4. Write a function delayedLoop that takes a number 3 and consoles a message 'Hello' three times after a delay of 1 second each, using a for-loop and setTimeout. You can practice this question in any JS editor or your browser console.

    ```jsx
    // Your Code here
    function delayedLoop(num) {

      for (let i = 1; i <= num; i++) {
        setTimeout(function() {
          console.log("Hello");
        }, i * 1000);
      }
    }

    delayedLoop(3);
    // should print Hello three times after 1 second each
    // Output:
    // Hello -- after 1 second
    // Hello -- after another 1 second
    // Hello -- after another 1 second
    ```

5. Make a fake fetch call that takes a message and a boolean value to get data and console the message received from the server. A fake fetch has been provided. You can practice this question in any JS editor or your browser console.

    ```jsx
    const fakeFetch = (msg, shouldSucceed) => {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          if (shouldSucceed) {
            resolve(`message from server: ${msg}`);
          }
          reject(`error from server: ${msg}`);
        }, 3000);
      });
    };
    
    // Your Code here
      fakeFetch("Hi", true)

    .then((data) => console.log(data))
    .catch((err) => console.log(err));
    // Hi -- after 3 seconds
    ```

6. EXAMPLE QUESTION: (Solution has been provided for this question for your understanding)

    Use this URL - <https://example.com/api/itemlist> to make a fake fetch call and handle errors if any. Show a proper message to the user on the DOM, as per the status and message received from the server. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.

    ```jsx
    const fakeFetch = (url) => {
     return new Promise((resolve, reject) => {
       setTimeout(() => {
         if (url === "https://example.com/api/itemlist") {
           reject({
             status: 404,
             message: "Items list not found."
           });
         } else {
           resolve({
             status: 200,
             data: {
               message: "Success",
               data: [
                 { itemName: "Bread", price: 30 },
                 { itemName: "Water Bottle", price: 50 },
                 { itemName: "Dairy Milk", price: 20 }
               ]
             }
           });
         }
       }, 2000);
     });
    }
    
    // Your Code here (Solution Given)
    const displayOutput = document.querySelector("#output");
    
    fakeFetch("https://example.com/api/itemlist")
      .then((response) => console.log(response))
      .catch((error) => {
        if (error.status === 404) {
          displayOutput.textContent =
            "The data you are looking for, does not exist.";
        }
      });
    
    // Output on the DOM should be: 
    // The data you are looking for, does not exist.
    ```

### Explanation

    In the above code solution, we are making a fakeFetch function call with the URL *`https://example.com/api/itemlist`*.

    If the Promise is resolved, the **`then`**method is executed with the successful response as the argument, and the console.log statement outputs the response object to the console.

    If the Promise is rejected, the **`catch`**method is executed with the error object as the argument, and the `if`statement checks if the error status is equal to 404. If the error status is 404, the message "The data you are looking for, does not exist." is displayed in the HTML element with ID "output".

7. Use this URL - <https://example.com/api/chat> to make a fake fetch call and handle errors if any. Show a proper message to the user on the DOM, as per the status and message received from the server. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.

  ```jsx
    const fakeFetch = (url) => {
     return new Promise((resolve, reject) => {
       setTimeout(() => {
         if (url === "https://example.com/api/chat") {
           reject({
             status: 503,
             message: "Service Unavailable"
           });
         } else {
           resolve({
             status: 200,
             data: {
               message: "Success"
             }
           });
         }
       }, 2000);
     });
    };
  // Your Code here
     const messageElem = document.getElementById("message");

      fakeFetch("https://example.com/api/chat")
        .then((response) => {
          const { status, data } = response;
          if (status === 200) {
            messageElem.innerText = data.message;
          } else {
            messageElem.innerText = `Unexpected status: ${status}`;
          }
        })
        .catch((error) => {
          messageElem.innerText = error.message;
        });
    // Output on the DOM should be: 
    // We are facing high demand at the moment. Please check back later in sometime.
  ```

8. Use this URL - <https://example.com/api/itemlist> to make a fake fetch call and list out all the items as an ordered list on the DOM. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.

```jsx
    const fakeFetch = (url) => {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          if (url === "https://example.com/api/itemlist") {
            resolve({
              status: 200,
              message: "Success",
              data: [
                { itemName: "Bread", price: 30, quantity: 10 },
                { itemName: "Water Bottle", price: 50, quantity: 50 },
                { itemName: "Dairy Milk", price: 20, quantity: 30 }
              ]
            });
          } else {
            reject({
              status: 404,
              message: "Items list not found."
            });
          }
        }, 2000);
      });
    };
    
    // Your Code here
    const displayItems = async () => {
  try {
    const response = await fakeFetch('https://example.com/api/itemlist');
    const items = response.data;

    items.forEach((item, index) => {
      console.log(`${index + 1}. ${item.itemName} -- INR ${item.price} -- ${item.quantity}`);
    });

  } catch (error) {
    console.error(`Error ${error.status}: ${error.message}`);
  }
};

// Call the function to display the items
displayItems();

    // Output on the DOM should be in the format, {itemName} -- INR {price} -- {quantity}:
    1. Bread -- INR 30 -- 10
    2. Water Bottle -- INR 50 -- 50
    3. Dairy Milk -- INR 20 -- 30
  ```

9. Use this URL - <https://example.com/api/data> to make a fake fetch call and handle errors if any. Show a proper message to the user on the DOM, as per the status and message received from the server. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.

    ```jsx
    const fakeFetch = (url) => {
     return new Promise((resolve, reject) => {
       setTimeout(() => {
         if (url === "https://example.com/api/data") {
           reject({
             status: 500,
             message: "Internal Server Error"
           });
         } else {
           resolve({
             status: 200,
             data: {
               message: "Success"
             }
           });
         }
       }, 2000);
     });
    };
    ```
    // Your Code here
    ```jsx
    <!-- HTML -->

    <div id="output"></div>
  
    // JavaScript

    const output = document.getElementById("output");

    fakeFetch("https://example.com/api/data")
      .then((response) => {
        output.innerText = response.data.message;
      })
      .catch((error) => {
        output.innerText = `Internal Server Error! The server crashed. Please try again in some time. Error Status: ${error.status}. Error Message: ${error.message}`;
      });

    // Output on the DOM should be: 
    // Internal Server Error! The server crashed. Please try again in some time.
    ```

10. Use this URL - <https://example.com/api/profile> to make a fake fetch call and handle errors if any. Show a proper message to the user on the DOM, as per the status and message received from the server. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.

```jsx
    const fakeFetch = (url) => {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          if (url === "https://example.com/api/profile") {
            reject({
              status: 401,
              message: "Unauthorized Access"
            });
          } else {
            resolve({
              status: 200,
              data: {
                message: "Success"
              }
            });
          }
        }, 2000);
      });
    };
```   
// Your Code here
```jsx    
    <!-- HTML code -->

    <div id="message"></div>
    // JS code

   fakeFetch("https://example.com/api/profile")
            .then((response) => {
              // Handle success response
              const messageEl = document.querySelector("#message");
              messageEl.textContent = response.data.message;
            })
            .catch((error) => {
              // Handle error response
              const messageEl = document.querySelector("#message");
              if (error.status === 401) {
                messageEl.textContent =
                  "Unauthorized Access! Looks like you are not logged in. Please login to see your profile data.";
              }
            });
        // Output on the DOM should be: 
        // Unauthorized Access! Looks like you are not logged in. Please login to see your profile data.
```

11. Use this URL - <https://example.com/api/profile/NC002> in which we are passing the id of a user to make a fake fetch call and display a welcome message to the user on the DOM. A fakeFetch has been provided. Use HTML, CSS & JS template in REPL or Vanilla template in CodeSandbox for this question.
```jsx
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/profile/NC002") {
        resolve({
          status: 200,
          data: {
            message: "Welcome, John!"
          }
        });
      } else {
        reject({
          status: 404,
          message: "User not found."
        });
      }
    }, 2000);
  });
};

const userId = "NC002";
const url = `https://example.com/api/profile/${userId}`;

fakeFetch(url)
  .then((response) => {
    const message = response.data.message;
    const welcomeMessage = document.createElement("h2");
    welcomeMessage.innerText = message;
    document.body.appendChild(welcomeMessage);
  })
  .catch((error) => {
    const message = error.message;
    const errorMessage = document.createElement("h2");
    errorMessage.innerText = message;
    document.body.appendChild(errorMessage);
  });
  
// Output on the DOM should be:
// Welcome, John!

```