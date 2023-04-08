ReactJS Practice Question Set 7
Questions:#
Create a React component that fetches weather data from an API endpoint using useEffect hook and displays the current temperature, humidity, and wind speed on the screen using the useState hook. Add a button which toggles between Celsius and Fahrenheit units for the temperature.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/weather") {
        resolve({
          status: 200,
          message: "Success",
          data: {
            temperature: 21,
            humidity: 50,
            windSpeed: 10
          }
        });
      } else {
        reject({
          status: 404,
          message: "Weather data not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On clicking the button

Example

Create a React component that fetches user data from an API endpoint using useEffect hook and displays the user's name, email, and phone number on the screen using the useState hook. Add a button which toggles the display of the user's address (street, suite, city, zipcode).
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/user") {
        resolve({
          status: 200,
          message: "Success",
          data: {
            name: "John Doe",
            email: "john.doe@example.com",
            phone: "+1 555-555-5555",
            address: {
              street: "123 Main St",
              suite: "Suite 456",
              city: "Anytown",
              zipcode: "12345"
            }
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
Expected Output#
Example

On clicking the button

Example

Create a React component that fetches a list of movies from an API endpoint using useEffect hook and displays the title, year, and rating of each movie on the screen using the useState hook. Add a dropdown which filters the movies by year. You can keep 5 dropdown values - 2005 to 2010.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/movies") {
        resolve({
          status: 200,
          message: "Success",
          data: [
            { title: "The Dark Knight", year: 2008, rating: 9.0 },
            { title: "Inception", year: 2009, rating: 8.8 },
            { title: "Interstellar", year: 2010, rating: 8.6 },
            { title: "Tenet", year: 2009, rating: 7.5 },
            { title: "Real Steal", year: 2007, rating: 7.5 },
          ],
        });
      } else {
        reject({
          status: 404,
          message: "Movies list not found.",
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On typing the year, it will filter

Example

Create a React component that fetches a list of users from an API endpoint using useEffect hook and displays the name, email, and website of each user on the screen using the useState hook. Add a dropdown which filters the users by company name.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/users") {
        resolve({
          status: 200,
          message: "Success",
          data: [
            { name: "John Doe", email: "john@example.com", website: "example.com", company: "ABC Inc" },
            { name: "Jane Doe", email: "jane@example.com", website: "example.com", company: "XYZ Corp" },
            { name: "Bob Smith", email: "bob@example.com", website: "example.com", company: "ABC Inc" },
            { name: "Alice Brown", email: "alice@example.com", website: "example.com", company: "ACME Corp" },
            { name: "Charlie Green", email: "charlie@example.com", website: "example.com", company: "XYZ Corp" },
          ]
        });
      } else {
        reject({
          status: 404,
          message: "Users list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On typing the name, it will filter out

Example

Create a component that displays a random quote from an API using the useEffect and useState hooks. The component should fetch a new quote when the user clicks a button.
const fakeFetch = () => {
  const quotes = [
    {
      content: "Be yourself; everyone else is already taken.",
      author: "Oscar Wilde",
    },
    {
      content: "Two things are infinite: the universe and human stupidity; and I'm not sure about the universe.",
      author: "Albert Einstein",
    },
    {
      content: "So many books, so little time.",
      author: "Frank Zappa",
    },
    {
      content: "A room without books is like a body without a soul.",
      author: "Marcus Tullius Cicero",
    },
    {
      content: "In three words I can sum up everything I've learned about life: it goes on.",
      author: "Robert Frost",
    },
  ];

  return new Promise((resolve) => {
    setTimeout(() => {
      const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];
      resolve(randomQuote);
    }, 1000);
  });
};
Expected Output#
Example

Clicking the button will generate a new quote

Example

Create a React component that fetches a list of movies from an API endpoint using useEffect hook and displays the title, year, and genre of each movie on the screen using the useState hook. Add a dropdown which filters the movies by genre.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/movies") {
        resolve({
          status: 200,
          message: "Success",
          data: [
            {
              title: "The Godfather",
              year: 1972,
              genre: "Crime"
            },
            {
              title: "The Shawshank Redemption",
              year: 1994,
              genre: "Drama"
            },
            {
              title: "The Dark Knight",
              year: 2008,
              genre: "Action"
            },
            {
              title: "Forrest Gump",
              year: 1994,
              genre: "Comedy"
            },
            {
              title: "The Matrix",
              year: 1999,
              genre: "Science Fiction"
            },
            {
              title: "Jurassic Park",
              year: 1993,
              genre: "Science Fiction"
            },
            {
              title: "Star Wars: Episode IV - A New Hope",
              year: 1977,
              genre: "Science Fiction"
            },
            {
              title: "The Terminator",
              year: 1984,
              genre: "Action"
            },
            {
              title: "Die Hard",
              year: 1988,
              genre: "Action"
            },
            {
              title: "Pulp Fiction",
              year: 1994,
              genre: "Crime"
            }
          ]
        });
      } else {
        reject({
          status: 404,
          message: "Movies list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On typing the genre, it will filter out

Example

Create a React component that fetches a list of products from an e-commerce API endpoint using useEffect hook and displays the product name, description, price, and quantity on the screen using the useState hook. Add a button which allows the user to sort the products by price (lowest to highest).
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/products") {
        resolve({
          status: 200,
          message: "Success",
         data: {
            products: [
              {
                name: "Product 1",
                description: "This is the first product",
                price: 25.99,
                quantity: 10
              },
              {
                name: "Product 2",
                description: "This is the second product",
                price: 19.99,
                quantity: 15
              },
              {
                name: "Product 3",
                description: "This is the third product",
                price: 35.50,
                quantity: 5
              },
              {
                name: "Product 4",
                description: "This is the fourth product",
                price: 49.99,
                quantity: 20
              }
            ]
          }

        });
      } else {
        reject({
          status: 404,
          message: "Product list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On clicking the button it will sort it out by price

Example

Adding on to the previous question, There should be three buttons for this purpose: "Low to High", "High to Low", and "Reset". When the user clicks on "Low to High", the products should be sorted by price in ascending order. When the user clicks on "High to Low", the products should be sorted by price in descending order. When the user clicks on "Reset", the products should be displayed in their original order.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/products") {
        resolve({
          status: 200,
          message: "Success",
         data: {
            products: [
              {
                name: "Product 1",
                description: "This is the first product",
                price: 25.99,
                quantity: 10
              },
              {
                name: "Product 2",
                description: "This is the second product",
                price: 19.99,
                quantity: 15
              },
              {
                name: "Product 3",
                description: "This is the third product",
                price: 35.50,
                quantity: 5
              },
              {
                name: "Product 4",
                description: "This is the fourth product",
                price: 49.99,
                quantity: 20
              }
            ]
          }

        });
      } else {
        reject({
          status: 404,
          message: "Product list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

On click Low to High

Example

On click High to Low

Example

On click the Reset button

Example

Create a React component that uses the useEffect hook to fetch the product data from the API endpoint using the fakeFetch function provided below. The component should use the useState hook to store the fetched data and a second state variable to store the sorted data. The sorted data should be sorted in descending order by rating.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/products") {
        resolve({
          status: 200,
          message: "Success",
          data: {
            products: [
              { name: "Color Pencils", price: 50, quantity: 40, rating: 4.5 },
              { name: "Sketchpens", price: 110, quantity: 20, rating: 3.8 },
              { name: "Eraser", price: 20, quantity: 20, rating: 4.2 },
              { name: "Sharpener", price: 22, quantity: 30, rating: 4.7 }
            ]
          }

        });
      } else {
        reject({
          status: 404,
          message: "Product list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example

Adding on to the previous question, Add a search bar to the component that allows users to filter the products by name. The search bar should update the list of displayed products in real-time as the user types. The search functionality should be case-insensitive.
const fakeFetch = (url) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (url === "https://example.com/api/products") {
        resolve({
          status: 200,
          message: "Success",
          data: {
            products: [
              { name: "Color Pencils", price: 50, quantity: 40, rating: 4.5 },
              { name: "Sketchpens", price: 110, quantity: 20, rating: 3.8 },
              { name: "Eraser", price: 20, quantity: 20, rating: 4.2 },
              { name: "Sharpener", price: 22, quantity: 30, rating: 4.7 }
            ]
          }

        });
      } else {
        reject({
          status: 404,
          message: "Product list not found."
        });
      }
    }, 2000);
  });
};
Expected Output#
Example
