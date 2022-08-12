***link href="style.css" rel="stylesheet"***
___
***Selector*** - The beginning of the ruleset used to target the element that will be styled.

***Declaration Block*** — The code in-between (and including) the curly braces ({ }) that contains the CSS declaration(s).

***Declaration*** — The group name for a property and value pair that applies a style to the selected element.

***Property*** — The first part of the declaration that signifies what visual characteristic of the element is to be modified.

***Value*** — The second part of the declaration that signifies the value of the property.

***href*** — like the anchor element, the value of this attribute must be the address, or path, to the CSS file.

***rel***  — this attribute describes the relationship between the HTML file and the CSS file. Because you are linking to a stylesheet, the value should be set to stylesheet.
___
- "*" - The universal selector. Means "all elements".

- ***.nameclass*** - To select an HTML element by ***CLASS***.

- ***#nameid*** - To select an HTML element by ***ID***.

-  ***nameselector[nametribute * = 'lastname']*** 

***Classes can be reusable, while IDs can only be used once.***

***IDs are more specific than classes, and classes are more specific than type. That means IDs will override any styles from a class, and classes will override any styles from a type selector.***
___
***Pseudo-class*** - user interaction, site navigation, and position in the document. (:focus, :visited, :disabled, :hover, :active)

- ***nameselector:pseudoclass*** 
___
***Chaining*** - combining multiple selectors.

-  ***nameselector.nameclass***
___
***Descendant Combinator*** -  supports selecting elements that are nested within other HTML elements, also known as descendants.

- ***.nameclass nameselector***

- ***nameselector nameselector***
___
***Multiple Selectors*** -  In order to make CSS more concise, it’s possible to add CSS styles to multiple CSS selectors all at once. This prevents writing repetitive code.

- ***name, name***
___
***Visual Rules***

- ***font-family*** - To change the typeface of text on your web page.

(When the name of a typeface consists of more than one word, it’s a best practice to enclose the typeface’s name in quotes)
- ***font-size***  - To change the size of text on your web page.
-  ***font-weight*** - controls how bold or thin text appears.
- ***text-align*** - property places text in the left, right, or center of its parent container. 

(***left*** — aligns text to the left side of its parent element, which in this case is the browser.
***center*** — centers text inside of its parent element.
***right*** — aligns text to the right side of its parent element.
***justify***— spaces out text in order to align with the right and left side of the parent element.)
- ***color*** - defines the color of the text.
-  ***background-color***  - this property styles an element’s background color.
-  ***opacity*** - is the measure of how transparent an element is.
- ***background-image***  - to make the background of an element an image.

(background-image: url(''))
- ***!important*** - will override any style, however it should almost never be used, as it is extremely difficult to override.
___

