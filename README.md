# react-document
# Setup for React Project

## Install node.js 
```
https://nodejs.org/en
```
## Check if the node is sucessefully install or not using below command
```
node -v
npm -v
```
* Go to visual Sudio code and create a folder xyz.
* open terminal and run the below mentoned command.
```
npm create vite@latest
```
* Mention project name ex - first_project.

## select the framework
* react
* javascript

``` 
cd first_project
npm install
npm run dev
```
## Integrate tailwindcss with react project 
```
npm install -D tailwindcss
npx tailwindcss init
```
* Go to the tailwind.config.js file and the below mentioned to the module.exports .

```
content: ["./src/**/*.]
```

* index.css is main css file of project, add the mentioned below
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```
# React
React is a frontend Javascript library. Is is an open source component-based library that is in charge of developing the application's view layer. Since its initial release in 2013, React has become one of most popular javascript libraries for UI development. It is easier to reason about and debug, and its capacity to effectively alter the user interface in response to data changes.

# Advantage of React
* React is easy to learn.
* The syntax of react is much like HTML which allow developers to create templates with detailed documentation.
* We can migrate one version to another.

## What is create react app 

* It create a new directory with the given project name and generates a basic file structure for a React.js application. the generated file structure includes the following:

* There are 3 folders in the following React boilerplate: node modules, public, and src, Read.md, package.json, gitgnore, and yarn.lock are additional files.

* node_modules : here we get all the necessary node package of our application.
* Public
* index.html : only one html file is there in the whole application.
* manifest.json : It is applied to transform the application into a progressive web app.
* favicon.ico : It is an icon in the tab.
* src
* App.css,index.css : These are different css files.
* index.js : A file which allows to connect all the components with index.html.
* App.js : A file where we usually import most of the presentational components.
* serviceWorker.js : is used to add progressive web app features.
* setupTest.js : to write testing cases.
*package.json : it shows the list of package the application uses.
* .gitignore : react boilerplate comes with git initiated and .gitignore allow files and folders to be ignored when commiting new changes.

## JSX
Jsx stands for javascript XML. It is a syntax extenstion for javascript that allow you to write HTML-like elements in our javascript code . it is used in react a describe the structure and content of a component.

One of the main benefits of JSX is that it makes it easy to create and manipulating the structure of a components.
```
const name =<h1> hello Bachoo</h1>
```
A JSX elements is converted into a regular javascript object during compilation so that it can be used to construct a genuine DOM elements . For instance, the javascript generated from the jsx code above might be as follow :
```
const name = React.createElement("hi", null,"hello bachoo");
```
## Basic difference between jsx and html
* Nested JSX must return a single element that wraps all other levels of nested elements, which we'll refer to as the parent elements.

* all html attributes and event references in JSX become camelCase, this way, onclick event become onclick and onchange - onchange.

## Browser can't react Jsx 
JSX is a combination of html and javascript. so, it is not supported by browser . so atranspiler called babel converts the jsx into pure javascript. Then browser understand the code and execute it. Browser can't read JSX because there is no inherent implementation for the browser engines to react and understand them.

## Why Jsx 
With help of JSX, we can write html code with javascript. React does not employ the createElement() method; Instead JSX elements are used to create HTML elements . As a result, JSX facilitates the writing and addition of html components in react .A transpiler called babel.js will converts Jsx to javascript on the browser.

### Advantages of Jsx 

* Because JSX  syntax is so similar to html syntax, which many developers are already fimilar with it is simpler to write and read.
* It enables you to specify your whole react components using declarative syntax in a single file by using JSX elements as the component's root.
* By using attributes which are indentical html attributes , it make it simples to give data to your code clean and manageable.

### Note 
* JSX must have one parent elements.
### Why?
JSX is converted into plain javascript object. In javascript, you can only return one object from a function. The same applies to JSX - If you want to return multiple Jsx tags, you need to wrap them in a parent tag.

## Ternary operation inside Jsx elements
The ternary operator can be used with JSX components to conditionally render differnt elements or components based on certain conditions. The ternary operator is shorthand version of if/else statement and has the following syntax :
```
Contition?true:false
```
Here is an example of ternary operators within a JSX components:
```
functionMyComponents(props){
    return(
        <div>
        {props.isLoggedIn ? <p>Welcome back!</p> : <p>please log in</P>}
    )
}
```
In this example the components receives a props called isloggedin and uses the ternary operator to determine whether to show a "welcome back message " or please login  message . The condition is the prop is loggedin is true it will render the first element and if it is false it will render the second element .

It worth nothing that the terniary operator is more concise that an if/else statement but it can be less readdable whrn the condition are complex in that case is recommended to use if/else statement.

## what are html attributes 
html attributes are properties that are  used to defiene the characteristics and behaviour of html elements. they are added to opening tag of html element and come in form of name-value pairs, with the name being the attribute and value being whats it set to

For example commonly used attribute include "class", "id", "src", "href", "for" etc and events like "onclick".

```<div class="my-class">Hellow world </div>
```
But in react we use 'classnamw' attribute insted of class.

Lets take another example of onclick event in html
in html we use "onclick in all lower case but in reacr we use camel case like 'onClick " . also in html we have to put the function in quotes and have to invoke it putting parametrs but in react we use curly braces and the fu7nction name without parenthesis.

* In html a "label" is an ewlement that can be used to privide a text description fior a form elemtnts such as text field or a checkbox. The "for"  attribuites of the label elements is used to associated the label.
With specific form elemtnts typically by specifying the ID the form element.
In rect a "label" components can be created using javascript and jsx to create and style a label elements. This components can be reusable and can be used in different parts of application.

### NOTE--
 we already know there are cartain different between html and jsx and one such difference that we have seen in htmlFor . in normall html we have for but we cannot use it in javascript since it is a reserved keywoed in javascript so we use htmlFor in jsx.

 ## Introduceing the new root API 
 A root in react refers to the top-level data structure that renders a tree. In React 18, we will have two root APIs: Legacy root API and New root API

### Legacy root API
The legacy root api is the existing API called with reactDOM.render method. It will create a root running in legacy mode, which is similar to usage in eact version 17. If we are using reactDOM.render() in your react 18 app, we will definitely see the below issue.

AJSX element is converted into regular javascript object during compilatin so that it can be used to construct a genuine DOM element .

The reason in ReactDOM.render is no longer supported in react 18. Earlier, we used to render the component in below way:

```
ReactDOM.render(<NavBar/>, document.getElementById('root'))
```

 The render() method of react-dom package is considered legacy starting react-dom version 18. ** The method is replaced with createRoot() method that is exported from react-dom/client. ** The createRoot() method taked the root elements as parameters and creates a react root.

 ### New Root API
 createRoot() is a new method instoduced in react 18 that allows you to create a separate root for a react tree outside of the main react DOM tree. it take a single argument, which is a reference to an existing DOM element. It returns a new root object that has a render() method for rendring react components into the specified DOM element.

call createRoot to create a React root for displaying content inside browser DOM element.

### old way to do 
```
impprt ReactDOM from 'react-dom';
const rootNode = document.getElementById('root');
ReactDOM.render(<App />; rootNode);
```
### new way to do 
```
import ReactDOM from 'react-dom/client';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
React will create a root for the domNode, and over managing the DOM inside it. After we've created a root, we need to call root.render to display a react component inside of it:
```
root.render(<app />)
```

An app fully build with react will usually only have one createRoot call for its root component. A page that uses "sprinkles" of react for part of page may have as many separate roots as needed.

