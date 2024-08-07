# JavaScript Calculator
<br></br>
![Calculator Screenshot](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/screenshot1..jpg)

<br></br>

[Live Website](https://nigelfinegan5p.github.io/project-2/)

[Live Repository](https://github.com/NigelFinegan5p/project-2)
<br></br>

## Table of Contents
1. [Introduction & Project objectives](#introduction)
2. [Design & Wireframe](#design)
3. [HTML for Structure](#html)
4. [CSS Styling](#css)
5. [JavaScript Functionality](#javascript)
6. [Fonts](#fonts)
7. [Lighthouse Testing](#lighthouse)
8. [HTML, CSS & JS Validation](#validation)
9. [Deployment](#deployment)
10. [Bugs, Errors & Fixes](#bugs)
11. [Bibliography & Sources](#sources)


<br></br>

## Introduction & Project objectives

<a name="introduction"></a>
This is what I intended to build from our project idea, is the following JavaScript calculator. My simple calculator will be able to perform the primary arithmetic operations, such as (addition, subtraction, multiplication and division) additionally and also on numbers containing decimal points. The calculator Functionality building blocks are from JavaScript, DOM model manipulation and (else if) statements allowing basic functions for performing the arithmetic operations. The structure comes from HTML and the style from CSS.

Design and appearance of the calculator is clean and simplistic in line with the project objectives and creating a colourful and visually appealing look. The outline features a bright yellow background, a large display for showing numbers, and large buttons for inputting data and performing calculations. Additionally, I have incorporated simple animations of a color change when hovering over the buttons for an enhanced user experience on the main (AC) and equals button.

<br></br>

## Design & Wireframe
<p></p>
<a name="design"></a>

![Wireframe1](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/wireframe1..jpg)
<br></br>

![Wireframe2](https://github.com/NigelFinegan5p/project-2/blob/main/docs/wireframe/wireframe2..jpg)
<p></p>
<br></br>

## HTML for Structure
<a name="html"></a>
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
<a name="css"></a>

To make our calculator visually appealing, we approached this by applying different CSS styles and effects.

To enhance the visual appeal of our calculator project with CSS. We applied styles to the buttons, display screen, and overall layout to make it user-friendly and appealing.

As the project has a numbers theme we kept the background image in alignment with the theme the website.

With the addition of the font-family: 'zen dots', amaranth, we set the background color to the entire body with styles to the container too. Using the color #f2c40f.

<br></br>
<br></br>

## JavaScript Functionality
<a name="javascript"></a>

We labelled the JavaScript file script.js, in which we wrote the JavaScript code for the calculation of the inputs. We have created declarations and functions for manipulating operations in the calculator.

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
<a name="fonts"></a>

We selected the following fonts for this project.

![font](https://github.com/NigelFinegan5p/project-2/blob/main/docs/screenshots/fonts.jpg)

<p></p>

![font](https://github.com/NigelFinegan5p/project-2/blob/main/docs/screenshots/fonts2.jpg)

<br></br>



## Lighthouse Testing
<a name="lighthouse"></a>

Lighthouse testing was used. Lighthouse the automated website analysis tool that tests your website and assigns it a score across four different categories: Performance. Accessibility. Best Practices & SEO. Results are below: <p></p>

![lighthouse test](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.test.jpg)
<br></br>

![lighthouse access](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.accessibility.jpg)
<br></br>

![lighthouse best practice](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.bestpractice.jpg)
<br></br>

![lighthouse seo](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/lighthouse.seo.jpg)
<br></br>
<br></br>

## HTML, CSS & JS Validation

<a name="validation"></a>

![HTML](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/validation.html.jpg)
<br></br>
<br></br>

![CSS](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/validation.css.jpg)
<br></br>
<br></br>

![JS Hint](https://github.com/NigelFinegan5p/project-2/blob/main/docs/validation/validation.js.jpg)
<br></br>
<br></br>


## Deployment

<a name="deployment"></a>

To deploy my project 2 JS calculator the following steps were taken:

1.  Clicked on  `Settings`  on the navigation menu in the GitHub repository
2.  Selected the  `Pages`  menu on the left hand side bar.
3.  In the first dropdown menu labeled  `Source`  I selected the branch of the name  `main`  from the dropdown.
4.  In the next icon from left to right in the dropdown labeled  `/root`  and selected this.
5.  Next step was to select Save
6.  At the top of the page the live site link is available to open in a new window

<br></br>
<br></br>

## Bugs, Errors & Fixes
<a name="bugs"></a>
Using the W3C CSS validator it shows up one error. 

> Sorry!We found the following errors (1)
Value Error : padding  `-3px`  negative values are not allowed :  -3px

After having run the CSS validator and picked up this error i changed the value in the style.css file and the border moved to close to the edge of the window.
For this reason i left the error in place. 

<br></br>
<br></br>


## Bibliography & Sources
<a name="sources"></a>

Eloquent JavaScript, 4th edition, Marijn Haverbeke <p></p>
https://eloquentjavascript.net/Eloquent_JavaScript.pdf

JavaScript: The Definitive Guide, 7th Edition David Flanagan<p></p>
https://pepa.holla.cz/wp-content/uploads/2016/08/JavaScript-The-Definitive-Guide-6th-Edition.pdf

JavaScript Elightenment, Cody Lindley <p></p>
http://ijevanlib.ysu.am/wp-content/uploads/2017/12/JavaScript_Enlightenment.pdf

<br></br>

***Sources***

How to create a JavaScript Calculator Using HTML, CSS, and JavaScript <p></p>
[https://stakedesigner.com/how-to-create-a-javascript-calculator/](https://stakedesigner.com/how-to-create-a-javascript-calculator/)
<p></p>

CodeTraversal / JavaScript <p></p>
[https://github.com/CodeTraversal/JavaScript-Projects/blob/main/Calculator/style.css](https://github.com/CodeTraversal/JavaScript-Projects/blob/main/Calculator/style.css)
<p></p>

How to make a Calculator using HTML CSS JavaScript <p></p>
[https://www.youtube.com/watch?app=desktop&v=LX8_z1nvqk4](https://www.youtube.com/watch?app=desktop&v=LX8_z1nvqk4)
<p></P>

How to Build a Calculator Using JavaScript: A Step-by-Step Guide <p></p>
[https://plainenglish.io/community/how-to-build-a-calculator-using-javascript](https://plainenglish.io/community/how-to-build-a-calculator-using-javascript)
<p></p>

Calculator by using HTML, CSS, and JavaScript <p></p>
[https://www.javaguides.net/2024/03/javascript-calculator-project.html](https://www.javaguides.net/2024/03/javascript-calculator-project.html)
<p></p>

CSS Grid Layout Module <p></p>
[https://www.w3schools.com/css/css_grid.asp](https://www.w3schools.com/css/css_grid.asp)
<p></p>

How to Build a Simple Calculator Using HTML, CSS, and JavaScript <p></p>
[https://www.makeuseof.com/build-a-simple-calculator-using-html-css-javascript/](https://www.makeuseof.com/build-a-simple-calculator-using-html-css-javascript/)
<p></p>


How To Create a Calculator Using HTML CSS & JavaScript | Simple Calculator in JavaScript <p></p>
[https://medium.com/@sharathchandark/how-to-create-a-calculator-using-html-css-javascript-simple-calculator-in-javascript-f88c264de03a](https://medium.com/@sharathchandark/how-to-create-a-calculator-using-html-css-javascript-simple-calculator-in-javascript-f88c264de03a)
<p></p>

JavaScript Simple Calculator Program (4 Ways With Code) <p></p>
[https://www.wscubetech.com/blog/javascript-calculator/](https://www.wscubetech.com/blog/javascript-calculator/)
<p></p>

How to build a calculator in JavaScript <p></p>
[https://www.educative.io/answers/how-to-build-a-calculator-in-javascript](https://www.educative.io/answers/how-to-build-a-calculator-in-javascript)
<p></p>





