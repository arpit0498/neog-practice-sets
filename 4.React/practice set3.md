# ReactJS Practice Question Set 3

## Instructions:
    Do these questions in a React JS template editor. You can use React JS CodeSandbox or React JS REPL.
    This set is about practicing JSX, conditional styling and use of useState hook in React.
    You can make use of methods such as .map(), .filter(), .reduce(), .length, .toLowerCase(), .toUpperCase() wherever needed.
    Do NOT use for-loops.

1.Build a React component which takes an image, image height and image width as props and sets the height and width of the image and displays the image on DOM. Image link - `<https://picsum.photos/200>`

2.Given an array of objects with cartoon character details as: id, name, superpower, magnitude. Build a React component and display all details of those characters whose magnitude is greater than 5. Data:
```jsx
const cartoons = [
{
    id: 1,
    name: 'Mickey Mouse',
    superpower: 'Invisibility',
    magnitude: 1
  },
  {
    id: 2,
    name: 'Spongebob Squarepants',
    superpower: 'Super Strength',
    magnitude: 3
  },
  {
    id: 3,
    name: 'Bugs Bunny',
    superpower: 'Teleportation',
    magnitude: 9
  },
  {
    id: 4,
    name: 'Tom and Jerry',
    superpower: 'Intelligence',
    magnitude: 8
  },
  {
    id: 5,
    name: 'The Powerpuff Girls',
    superpower: 'Flight',
    magnitude: 10
  }
]
```
3.Use the cartoons data from above question (2) and build a React component to display only the names of characters whose magnitude is an even number. Use h1 tag to display names. Pass the entire data as props.

4.Use the cartoons data from above question (2) and build a React component that takes the superpower ”Intelligence”, as prop and display the details of the character having that super power. Show details on DOM in the format “name - superpower - magnitude”.

5.Build a React component to display the list of all the vegetables and their pick date as ordered list. Create a button which says “Highlight Fresh Vegetables”. On click of the button change the color of the vegetable to green whose pick date is ‘2023-03-30’.

Data:
```jsx
const vegetables = [
  {
    id: 1,
    name: 'Carrots',
    pickDate: '2023-03-25',
  },
  {
    id: 2,
    name: 'Broccoli',
    pickDate: '2023-03-30',
  },
  {
    id: 3,
    name: 'Peppers',
    pickDate: '2023-03-25',
  },
  {
    id: 4,
    name: 'Tomatoes',
    pickDate: '2023-03-27',
  },
  {
    id: 5,
    name: 'Ladies Finger',
    pickDate: '2023-03-30',
  },
]
```

6.Build a React component which takes an array of objects as props. The object represents a bouquet of mixed flowers and consists of: id, flowers, totalFlowers, and price. Display the price of that bouquet on the DOM that has rose in it, in the format, “Price of bouquet with roses : {price}”

Data:
```jsx
const bouquet = [
  {
    id: 1,
    flowers: ['rose', 'lily', 'marigold'],
    totalFlowers: 9,
    price: 1400,
  },
  {
    id: 2,
    flowers: ['snapdragon', 'sunflower'],
    totalFlowers: 10,
    price: 3400,
  },
]
```
7.Build a React component to display the flowers of a bouquet in an ordered list on the DOM which has a price above 2000. Pass data as prop.

Data:
```jsx
const bouquet = [
  {
    id: 1,
    flowers: ['rose', 'lily', 'marigold'],
    totalFlowers: 9,
    price: 1400,
  },
  {
    id: 2,
    flowers: ['snapdragon', 'sunflower'],
    totalFlowers: 10,
    price: 3400,
  },
]

// Expected Output
// 1. snapdragon
// 2. sunflower
```

8.Given an array of objects representing people who donated money to the NGO. Each object consists of: id, name, amount. Build a React component that takes the data as props and shows the total donation collected on the DOM. Output should be in the format: `Total Donation Collected: _amount_`

Data:

```jsx
const DonationData = [
  {
    id: 1,
    name: 'Nitin',
    Donation: 7800,
  },
  {
    id: 2,
    name: 'Mehak',
    Donation: 9500,
  },
  {
    id: 3,
    name: 'Mehul',
    Donation: 65000,
  },
  {
    id: 4,
    name: 'Nina',
    Donation: 560,
  },
]
```
9.Given an array of objects representing a list of cars. Each object consists of: id, name, price, category. Build a React component that shows on the DOM the total number of cars present in each category. For Example: if there are categories, luxury and sports, where there are 5 luxury cars and 2 sports car then the data should be represented as:

`luxury: 5`

`sports: 2`

Data:
```jsx
const cars = [
  {
    id: 1,
    name: 'supra',
    price: 500000,
    category: 'sports',
  },
  {
    id: 2,
    name: 'A5',
    price: 700000,
    category: 'luxury',
  },
  {
    id: 3,
    name: 'huyara',
    price: 1500000,
    category: 'sports',
  },
  {
    id: 4,
    name: 'agera R',
    price: 3500000,
    category: 'sports',
  },
]
```

10.Create an array of objects representing students marks out of 100. Each object consists of: id, name and marks. Build a React component that calculates the mean marks of all the students to see if the institute passes the criteria of the certification.

If the mean is above 80, display on the DOM `Certification Approved`

If the mean is below 80, display on the DOM `Certification Not Approved`

Data:
```jsx
const studentData = [
  {
    id: 1,
    name: 'Nitin',
    marks: 78,
  },
  {
    id: 2,
    name: 'Mehak',
    marks: 95,
  },
  {
    id: 3,
    name: 'Mehul',
    marks: 65,
  },
  {
    id: 4,
    name: 'Nina',
    marks: 56,
  },
]
```