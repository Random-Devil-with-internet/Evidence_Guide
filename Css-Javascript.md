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

## How to use a button with JavaScript
You first need to make a function inside that function you will put the paragraph's id after it you type in '.textContent' and assign a string to it. Next outside the function you put the button's id but this time you type '.onclick' and assign the function above to it.

```html
<p id="Paragraph">Paragraph</p>

<button id="Button">Button</button>

<script>
function Click() {
  Paragraph.textContent = 'Clicked';
};

Button.onclick = Click;
</script>
```
What this code does is that when you press the button the text in the paragraph gets updated with the new text.

![Html button unpressed with JavaScript](https://github.com/Random-Devil-with-internet/Evidence_Guide/blob/main/Button.png)
![Html button pressed with JavaScript](https://github.com/Random-Devil-with-internet/Evidence_Guide/blob/main/Button_2.png)

You can also use diffrent inputs in html like the text box combained with the button to change the text with the input form the text box.
```html
<p id="Paragraph">Paragraph</p>
<input type="text" id="Input" />
<button id="Button">Button</button>

<script>
function Click() {
const input = document.getElementById("Input");
const inputValue = input.value;
Paragraph.textContent = inputValue;
};

Button.onclick = Click;
</script>
```
With the document.getElementById and adding .style with the property you can also change the properties of the element eg. font size and colour.
```html
<p id="Paragraph">Paragraph</p>
<input type="text" id="Input" />
<button id="Button">Button</button>

<script>
function Click() {
const input = document.getElementById("Input");
const inputValue = input.value;
document.getElementById("Paragraph").style.color = inputValue;
};

Button.onclick = Click;
</script>
```
# Reflection


