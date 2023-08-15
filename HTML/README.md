HTML stand for : hyper text markup language
responsible for web structure

HTML Tags:-->
```html


<h1> ->Heading tag(biggest heading)
<h6> ->Heading tag(smallest heading)    
<img> ->image tag
<p> ->paragraph
</br> ->line break
<sub> -> make to the top ex:1st
<sup> -> make to the bottome:log2
<strong> ->make the element inside it bold
<em> -> make the element inside it italyc
<ul> ->unordered list
<li> -> list item
<ol> ->Orderde list
<table> ->this is use to make table it has 3 element <tr>,<td>,<th>;
<tr> ->table row
<td> ->table column
<form> ->form element
<input> ->tag to take input from the user, there many multiple type of input
<label> -> just join input with some name has 1 attribute of 'for' which equeal to input tag id
<button> ->simple button having perticular type
<textarea> -> it is use to take long input from the user
```

index.html will the home page of any website so each project should have index.html

''' HTML 

<h1>This is our first html file</h1>
<p>This is my new paragraph</p>

'''

Structure in HTML
'''html

<!DOCTYPE html>
<!-- This is version of html element -->
<html lang="en">
    <!-- This is html root element  -->
<head>
    <!-- Data about website ie data about data -->
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!-- Content of html page -->
</body>
</html>
'''

html is widespace collasping language because it remove extra space in between two word ex: <h1>this is space </h1> then html will automicall remove extra space and display as simeple "this is space"

lorem provide dummy text it is like the place holder

ctrl + spacebar -:=> provide back the suggession if we miss

what were we have in between the tags are called attributes
ex: ```html 
<img src="" alt="">
``` here src and alt are attributes
image tag:
-Royelty free images: pexels.com , pixabay.com
-we use width, height attribute to change the width and height of the images
-even thought width and height attribute is one of the option to crop the image but still we need to render this full image so it is good practise to crop the images in advance so that it will not slow down your site

Link:
<a> is use to provide line to internal and external website or even to same page
<a href="">content to be display</a>

we also have target attribute which help to open link in new tab
target="\_blank"

provide the id attribute to any resource in same webpage then use '#idProvided in href' then we will get navigate to that id in same page

strong and em are just for proper or good ui it help for screen reader to make sentence strong or em and if you want to make just for visual impact then use CSS

Special Character:
use "&" to access special character
ex: "&copy"

formspree is website for testing the form submission on without backend website

form:
it have 2 attributes
action,method

<form action="" method=""><form>

input:
it has default 2 attribute ie type,name
name provide the datavalue,and type is type of data
we can also provide placeholder so that user can know what to type immediatly
we can also provide initial value using 'value' attribute
type submit help us to create the button which will submit the form after doing type checking
we can also use button tag with type of 'submit'
<input type="text">name
<input type="password">password
<input type="password" placeholder="enter you password here">password
<input type="submit">submit here

when we click submit button then the name and there value add as parameter to link and do given request to given url

input with type radio will create the radio button we can have as many radio button as we can but each one should have same name for given option also we should provide value attribute since when we submit form that value will get pass
also if we dont have same name then we can select multiple option/radio button
add check attribut so that it will checked by default

we should use check boxes for submitting multipe value insted of radio button

use select for drop down list
<select name="languages">

<option value='javascript'>javascript</option>
<option value='java'>java</option>
</select>
