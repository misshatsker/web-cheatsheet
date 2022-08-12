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

