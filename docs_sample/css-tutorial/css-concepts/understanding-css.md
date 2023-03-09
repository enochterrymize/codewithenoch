# Understanding CSS : Thinking inside the Box

Imagine that there is an invisible box around every HTML Element.

### Block and Inline Elements

Block level elements look like start on a new line example
```
<h1></h1>
<p></p>
<div></div>

```

Inline elements flow within the text and do not start on a new line
```
<b></b>,<li>,<img><em>

```
### CSS Associates style rules with HTML Elements

CSS works by associating with HTML elements. 

## CSS Rule containts two parts : a selector and a declataion 

```
p{font-family: Arial;}

```

Here p is the selector, Selector indicates which element the rule applies to.

Declaration indicate how the elements reffered to in the selector should be styled.

Declaration are split into two parts( a property and a value ) and are seperated by colon.

CSS declaration sit inside curly brackets and each is made up of two parts: a property and a value seperated by a colon; you can specify several properties in one declartion, each seperated by semicolon.

```
h1,h2,h3{
    font-family:Arial;
    color: yellow;
}
```
Property indidicate the aspects of the elements you want to change.For Example font,color, width, height, and border.

Value specify the settings you want to use for the chosen properties. 

## Using External CSS

## <link>

The link element can be used in an HTML document to tell the browser where to find the CSS file used to style the page. It is an empty element meaining it does not need a closing tag, and it lives inside the <head> element. it should use three attributes.

```
<link href="" type="" rel="" />
```
## href

This specifies the path to the CSS File(Which is often placed in a folder called css or styles)

## type 

This attribute specifies the type of document being linked to. The value should be text/

## rel

This specifies the relationship between the HTML Page and the file it is linked to. The value should be stylesheet when linking to a CSS File.
