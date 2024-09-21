# Css & JavaScript

# Css
In week 2 I learned css. Css instead of being a markup language is a stylesheet language that is used together with html to add style and layout to a website.

## Syntax
In html you have elements eg. h1, p, img to add style to a specific element you have to type the element as you would in html but without the arrows outside it. Instead you put curly brackets after the element. Inside the curly brackets you put all the properties of the element. Properties can be color, width, font type, etc. and after each property you put a colon with the value ending with a semicolon.

Example:
```css
p {
  color: rgb(255, 255, 255); /* white */
  font-family: Arial, sans-serif;
  font-size: 14px;
}
```
How you put css in a html file is by either using an external file or putting it into the html file. You can also put the css in Inline but that will not be covered. To link an external css file you need to use a link tag, inside the link tag there are two attributes href, rel. The href attribute is the file path, the rel attribute is to indicate that it is a style sheet. To put the css into the html file you put the css inside two style tags.

Example:

External
```css
<link rel="stylesheet" href="style.css">
```

Internal 
```html
<style>
p {
  color: rgb(255, 255, 255);
  font-family: Arial, sans-serif;
  font-size: 14px;
}
</style>
```

# JavaScript
In week 3 I learned JavaScript which is a proper programming language this time. JavaScript is mostly used on websites to program interactive and behavioural features. This guide will not show you the basic syntax nor the structure of JavaScript since I have already leared python.

## How to ues a button with JavaScript
You first need to make a fuction inside that fuction you will put the button's id after it type in '.textContent' and assgin a string to it. Next outside the fuction
