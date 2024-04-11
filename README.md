# HTML Generator Project

This project is a simple HTML generator implemented in JavaScript. It dynamically creates HTML elements based on a predefined data structure. The generated HTML consists of parent elements with specified attributes and child elements nested within them.

## Usage

1. Clone or download the repository.
2. Open the `index.html` file in a web browser.

## How It Works

- The main functionality of the project is defined in the `index.html` file.
- It utilizes an array of objects called `fileData`, each representing a section of the HTML structure.
- Each object in `fileData` contains information about a parent HTML element, such as its tag name, attributes, and children elements.
- Child elements can have their own attributes and even event listeners, such as click events.
- The `generateElement` function iterates through the `fileData` array, creates HTML elements based on the provided data, and appends them to the document body.

## Features

- Dynamic generation of HTML elements based on a predefined data structure.
- Customizable attributes and event listeners for each HTML element.
- Easily extendable for more complex HTML structures.

## Example

```javascript
const fileData = [
  {
    element: 'div',
    attributes: [
      {
        class: 'parent',
        id: 'parent_1_id',
      },
    ],
    children: [
      {
        element: 'input',
        attributes: [
          {
            type: 'button',
            value: 'Try It!',
            class: 'child',
            id: 'child_1_id',
          },
        ],
        events: [
          {
            click: myFuncntion,
          },
        ],
      },
    ],
  },
  {
    element: 'div',
    attributes: [
      {
        class: 'parent',
        id: 'parent_2_id',
      },
    ],
    children: [
      {
        element: 'p',
        data: 'This is 2nd jsx',
        attributes: [
          {
            class: 'child',
            id: 'child_2_id',
          },
        ],
      },
    ],
  },
]

// Function to generate HTML elements
const generateElement = (element, parent) => {
  // Implementation of the generateElement function...
}

// Loop through fileData and generate HTML elements
for (let i = 0; i < fileData.length; i++) {
  generateElement(fileData[i], null)
}
