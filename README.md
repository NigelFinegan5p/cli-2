# JavaScript Calculator
<br></br>
![Calculator Screenshot](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/screenshot1..jpg)

<br></br>

## Introduction & Project objectives

This is what I intended to build from our project inception idea is the following JavaScript calculator. My simple calculator will be able to perform the primary arithmetic operations, such as (addition, subtraction, multiplication and division) additionally and also on numbers containing decimal points. The calculator Functionality building blocks are from JavaScript, DOM model manipulation and (else if) statements allowing basic functions for performing the arithmetic operations. The structure comes from HTML and the style from CSS.

Design and appearance of the calculator is clean and simplistic in line with the project objectives and creating a colourful and visually appealing look. The user outline features a bright yellow background, a large display for showing numbers, and large buttons for inputting data and performing calculation. Additionally, I have incorporated simple animations of a color change when hovering over the buttons for an enhanced user experience on the main (AC) and equals button.

<br></br>

## Design & Wireframe
<p></p>

![Wireframe1](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/wireframe1..jpg)
<br></br>

![Wireframe2](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/wireframe2..jpg)
<p></p>
<br></br>

## HTML for Structure
HTML for Structure, CSS for style and Javascript for functionality

We started our project with HTML for structure. 
We created a basic  layout for our JavaScript Calculator in the Index.html file.

In the HTML structure, we have created a container for the JavaScript Calculator buttons for numbers, operators, and the clear and equal sign.

The HTML file starts with boilerplate html `<!DOCTYPE html>` declaration, followed by the `<html>` element tag.

In the `<head>` section, we created meta tags for the character set and viewport settings, along with a title for the page <title>Calculator-Javascript</title>

A link to an external CSS file is included and written into the link by href="assets/css/style.css"

The `<body>` element, contains a `<div>` with the class “calculator” that contains all the calculator components, in total 20 input functions ( buttons ).

Inside the calculator `<div>`, there’s the text input “display”. This is where the output of the calculation result will display.

The rest of the calculator buttons are encased inside a number of other `<div>.`

<br></br>
<br></br>

## CSS Styling

To make our calculator visually appealing, we approached this by applying different CSS styles and effects.

To enhance the visual appeal of our calculator project with CSS. We applied styles to the buttons, display screen, and overall layout to make it user-friendly and appealing.

As the project has numbers theme we kept the background image in alignment with the theme the website.

With the addition of and the font family font-family: 'zen dots', amaranth. We set the background color to the entire body with styles to the container too. Using the color #f2c40f.

<br></br>
<br></br>

## JavaScript Functionality

We labelled the JavaScript file script.js, in which will write the JavaScript code for the calculation of the inputs. We have created declarations and functions for manipulating operations in the calculator.

We approached this using the Document Object Model (DOM) to manipulate elements within the HTML file structure index.html.

Using a document object, the document object represents the owner of all other objects

Using the below declaration we will manage to show input/output for the operations that the end user performs on the calculator. In addition we added another declaration with document.querySelectorAll.

    let input = document.getElementById('inputBox');
    let buttons = document.querySelectorAll('button');
    
This will help to get all the elements based on the value/parameter. According to MDN web docs it is representing a list of the document's elements, that match the specified group of selectors, in this case the pre-selected button and there numerical value as inputs and therefore returning a static not live node list.

If and when we use the value / parameter / return value --- approach with an element name called i.e. (div), it will get all the elements containing div in the current document and will give an attribute value with the help of dot-like (.value) string evaluation with the class value

Each of the received elements from the querySelectorAll will then add the event called “click” , subsequently it will add events, only a number in this case into the innerText and into the calculator display.

    let string = "";
    let arr = Array.from(buttons);
    arr.forEach(button => {
        button.addEventListener('click', (e) => {
        if (e.target.innerHTML === '=') {
           string = eval(string);
           input.value = string;
           }

For example, if the person using the calculator clicks number 1 on the button display, we have added a click event which is received on the inner Text of the display. It will then concatenate the values and produce the answer on the calculator display.

From another perspective and in other words when the user clicks on the button, the button value will display on the input field. When the equal button (=, +, -, or /) is clicked, the solve () function is called and evaluates the expression, and displays the result on the input text field.

The concatenated string is evaluated and a result is displayed.

This very simplistic JavaScript calculator will perform operations like addition, subtraction, multiplication, and division.

Using the querySelectorAll it will in one event perform all four operations and display a result.

<br></br>

***Control Flow & Else If***

In working through the JavaScript course modules and understanding conditional statements and there practical uses I wanted to get a better understanding of control flow, decision making structures and and how to structure them for practical solutions and to work through this project to grasp their usage effectively.

In MDN web docs they articulate Control flow as the order in which the computer executes statements in a script. Code is run in order from the first line in the file to the last line, unless the computer runs across the (extremely frequently) structures & sub structures that change the control flow, such as conditionals and loops.
In essence the control flow is fluid; the only times it is disrupted are when the statements change flow and test for validity. 
<p></p>
[MDN Web Docs Control Flow](https://developer.mozilla.org/en-US/docs/Glossary/Control_flow)<p></P>
[CI - Control Flow in Javascript](https://codeinstitute.net/global/blog/control-flow-in-javascript/)
<br></br>
<br></br>

## Fonts

![font](https://github.com/NigelFinegan5p/project-2/blob/main/docs/screenshots/fonts.jpg)

<p></p>

![font](https://github.com/NigelFinegan5p/project-2/blob/main/docs/screenshots/fonts2.jpg)

<br></br>
<br></br>

## Lighthouse Testing
![lighthouse test](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.test.jpg)
<br></br>

![lighthouse access](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.accessibility.jpg)
<br></br>

![lighthouse best practice](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.bestpractice.jpg)
<br></br>

![lighthouse seo](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.seo.jpg)
<br></br>