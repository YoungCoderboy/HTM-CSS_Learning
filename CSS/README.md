Responsible for styling the web
selector{property:value}
There are three type of CSS
-Inline CSS
-External CSS
-Internal CSS

Inline CSS:
-adding style attribute to element
-hard to read
-syntex: style="color:red;"

Internal CSS:
-Within the head element we add style tag and define CSS there

<style>
    h1{

        color:red;
        font-size:50px;
    }

</style>

internal CSS is great but what if we want another page then we need to define css again hence we use external CSS

External CSS:
-It can be add using link tag

<link rel="stylesheet" href="./styles.css"/>

Power Struggle: Inline CSS > Internal CSS > External CSS
above order will also get affected by order in which we apply
ex:
one:

<style>
    h1{

        color:red;
        font-size:50px;
    }

</style>
<link rel="stylesheet" href="./styles.css"/>
two:
<link rel="stylesheet" href="./styles.css"/>
<style>
    h1{
        //this will get applied
        color:red;
        font-size:50px;
    }

</style>

selector{
color:green;
}

<!-- CSS Selector -->

There are many type of selector:
-element selector
-class selector
-id selector
-{}-called decleration block
-within the decleration we have property and value

Element Selector:
h1{
color:red;
font-size:20px;
}

Group Selector:
h1,h2,p{
color:green;
}

ID Selector:
-use # for target
#title{
color:blue;
background:red;
}

Class Selector:
-use . for target
.redElement{
color:red;
background:black;
}
we can add multiple class to same element or same class to multiple element

Div and span are used to grouping element
Div: use to group multiple element
Span: used to Group inline content

Inheritance:
Children inherit styles from the parent, unless have their own styles

body{
color:red;
}
all other child will inherite color red from body unless they have there own styles
if you add multiple rule of css then last rule will govern the defined property

ID > Class > Element specificity > Universal Specificity

Unversal Specifier:
-it is use to remove default browser style
\*{
color:green;
}

Combine the Selector:
.container p{

<!-- only those paragraph are selected those are inside the container -->

color:green;
}

Color In CSS:
-color: property contorl the color of element
-background_color: property contorl the background color of element
-you can also use background element to set the color of background but this element is not limited to backgroung color you can also set the background image of element
-140+ inbuild color
-rgba() allows us to contorl the opacity a==[0,1];
-HexValue represent RRGGBB

Units:
-absolute,relative
-pixels
-em,rem
-vw,vh
-font-size,height,width

Pixels:
-oversimplified form of unit
-absolute value, one dot on the screen;
-font-size:size of font
-width:width of element
-height:height of element

Percent Unit:
-relative unit/value. Depends on parents
-while using relative unit its parents units should be absolute

em: Relative units,depends on parent
1em-default is 16px set by browser
2em-base value(16px)*2=32;
2em-base value(10px)*2=20;

HTML

<div>
    <h3 class="relavtive">Some text</h3>
</div>

CSS

div{
font-size:10px; --base value,parent value
}
.relative{
font-size:2em; 2\*10:20px
}

rem: relative, depends on root(html tag is root of element)
1rem: base_value(16px)\*1:16px

vh:-height-percent of screen
vw:-width-percent of screen

way to remove default browser style
\*{
margin:0;
padding:0;
box-sizing:border-box;
}

//way to change text size according to screen size
.check{
// heading class
font-size: 5vw;
}

.container{
// div class actually there is no need for div class
width:50vw;
height: calc(100vh - 50px);
background: red;

}

calc Function:
-perform math operation
-mix and matching values
.navbar{

    background: blue;
    height: 100px;
    color: white;
    font-size: 3rem ;

}
.banner{
background: red;
height: calc(100vh - 100px);

}
always be careful with calc since you should give space between two value and '-' operator

height: auto,min-height,max-height,overflow
-height:auto; this will change the height according to content inside element by default height is auto
-ex: height of div tag depends on content inside the div
-if the height is not enough to store the content inside the div then it will overflow to avoid that we can use overflow attribute
-ex:overflow:hidden; overflow:scroll;
-if we specify the min-height then the content will atleast min-height then it can increase in height
