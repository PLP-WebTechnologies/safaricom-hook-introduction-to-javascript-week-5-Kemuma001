### **Assignment: Exploring JavaScript Fundamentals and DOM Manipulation** 🌟

---

#### **Objective:**
This assignment aims to test your understanding of JavaScript basics, control structures, and the Document Object Model (DOM). You will demonstrate your skills by creating an interactive webpage that uses variables, data types, operators, control structures, and DOM manipulation.

---

### **Instructions:**

1. **Create a new HTML file** and include an external JavaScript file for your script.  
2. Name your HTML file as `assignment.html` and your JavaScript file as `script.js`.  
3. Follow the tasks below and ensure you structure your code for readability with proper comments.  

---

### **Tasks:**

#### **Part 1: JavaScript Basics**

1. **Variables and Data Types**:
   - Declare variables of different types: string, number, boolean, array, and object.  
   - Use `console.log()` to print their values and types in the browser console.  

   **Example Output**:  
   ```
   Name: John Doe (Type: string)  
   Age: 25 (Type: number)  
   Is student: true (Type: boolean)





                            <!DOCTYPE html>
                                       <html lang="en">
                                           <head>
                                   <meta charset="UTF-8">
                                   <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                   <title>Assignment: JavaScript Basics</title>
                                      </head>
                                          <body>
                                   <h1>JavaScript Basics - Variable Declaration and Data Types</h1>
                                  <p>Check your browser console for the output.</p>

                               <!-- Link to the external JavaScript file -->
                                 <script src="script.js"></script>
                                 </body>
                                  </html>






                              // Part 1: JavaScript Basics - Variables and Data Types

                                  // 1. Declare variables of different types:

                                           // String
                                let greeting = "Hello, World!";

                               // Number
                                 let age = 25;

                             // Boolean
                                        let isStudent = true;

                           // Array
                                        let favoriteColors = ["red", "blue", "green"];

                         // Object
                                       let person = {
                                        name: "John Doe",
                                          age: 30,
                                         job: "Web Developer"
                                                   };

                       // 2. Use console.log() to print their values and types:

                              // Printing string value and its type
                                   console.log("String value: " + greeting);
                                   console.log("Type of greeting: " + typeof greeting);

                            // Printing number value and its type
                                   console.log("Number value: " + age);
                                   console.log("Type of age: " + typeof age);

                          // Printing boolean value and its type
                                  console.log("Boolean value: " + isStudent);
                                  console.log("Type of isStudent: " + typeof isStudent);

                        // Printing array value and its type
                                 console.log("Array value: " + favoriteColors);
                                 console.log("Type of favoriteColors: " + typeof favoriteColors);

                       // Printing object value and its type
                                 console.log("Object value: ", person);
                                 console.log("Type of person: " + typeof person);




2. **Operators**:
   - Write a simple calculator function that performs addition, subtraction, multiplication, and division using two numbers provided by the user (use `prompt()` for input).  
   - Use arithmetic and comparison operators to validate user input and display appropriate messages.

   **Example Output**:  
   ```
   Enter the first number: 10  
   Enter the second number: 2  
   Choose an operation (+, -, *, /): *  
   Result: 20
   ```


            <!DOCTYPE html>
                <html lang="en">
                       <head>
                          <meta charset="UTF-8">
                          <meta name="viewport" content="width=device-width, initial-scale=1.0">
                            <title>Simple Calculator</title>
                            </head>
                              <body>
                         <h1>Simple Calculator</h1>
                          <p>Open the browser's developer tools to see the output.</p>

                     <!-- Link to the external JavaScript file -->
                         <script src="script.js"></script>
                            </body>
                                </html>




                                  // Simple Calculator Function
                                       function simpleCalculator() {
                                    // Prompt user for two numbers
                                        let num1 = parseFloat(prompt("Enter the first number:"));
                                        let num2 = parseFloat(prompt("Enter the second number:"));

                                   // Validate user input to ensure both inputs are numbers
                                        if (isNaN(num1) || isNaN(num2)) {
                                         console.log("Error: Please enter valid numbers.");
                                          return; // Exit the function if input is invalid
                                                        }

                                 // Prompt user to select an operation
                                           let operation = prompt("Choose an operation: +, -, *, /");

                                // Perform the operation based on user input
                                           let result;

                                         if (operation === '+') {
                                             result = num1 + num2;
                                              } else if (operation === '-') {
                                              result = num1 - num2;
                                       } else if (operation === '*') {
                                             result = num1 * num2;
                                       } else if (operation === '/') {
                          // Check for division by zero
                                       if (num2 === 0) {
                                           console.log("Error: Division by zero is not allowed.");
                                             return; // Exit the function if division by zero
                                                              }
                                                result = num1 / num2;
                                          } else {
                                               console.log("Error: Invalid operation selected.");
                                             return; // Exit the function if an invalid operation is chosen
                                                         }

                         // Display the result of the operation
                                         console.log(`Result: ${num1} ${operation} ${num2} = ${result}`);
                                                     }

                        // Call the function to start the calculator
                                          simpleCalculator();



4. **Functions**:
   - Create a function named `greetUser` that takes a name as a parameter and returns a greeting message. Display the message in an HTML element.  

---



                     <!DOCTYPE html>
                          <html lang="en">
                                     <head>
                                  <meta charset="UTF-8">
                                 <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                 <title>Greet User</title>
                                         </head>
                                         <body>
                                   <h1>Welcome to the Greeting Application</h1>
    
                                  <!-- Input for the user's name -->
                                <label for="name">Enter your name: </label>
                                <input type="text" id="name" placeholder="Your name">

                               <!-- Button to trigger the greeting function -->
                                <button onclick="displayGreeting()">Greet Me</button>

                                <!-- Element to display the greeting message -->
                               <p id="greetingMessage"></p>

                              <!-- Link to the external JavaScript file -->
                                  <script src="script.js"></script>
                                 </body>
                                      </html>





                                      // Function to greet the user
                                               function greetUser(name) {
                                                  return `Hello, ${name}! Welcome to our website.`;
                                                              }

                                    // Function to capture the input and display the greeting message
                                              function displayGreeting() {
                                   // Get the value entered in the input field
                                              const name = document.getElementById('name').value;

                                  // If name is not empty, call greetUser function
                                              if (name.trim() !== '') {
                                               const message = greetUser(name);
                                        document.getElementById('greetingMessage').textContent = message;  // Display message in HTML
                                       } else {
                                       document.getElementById('greetingMessage').textContent = 'Please enter your name.';  // Error message if name is empty
                                                  }
                                                    }



#### **Part 2: JavaScript Control Structures**

4. **If Statements**:
   - Ask the user for their age using `prompt()`. Use an `if` statement to check if they are eligible to vote (age >= 18). Display a message indicating their eligibility in an HTML element.

                   <!DOCTYPE html>
                     <html lang="en">
                                <head>
                                  <meta charset="UTF-8">
                                   <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                    <title>Voting Eligibility</title>
                                   </head>
                                          <body>
                               <h1>Check Voting Eligibility</h1>
    
                           <!-- Element to display the eligibility message -->
                             <p id="eligibilityMessage"></p>

                          <!-- Link to the external JavaScript file -->
                           <script src="script.js"></script>
                         </body>
                          </html>


                      // Function to check voting eligibility
                                 function checkEligibility() {
                     // Prompt the user for their age
                                 let age = prompt("Please enter your age:");

                    // Convert age to an integer (in case the user enters a non-numeric value)
                                  age = parseInt(age);

                    // Check if the age is valid (a number)
                               if (isNaN(age)) {
                                  document.getElementById('eligibilityMessage').textContent = "Please enter a valid age.";
                               } else if (age >= 18) {
                     // If age is 18 or above, the user is eligible to vote
                              document.getElementById('eligibilityMessage').textContent = "You are eligible to vote!";
                                     } else {
                     // If age is below 18, the user is not eligible to vote
                             document.getElementById('eligibilityMessage').textContent = "You are not eligible to vote yet.";
                                }
                                   }

                     // Call the function to check eligibility when the page loads
                             checkEligibility();





5. **Loops**:
   - Write a loop to display numbers from 1 to 10 on the webpage. Use an ordered list (`<ol>`) to present the numbers.
                         <!DOCTYPE html>
                            <html lang="en">
                               <head>
                                <meta charset="UTF-8">
                          <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                <title>Number List</title>
                               </head>
                             <body>
                            <h1>Numbers from 1 to 10</h1>
    
                             <!-- Ordered list to display the numbers -->
                              <ol id="numberList"></ol>

                           <!-- Link to the external JavaScript file -->
                           <script src="script.js"></script>
                                 </body>
                                     </html>







                                // Function to generate and display numbers from 1 to 10
                                     function displayNumbers() {
                               // Get the ordered list element by its ID
                                     const numberList = document.getElementById('numberList');

                             // Loop through numbers from 1 to 10
                                    for (let i = 1; i <= 10; i++) {
                           // Create a new list item (<li>) for each number
                                   let listItem = document.createElement('li');
        
                         // Set the text content of the list item to the current number
                                 listItem.textContent = i;

                          // Append the list item to the ordered list
                                  numberList.appendChild(listItem);
                                     }
                                           }

                         // Call the function to display the numbers when the page loads
                                    displayNumbers();



---

#### **Part 3: Introduction to the DOM**

6. **Creating HTML Structure**:
   - Add the following HTML elements to your webpage:
     - A heading (`<h1>`) with the text **"JavaScript Assignment"**.  
     - A paragraph (`<p>`) with the text **"Learning JavaScript is fun!"**.  
     - A `<div>` with an `id` of `dynamic-content`.
    
                              <!DOCTYPE html>
                                <html lang="en">
                                       <head>
                                      <meta charset="UTF-8">
                                         <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                        <title>JavaScript Assignment</title>
                                                </head>
                                                  <body>
                                     <h1>JavaScript Assignment</h1>
                                           <p>Learning JavaScript is fun!</p>
                                              <div id="dynamic-content"></div>
                                              </body>
                                              </html>
 

7. **Selecting and Modifying HTML Elements**:
   - Use JavaScript to:
     - Change the text of the `<h1>` element to **"JavaScript in Action!"**.  
     - Add a new `<p>` inside the `dynamic-content` `<div>` with the text **"This content was added dynamically using JavaScript."**.
    

                       <!DOCTYPE html>
                          <html lang="en">
                                  <head>
                                <meta charset="UTF-8">
                                <meta name="viewport" content="width=device-width, initial-scale=1.0">
                                <title>JavaScript Assignment</title>
                                    <script>
                      // JavaScript to change the h1 text and add a new paragraph dynamically
                                  window.onload = function() {
                      // Change the text of the h1 element
                                 document.querySelector('h1').textContent = "JavaScript in Action!";

                     // Create a new paragraph element
                                 var newParagraph = document.createElement('p');
                                 newParagraph.textContent = "This content was added dynamically using JavaScript.";

                    // Append the new paragraph inside the dynamic-content div
                                   document.getElementById('dynamic-content').appendChild(newParagraph);
                                           };
                       </script>
                              </head>
                                 <body>
                               <h1>JavaScript Assignment</h1>
                            <p>Learning JavaScript is fun!</p>
                               <div id="dynamic-content"></div>
                                    </body>
                                   </html>



 

---

