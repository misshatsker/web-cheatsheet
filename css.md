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

***Introduction to the Box Model***

-  ***width and height***  - The width and height of the content area.
- ***min-width*** — this property ensures a minimum width of an element’s box.
- ***max-width***  — this property ensures a maximum width of an element’s box.
- ***min-height*** — this property ensures a minimum height for an element’s box.
- ***max-height*** — this property ensures a maximum height of an element’s box.
- ***padding*** - The amount of space between the content area and the border.
- ***border*** - The thickness and style of the border surrounding the content area and padding.

(Borders can be set with a specific width, style, and color)
- ***border-radius*** - modify the corners of an element’s border box.
- ***margin*** - The amount of space between the border and the outside edge of the element.

(***margin: 0 auto*** - will center the divs in their containing elements. The 0 sets the top and bottom margins to 0 pixels. The auto value instructs the browser to adjust the left and right margins until the element is centered within its containing element.)
- ***overflow*** -  controls what happens to content that spills, or overflows, outside its box.

(***hidden***  —when set to this value, any content that overflows will be hidden from view.

***scroll*** —when set to this value, a scrollbar will be added to the element’s box so that the rest of the content can be viewed by scrolling.

***visible***—when set to this value, the overflow content will be displayed outside of the containing element. Note, this is the default value.
)
- ***Visibility*** - elements can be hidden from view.
(***hidden*** — hides an element.

***visible*** — displays an element.

***collapse*** — collapses an element.)
___

***Change the Box Model***
