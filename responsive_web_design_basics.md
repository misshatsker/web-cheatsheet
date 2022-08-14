***Set the viewport*** 

![](/media/10.jpg)

- width=device-width - instructs the page to match the screen's width in device-independent pixels.
- initial-scale=1 - instructs browsers to establish a 1:1 relationship between CSS pixels and device-independent pixels regardless of device orientation, and allows the page to take advantage of the full landscape width.
___
***Ensure an accessible viewport***

In addition to setting an initial-scale, you can also set the following attributes on the viewport:

- minimum-scale
- maximum-scale
- user-scalable

When set, these can disable the user's ability to zoom the viewport, potentially causing accessibility issues. Therefore we would not recommend using these attributes.
___
***Size content to the viewport***

- images

An image has fixed dimensions and if it is larger than the viewport will cause a scrollbar. A common way to deal with this problem is to give all images a max-width of 100%
![](/media/11.jpg)

When using max-width: 100% you are overriding the natural dimensions of the image, however you should still use the width and height attributes on your img tag. This is because modern browsers will use this information to reserve space for the image before it loads in, this will help to avoid layout shifts as content loads.

- Flexbox - is ideal when you have a set of items of different sizes and you would like them to fit comfortably in a row or rows, with smaller items taking less space and larger ones getting more space.
![](/media/12.jpg)

In a responsive design, you can use Flexbox to display items as a single row, or wrapped onto multiple rows as the available space decreases.

- CSS Grid Layout - allows for the straightforward creation of flexible grids.
![](/media/13.jpg)

Grid can also be used to create regular grid layouts, with as many items as will fit. 

- Multiple-column layout - which can create responsive numbers of columns with the column-width property.
___
***Use CSS media queries for responsiveness*** - are simple filters that can be applied to CSS styles. They make it easy to change styles based on the types of device rendering the content, or the features of that device, for example width, height, orientation, ability to hover, and whether the device is being used as a touchscreen.

To provide different styles for printing, you need to target a type of output so you could include a stylesheet with print styles as follows:
![](/media/14.jpg)

Alternatively, you could include print styles within your main stylesheet using a media query:
![](/media/16.jpg)

***How to choose breakpoints***

To insert a breakpoint at 600px, create two media queries at the end of your CSS for the component, one to use when the browser is 600px and below, and one for when it is wider than 600px.

![](/media/15.jpg)
___
***FLEX***

***display*** - specifies the display behavior (the type of rendering box) of an element.
- display: flex - Displays an element as a block-level flex container.
- display: inline-flex - Displays an element as an inline-level flex container.

***justify-content*** property aligns the flexible container's items when the items do not use all available space on the main-axis (horizontally).
- flex-start.	Default value. Items are positioned at the beginning of the container	
- flex-end.	Items are positioned at the end of the container	
- center.  Items are positioned in the center of the container	
- space-between. Items will have space between them	
- space-around.	Items will have space before, between, and after them	
- space-evenly.	Items will have equal space around them.

***align-items*** - property specifies the default alignment for items inside the flexible container.

- stretch.	Default. Items are stretched to fit the container	
- center.	Items are positioned at the center of the container	
- flex-start.	Items are positioned at the beginning of the container	
- flex-end.	Items are positioned at the end of the container	
- baseline.	Items are positioned at the baseline of the container.

***align-content*** - property modifies the behavior of the flex-wrap property. It is similar to align-items, but instead of aligning flex items, it aligns flex lines.

- stretch.	Default value. Lines stretch to take up the remaining space	
- center.	Lines are packed toward the center of the flex container	
- flex-start.	Lines are packed toward the start of the flex container	
- flex-end.	Lines are packed toward the end of the flex container	
- space-between.	Lines are evenly distributed in the flex container	
- space-around.	Lines are evenly distributed in the flex container, with half-size spaces on either end	
- space-evenly.	Lines are evenly distributed in the flex container, with equal space around them.

***align-self*** - property specifies the alignment for the selected item inside the flexible container.

- auto.	Default. The element inherits its parent container's align-items property, or "stretch" if it has no parent container	
- stretch.	The element is positioned to fit the container	
- center.	The element is positioned at the center of the container	
- flex-start.	The element is positioned at the beginning of the container	
- flex-end.	The element is positioned at the end of the container	
- baseline.	The element is positioned at the baseline of the container.

***flex-wrap*** - property specifies whether the flexible items should wrap or not.

- nowrap.	Default value. Specifies that the flexible items will not wrap	
- wrap.	Specifies that the flexible items will wrap if necessary	
- wrap-reverse.	Specifies that the flexible items will wrap, if necessary, in reverse order.

***order*** - property specifies the order of a flexible item relative to the rest of the flexible items inside the same container.

- number.	Default value 0. Specifies the order for the flexible item.

***flex-basis*** - property specifies the initial length of a flexible item.
- number. A length unit, or percentage, specifying the initial length of the flexible item(s)	
- auto.	Default value. The length is equal to the length of the flexible item. If the item has no length specified, the length will be according to its content.

***flex-grow*** - property specifies how much the item will grow relative to the rest of the flexible items inside the same container.
-  number -   specifying how much the item will grow relative to the rest of the flexible items. Default value is 0.

***flex-shrink*** - property specifies how the item will shrink relative to the rest of the flexible items inside the same container.
-  number - specifying how much the item will shrink relative to the rest of the flexible items. Default value is 1.

***flex***  -  property sets the flexible length on flexible items.

The flex property is a shorthand property for:

- flex-grow
- flex-shrink
- flex-basis.

***flex-direction*** - property specifies the direction of the flexible items.

- row.	Default value. The flexible items are displayed horizontally, as a row	
-  row-reverse.	Same as row, but in reverse order	
- column.	The flexible items are displayed vertically, as a column	
- column-reverse.	Same as column, but in reverse order.

***flex-flow*** - property is a shorthand property for: ***flex-direction***,
***flex-wrap***.

- flex-direction.	Possible values:
row
row-reverse
column
column-reverse
initial
inherit
Default value is "row".
- flex-wrap. Possible values:
nowrap
wrap
wrap-reverse
initial
inherit
Default value is "nowrap".
___

***GRID***

***display***
- ***display: grid*** - Displays an element as a block-level grid container. Occupies the entire width of the parent.
- ***inline-grid*** - Displays an element as an inline-level grid container. The width of the object is equal to the width of the content.

***grid-template-rows*** - property specifies the number (and the heights) of the rows in a grid layout.
- none.	No size is set. Rows are created if needed	
- auto.	The size of the rows is determined by the size of the container, and on the size of the content of the items in the row	
- max-content.	Sets the size of each row to depend on the largest item in the row	
- min-content.	Sets the size of each row to depend on the smallest item in the row	
- length.	Sets the size of the rows, by using a legal length value.

***grid-template-columns*** - property specifies the number (and the widths) of columns in a grid layout.

- none.	Default value. Columns are created if needed	
- auto.	The size of the columns is determined by the size of the container and on the size of the content of the items in the column	
- max-content.	Sets the size of each column to depend on the largest item in the column	
- min-content.	Sets the size of each column to depend on the smallest item in the column	
- length.	Sets the size of the columns, by using a legal length value.

***1fr*** - unit of flexibility. distributes the column width space evenly, trying to fill the entire grid container.

***grid-template-areas*** - property specifies areas within the grid layout.

Each area is defined by apostrophes. Use a period sign to refer to a grid item with no name.

- none.	Default value. No named grid areas	
- itemnames.	A sequence that specifies how each columns and row should display.

![](/media/17.jpg)

***grid-area*** - property specifies a grid item's size and location in a grid layout, and is a shorthand property for the following properties:

- grid-row-start
- grid-column-start
- grid-row-end
- grid-column-end.

![](/media/18.jpg)

***grid-template*** - property is a shorthand property for the following properties:

- grid-template-rows /
- grid-template-columns
- grid-template-areas.

(e.g.- grid-template: 150px / auto auto auto;)

***grid-auto-rows*** - property sets a size for the rows in a grid container.

This property affects only rows with the size not set.

***grid-auto-columns*** - property sets a size for the columns in a grid container.

This property affects only columns with the size not set.

***grid-auto-flow*** - property controls how auto-placed items get inserted in the grid.

- row.	Default value. Places items by filling each row	
- column. Places items by filling each column	
- dense. Place items to fill any holes in the grid	
- row dense. Places items by filling each row, and fill any holes in the grid	
- column dense.	Places items by filling each column, and fill any holes in the grid.





















