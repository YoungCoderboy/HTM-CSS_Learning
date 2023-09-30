# CSS
Responsible for styling the web
selector{property:value}
There are three type of CSS
- Inline CSS
- External CSS
- Internal CSS

# Inline CSS:
- adding style attribute to element
- hard to read
- syntex: style="color:red;"

# Internal CSS:
- Within the head element we add style tag and define CSS there

```html
<style>
  h1 {
    color: red;
    font-size: 50px;
  }
</style>
```

- internal CSS is great but what if we want another page then we need to define css again hence we use external CSS

# External CSS:
- It can be add using link tag

```html
  <link rel="stylesheet" href="./styles.css" />
```

- Power Struggle: Inline CSS > Internal CSS > External CSS
- above order will also get affected by order in which we apply
- ex:

```html
<!-- first -->
<style>
  h1 {
    color: red;
    font-size: 50px;
  }
</style> 
<link rel="stylesheet" href="./styles.css" />
two:
<link rel="stylesheet" href="./styles.css" />
<style>
  h1 {
    /* //this will get applied */
    color: red;
    font-size: 50px;
  }
</style>

selector{
  color:green;
}

```
<!-- CSS Selector -->

- There are many type of selector:
-- element selector
-- class selector
-- id selector
-- {}-called decleration block
-- Within the decleration we have property and value

## Element Selector:

```css
h1 {
  color: red;
  font-size: 20px;
}
```

# Group Selector:

```css
h1,
h2,
p {
  color: green;
}
```

# ID Selector:
- use # for target

```css
#title {
  color: blue;
  background: red;
}
```

# Class Selector:
- use . for target

```css
.redElement {
  color: red;
  background: black;
}
```

- we can add multiple class to same element or same class to multiple element

- Div and span are used to grouping element
- Div: use to group multiple element
- Span: used to Group inline content

- Inheritance: Children inherit styles from the parent, unless have their own styles

```css
body {
  color: red;
}
```

- all other child will inherite color red from body unless they have there own styles
- if you add multiple rule of css then last rule will govern the defined property

ID > Class > Element specificity > Universal Specificity

# Unversal Specifier:
- it is use to remove default browser style

```css
* {
  color: green;
}
```

# Combine the Selector:

```html
.container p{

<!-- only those paragraph are selected those are inside the container -->

color:green; }
```

# Color In CSS:
- color: property contorl the color of element
- background_color: property contorl the background color of element
- you can also use background element to set the color of background but this element is not limited to backgroung color you can also set the background image of element
- 140+ inbuild color
- rgba() allows us to contorl the opacity a==[0,1];
- HexValue represent RRGGBB

# Units:
- absolute,relative
- pixels
- em,rem
- vw,vh
- font-size,height,width

# Pixels:
- oversimplified form of unit
- absolute value, one dot on the screen;
- font-size:size of font
- width:width of element
- height:height of element

# Percent Unit:
- relative unit/value. Depends on parents
- while using relative unit its parents units should be absolute

- em: Relative units,depends on parent
- 1em-default is 16px set by browser
- 2em-base value(16px)*2=32;
- 2em-base value(10px)*2=20;

# HTML

```html
<div>
  <h3 class="relavtive">Some text</h3>
</div>
```

# CSS

```css
div{ font-size:10px; --base value,parent value } .relative{ font-size:2em;
2\*10:20px }
```

- rem: relative, depends on root(html tag is root of element)
- 1rem: base_value(16px)\*1:16px

- vh:-height-percent of screen
- vw:-width-percent of screen

* way to remove default browser style

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
/* //way to change text size according to screen size */
}
```


```css
.check{
   /* // heading class  */
   font-size: 5vw; }
.container{ 
  /* // div class actually
  there is no need for div class  */
  width:50vw; 
  height: calc(100vh - 50px);
  background: red;
}
```

* calc Function:
- perform math operation
- mix and matching values

```css
.navbar {
  background: blue;
  height: 100px;
  color: white;
  font-size: 3rem;
}
.banner {
  background: red;
  height: calc(100vh - 100px);
}
```

- always be careful with calc since you should give space between two value and '-' operator

- height: auto,min-height,max-height,overflow
- height:auto; this will change the height according to content inside element by default height is auto
- ex: height of div tag depends on content inside the div
- if the height is not enough to store the content inside the div then it will overflow to avoid that we can use overflow attribute
- ex:overflow:hidden; overflow:scroll;
- if we specify the min-height then the content will atleast min-height then it can increase in height

# Typography Introduction:

- font-size - size of the fonts
- font-family - describe the fonts of the element
- we create font-stack of generic family: becaue if some of the font we mension are not installed or cached by the browser then it will break the code thus we provide stack of fonts so that if top one is not there then next -next will come in use by browser
- Google font link should be place before styles.css file
- system fonts are the fonts that's is already installed on ther user computer/devices of the user
- ----fast load time
- ----less headaches
- ----projects look differect
- some important font
- ----trade winds
- font-weigth: how thick or thin character in text should be
- font-styles: sets the fonts style for a text
- text-align,text-indent
- text-align make the whole text to move toward speficied location on window may be center,right;
- text-indent: help to add indentation to element
- line-height : it is the distince between the lines
- letter-spacing
- word-spacing
- text-transform: help to change text case
- text-decoration

```css
body {
  font-family: "Silkscreen", cursive;
  font-size: 20px;
  line-height: 1.5; /*30px*/
}
h1 {
  font-family: "Cinzel", serif;
  font-size: 50px;
  letter-spacing: 0.5rem;
}
p {
  word-spacing: 10px;
}
a {
  font-size: 3rem;
  text-decoration: none; /*remove the underline from the word*/
}
```

```html
<a href="google.com">google.com</a>
<h1>hey dude i'm main heading</h1>
<p>
  Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid, atque
  accusantium, fugiat quae deserunt repellendus tempore, nobis a non soluta
  molestiae vero libero deleniti mollitia. Excepturi quia harum consequatur
  repellendus.
</p>
```

# CSS-Box_Models:

- each and every element in css is represented as the box
- magin: distance between element and other element or screen
- border: line between margin and padding
- padding:space is created between content and element  
- content
- 
- we have some margin added by browser

```css
h1 {
  border-style: solid;
  border-width: 10px;
  border-color: black;
  /* shortcut */
  /* border: width style color; */
  /* border-radius:- controls the edges of the border */
  /* we can also use -ve margin */
}
/* text-decoration is use to remove or add underline */
```

```css
.one {
  outline-width: 0.2rem;
  outline-color: black;
  outline-style: solid;
  outline-offset: 10px;
  /* above one can be -ve and offset create space between border and margine*/
}
/* simple trick */

* {
  border: 2px solid red;
}
above show all element present and there behavior .div {
  margin: 3rem auto;
  /* make this center aligne */
}
```

# Display Property

- Element have it setby default
- Block: Always Start with new Line and Span full width
- Inline: Doesnot start with new line and span only content

```html
<!-- below is block element -->
<div class="block">i am block element</div>
<h1 class="block">i am block element</h1>
<p class="block">i am block element</p>
```

```html
<span class="inline">i am inline Element</span>
<a class="inline">i am inline Element</a>
<img class="inline" />
```

```css
.block {
  display: inline;
}
.inline {
  display: block;
}
```

# Horizontal Centering
- block element get center by:
- -margin: 0 auto ;
- inline element get center by changing parent element:
- -text-align:center;

- Block: browser respects width/height, top/bottom margin
- Inline:browser does not respect width/height, to/bottom margin

```css
ul li{
  /* this will remove dot before list  */
  list-style-type:none;
  display:block;
}
/* make display block so that it can respect padding or margin */
```

* box-sizing
- default is content-box;
- we should change to border-box
- box-sizing:border-box; then padding will apply within the element it doest not change its fixed size

- inline-block;:doesnot start with new line but browser respect the margin, width, height
- display:none :- remove from the flow, hide the element collapse the space
- opacity:0 visibility:hidden -hides element preserve the space

# image

```css
div{
  /* sets the  background image  */
  background: url('./image/big.jpeg');
}
```
- if image is small then the background image will repete beacuse of repete property

```css
background-repeat:repeat;
/* ----> default action */
```
- other values are:
- - no-repeat
- - repeat-x
- - space: add space along with image
- - round: if there is space for two image then i will add another image

```css
background-size: 
/* this propety is use to fix the size of image  */
```
- possbile values are:
- cover: try to cover entire div
- contain: try to show entire content

```css
background-position:
```
- possible values are:
- center: make the image center of content
- left right top bottom are other value
- we can also use percentage 
```css
background-position:0 0; 
/* we give x and y */
background-attachment: fixed;
/* this will fixed the image and move text above it  */
/* scroll is default behavior */
```

```css
background:linear-gradient(to bottom,red x%,green y%);
/* here x and y are optional value also these are numerical value more the x more will the solid color is  */
/* instead of to bottom we can also use degreee value for examle 315deg  */
```

```css
div{
  /* this will add ovelay on the top of image */
  /* this will help to see image more clear */
  background: linear-gradient(rgba(0,0,0,0.5),rgba(0,0,0,0.5)),url(path)
}
```


# float postion media query

```css
.banner{
  float: right;
}
p{
  clear:right;
}

/* make the image float */
```

- to make the column layout set the width parent with 100/no of column then make it float
- position:static -default, always positioned according to normal flow 
- position:relative -position relative to its normal  flow use top right left property to change the position
- position:absolute - relative to parent with position position:relative 
- position:fixed - relative to viewpoint stay as we are scrolling 
- position:sticky -toggles between the relative and fixed once the position is met in the viewpoint then it sticks
- body is always positioned relative

# media query
- responsive design
- style element on different screen size 
- min-width ---starting from 
- max-width ---up to 
- mobile first 

 ```css
 @media screen and (min-width){
    body{
      background:green;
    }
    .banner{
      color: red;
    }
 }
 ```

z-index
 - z-axis
 - 0 by default
 - does not work on position static

 ::before ::after psedo elements creates element  and insert before and after CONTENT
 content:'' is required 
 img: does not work

 ```css
 p::before{
  content:'hello there';

 }
 /* if we dont have any content then we can use width and height so that we can see it else it will not shown */
 ```

- div > h1 ==> this will choose only child not all decendent 
- ::first-line ::first-letter are two pseudo selector

* :hover pseudo class it represent perticular state of element
```css
div:hover{
  color: red;
}
```

* Other Pseudo Class:
- :link - unvisited links with href
- :visited -visited links 
- :active - as the user clicks 
* :root -> selects root element of document, higher specificity html element
- general style
- css variable

# Transform, Transition and animation 
- transform: translate(), rotate(), scale(), skew()
- transition: change over time
- animation: change over time with more control

* transform 
```css
div{
  transform: translate(x,y);
  /* if x is in percent then the in pixel it will x perxent of width or heigh */
  transform: scale(0.5 ,0); 
  /* same as scaleX(0.5 ) */
  transform: rotate(20deg);
  transform: skew(10deg, 20deg);
}
```

* transition 
```css
div{
  transition-propety: background, border-radius ;
  transition-duration: 1000ms, 2s;
  transition-delay: 2s;
}

div:hover{
  background: wheat;
  border-radius: 50%;

}
/* shorthand
  transition: property time transition-timing delay , same , same for multiple propety;
*/


```

* transition timing: how the transition take place
- transition-timing-function
- transition: all 3s here 2s;
- ease = default
- ease = slow start, fast , slow end 
- linear = same speed start to end 
- ease-in slow start
- ease-out slow end
- ease-in-out : slow start ,fast ,slow end 
```css

div{
  transition-timing-function: ease;
}

```

* Animation;
- this provide multiple state

```css
.animation[

  animation-name: _name;
  animation-duration: 10s;
  animation-iteration-count:2;
  animation-fill-mode: forward; 
  /* using above our state doesnt change to original back */
]
@keyframe _name{
  0%{
    /* properties */
  }
  1%{

  }
  10%{

  }
  100%{

  }
}

```