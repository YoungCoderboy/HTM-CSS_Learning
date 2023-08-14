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
