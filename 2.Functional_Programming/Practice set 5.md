# Functional Programming Set 5 (ReactJS)

**Instructions:**

1. Make use of **React JS** **template** in CodeSandbox and **.map()** method in this set. This is not a React JS exercise. There will be **no use of useState or any other React hook**.
2. You can make use of basic methods such as .length, toLowerCase(), toUpperCase() if needed.
3. Do NOT use for-loops.
4. An example has been provided for your understanding. You can find the practice questions below this example.
5. Create your own data for the practice questions where ever needed. You can see the example for reference.

Level UP! Happy Coding. 😊

## Example

You are building a shopping cart app with React. You have an array of objects called items, representing the items in the cart, with each object having the following properties:

```jsx
const items = [
{ id: 1, name: 'Book', price: 10 },
{ id: 2, name: 'T-Shirt', price: 15 },
{ id: 3, name: 'Hat', price: 8 },
{ id: 4, name: 'Sunglasses', price: 12 },
];
```

You also have a variable called total, that contains the total price of all the items in the cart:

```jsx
const total = 45;
```

Using React's map method, write code that generates an unordered list (ul) with one list item (li) for each item in the items array. Each list item should display the item's name and price in the following format:

```jsx
[Item Name]: ([Item Price])
```

The li elements should be wrapped in a div element that contains a heading (h1) with the text "Shopping Cart" and a paragraph (p) that displays the total price in the following format:

```markdown

Total: [Total Price]
```

The li elements should each have a unique key attribute based on the item's id property.

### Solution

```jsx
const items = [
  { id: 1, name: 'Book', price: 10 },
  { id: 2, name: 'T-Shirt', price: 15 },
  { id: 3, name: 'Hat', price: 8 },
  { id: 4, name: 'Sunglasses', price: 12 },
];

const total = 45;

function ShoppingCart() {
  return (
    <div>
      <h1>Shopping Cart</h1>
      <ul>
        {items.map(item => (
          <li key={item.id}>
            {item.name}: ({item.price})
          </li>
        ))}
      </ul>
      <p>Total: {total}</p>
    </div>
  );
}
```

## Practice questions

1. Create an array of objects representing movies in your watchlist. Each object has the following properties: id, title and director. Write a React component that takes the array of movies as input and returns an unordered list of movies, where each list item displays the movie's title and director.

2. Create an array of objects representing products in an online store. Each object has the following properties: id, name, price, and category. Write a React component that takes the array of products as input and returns an unordered list of products, where each list item displays the product's name, price, and category.

3. Create an array of objects representing books in a library. Each object has the following properties: id, title, author, and rating. Write a React component that takes the array of books as input and returns an unordered list of books, where each list item displays the book's title, author, and rating.

4. Create an array of objects representing employees in a company. Each object has the following properties: id, name, department, and salary. Write a React component that takes the array of employees as input and returns an unordered list of employees, where each list item displays the employee's name, department, and salary.

5. Create an array of objects representing recipes in a cookbook. Each object has the following properties: id, recipe name, recipe creator name. Write a React component that takes the array of recipes as input and returns an unordered list, where each list item displays the recipe's name and recipe creator name.

6. Create an array of objects representing cars in a dealership. Each object has the following properties: id, make, model, and price. Write a React component that takes the array of cars as input and returns an unordered list of cars, where each list item displays the car's make, model, and price.

7. Create an array of objects representing students in a class. Each object has the following properties: id, name, grade, and attendance. Write a React component that takes the array of students as input and generates an ordered list of students, where each list item displays the student's name, grade, and attendance.

8. Create an array of objects representing movies in your watchlist. Each object has the following properties: id, title, director, and runtime. Write a React component that takes the array of movies as input and generates an ordered list of movies, where each list item displays the movie's title, director, and runtime.

9. Create an array of objects representing products in an online store. Each object has the following properties: id, name, price, and category. Write a React component that takes the array of products as input and generates an ordered list of products, where each list item displays the product's name, price, and category.

10. Create an array of objects representing recipes in a cookbook. Each object has the following properties: id, name, ingredients, and instructions. Write a React component that takes the array of recipes as input and generates an ordered list of recipes, where each list item displays the recipe's name, ingredients, and instructions. Data has been provided below for this questions.

```jsx
const recipes = [  
 { 
  id: 1,    
  name: "Spaghetti with Meatballs",    
  ingredients: [      
   "1 lb spaghetti",      
   "1 lb ground beef",     
   "1 cup breadcrumbs",      
   "1 egg",      
   "1/4 cup chopped parsley",      
   "1/4 cup grated Parmesan cheese",      
   "1/4 cup milk",      
   "1/2 teaspoon salt",      
   "1/2 teaspoon black pepper",      
   "2 tablespoons olive oil",      
   "1 onion, chopped",      
   "3 cloves garlic, minced",      
   "1 can (28 oz) crushed tomatoes",      
   "1 teaspoon sugar",      
   "1/4 teaspoon red pepper flakes",      
   "1/4 cup chopped fresh basil",    
  ],
    instructions: [
      "1. Cook the spaghetti according to package instructions until al dente.",
      "2. In a large bowl, combine the ground beef, breadcrumbs, egg, parsley, Parmesan, milk, salt, and pepper. Mix until well combined and form into meatballs.",
      "3. In a large skillet, heat the olive oil over medium heat. Add the onion and garlic and cook until softened, about 5 minutes.",
      "4. Add the crushed tomatoes, sugar, and red pepper flakes. Bring to a simmer and add the meatballs. Cover and simmer for 15-20 minutes, until the meatballs are cooked through.",
      "5. Serve the meatballs and sauce over the cooked spaghetti. Garnish with fresh basil.",
    ],
  },
  {
    id: 2,
    name: "Chocolate Chip Cookies",
    ingredients: [
      "2 1/4 cups all-purpose flour",
      "1 teaspoon baking soda",
      "1 teaspoon salt",
      "1 cup unsalted butter, at room temperature",
      "3/4 cup white sugar",
      "3/4 cup brown sugar",
      "2 large eggs",
      "2 teaspoons vanilla extract",
      "2 cups semisweet chocolate chips",
    ],
    instructions: [
      "1. Preheat the oven to 375 degrees F (190 degrees C). Line a baking sheet with parchment paper.",
      "2. In a medium bowl, whisk together the flour, baking soda, and salt.",
      "3. In a large bowl, beat together the butter, white sugar, and brown sugar until light and fluffy, about 2-3 minutes.",
      "4. Add the eggs one at a time, beating well after each addition. Stir in the vanilla extract.",
      "5. Gradually add the dry ingredients to the wet ingredients, mixing until just combined.",
      "6. Stir in the chocolate chips.",
      "7. Drop the dough by rounded tablespoons onto the prepared baking sheet, spacing the cookies about 2 inches apart.",
      "8. Bake for 10-12 minutes, until the edges are golden brown and the centers are set.",
      "9. Cool the cookies on the baking sheet for 5 minutes, then transfer to a wire rack to cool completely.",
    ],
  },
];
```
