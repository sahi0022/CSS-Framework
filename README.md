# Custom CSS Framework
Installation
Step 1: Clone the Repository
Start by cloning the repository to your local machine:


git clone https://github.com/sahi0022/CSS-Framework.git


Step 2: Include the CSS File in Your Project
After cloning the repository, link the compiled CSS file (custom-css-framework.css) in your HTML file:

<link rel="stylesheet" href="path/to/custom-css-framework.css">

Replace "path/to/custom-css-framework.css" with the actual path to the CSS file in your project.


Usage
Change Theme Colors
You can easily customize the default theme by modifying the variables in the _variables.scss file.

$primary-color: #3498db; // Change primary color

$secondary-color: #2ecc71; // Change Secondary color

$font-color: #333;   // Change font color

$font-family-base: 'Arial, sans-serif'; // Change font family 

Customize Components

The framework comes with reusable mixins, classes, and components.

Example:
You can adjust buttons using the button-style mixin:
.button-custom {
  @include button-style($primary-color);
}


Use Utility Classes
Here are some built-in utility classes you can use directly in your HTML:

Margin Utilities:
<div class="m-1 mt-1">This element has margin</div>

Padding Utilities:
<div class="p-1">This element has padding</div>

Text Utilities:
<p class="text-primary">This is a primary colored text</p>
<p class="text-secondary">This is a secondary colored text</p>



Compiling Sass to CSS
After customizing your Sass files, compile them into CSS.

Step 1: Install Node.js & Sass (if you haven’t already)
npm install -g sass

Step 2: Compile Sass
Navigate to the project root folder and run:

sass src/custom-css-framework.scss dist/custom-css-framework.css

This will compile the custom-css-framework.scss file into a CSS file in the dist folder.


PROJECT EXAMPLE : 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Custom CSS Framework</title>
    <link rel="stylesheet" href="./dist/custom-css-framework.css">
</head>
<body>
    <div class="container mt-5">
        <h1 class="fw-bold text-center">Welcome to Custom CSS Framework</h1>
        <p class="text-secondary text-center">Highlights the responsive design capabilities achieved through our custom CSS framework created with SCSS.</p>
        <section id="buttons" class="mt-3">
            <h2 class="text-secondary">Buttons</h2>
            <button class="btn-primary">Primary Button</button>
            <button class="btn-secondary">Secondary Button</button>
            <button class="btn-outline-primary">Outline Button</button>
        </section>        
        <section id="forms" class="mt-4 ">
            <h2>Forms</h2>
            <form>
 <input type="text" placeholder="Enter your name">
                <input type="email" placeholder="Enter your email">
                <select>
                    <option value="option1">Option 1</option>
                    <option value="option2">Option 2</option>
                </select>
                <textarea class="p-2"  placeholder="Your message"></textarea>
                <button class="btn-primary" type="submit">Submit</button>
            </form>
        </section>
        <section id="lists" class="mt-4">
            <h2 >Lists</h2>
            <ul class="row ">
                <li class="m-4">Item 1</li>
                <li class="m-4">Item 2</li>
                <li class="m-4">Item 3</li>
            </ul>
            <ol class="column">
                <li class="m-4">Ordered Item 1</li>
                <li class="m-4" >Ordered Item 2</li>
                <li class="m-4">Ordered Item 3</li>
            </ol>
        </section>
        <section id="tables" class="mt-4">
          <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Email</th>
                    <th>Phone Number</th>
                </tr>
            </thead>
<tbody>
                <tr class="text-center">
                    <td>John Doe</td>
                    <td>john.doe@example.com</td>
                    <td>(123) 456-7890</td>
                </tr>
                <tr class="text-center">
                    <td>Jane Smith</td>
                    <td>jane.smith@example.com</td>
                    <td>(987) 654-3210</td>
                </tr>
                <tr class="text-center">
                    <td>Michael Brown</td>
                    <td>michael.brown@example.com</td>
                    <td>(555) 123-4567</td>
                </tr>
            </tbody>
        </table>
        
        </section>
        <section id="utilities" class="mt-4 p-2  bg-white">
            <h2 >Utility Classes</h2>
            <div class="text-primary m-1">Primary Text with Margin</div>
            <div class="text-secondary p-2 border-rounded">Secondary Text with Padding and Rounded Border</div>
    </section>
        <section class="about-section mt-4">
          <h2>About Our Company</h2>
          <p class="bg-primary text-white p-2">
              Welcome to our company! We are dedicated to providing the highest quality products and services to our customers. Our team of experienced professionals works tirelessly to ensure that every aspect of your experience with us exceeds your expectations. With a commitment to innovation and excellence, we strive to lead in our industry and create lasting relationships with our clients.
          </p>
      </section>
      </div>
</body>
</html>
