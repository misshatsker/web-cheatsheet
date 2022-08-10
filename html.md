***h1 to h6*** - Headings and sub-headings are used to provide titles for sections of content.
___
***p, span and div*** - tags specify text or blocks.
___
***em*** -  is used to define emphasized text.
___
***strong*** - is used to define text with strong importance. 
___
***br*** - Line breaks.
___
***ol*** - Ordered lists.

***ul*** - unordered lists.
___
***img*** - Images.

***video*** - video.
___
***a*** - can add links to a web page. 

***a href="" target="_blank"*** - web page open in a new browser window.

***a href="./index.html"*** - (index.html- folder) open a specific folder.

***a href="#introduction"*** - when we have ***div id="introduction"***. 
___
***TABLE***

***table*** - will contain all of the tabular data we plan on displaying.

***thead*** - defines a set of rows defining the head of the columns of the table.

***tbody*** - used to group the body content in an HTML table.

***tr*** - to add rows.

***th*** - add titles to rows and columns.
- ***th scope="col"***  - this value makes it clear that the heading is for a column.
- ***th scope="row"*** - this value makes it clear that the heading is for a row.

***td*** - add data.
- ***td colspan=""*** - defines the number of columns a table cell should span.
- ***td rowspan="2*** - specifies the number of rows a cell should span.

***tfoot*** - defines a set of rows summarizing the columns of the table.
___
***FORM***

***form*** - collecting information to send somewhere else.

-  ***form action=""*** - determines where the information is sent.
- ***form method=""*** - is assigned a HTTP verb that is included in the HTTP request.

***input*** - determines how it renders on the web page and what kind of data it can accept.
- ***input type="text" name="" value="" id=""***
- ***input type="password" name="" value="" id=""***
- ***input type="number" name="" value="" id=""***
- ***input type="range" name="" value="" id=""*** - defines a control for entering a number whose exact value is not important (like a slider control). Default range is 0 to 100.
- ***input type="checkbox" name="" value="" id=""*** - The checkbox is shown as a square box that is ticked (checked) when activated. Checkboxes are used to let a user select one or more options of a limited number of choices.
- ***input type="radio" name="" value="" id=""*** - Checkboxes work well if we want to present users with multiple options and let them choose one or more of the options.
- ***input type="submit" value=""*** - users click on it when they are finished with filling out information in the form and they’re ready to send it off. 

***label for="(write this id in input)"*** - is used to define a caption for an element in an HTML form. 

***select id="" name=""*** - to create the dropdown list.
- ***option  value=""*** - To populate the dropdown list.

***datalist*** - is used with an ***input type="text"*** element. The ***input*** creates a text field that users can type into and filter options from the ***datalist***. (datalist id="")
(input type="text" list="" id="" name="")
- ***datalist id=""*** then
***option value=""***

***textarea id="" name="" rows="" cols="*** - represents a multi-line plain-text editing control, useful when you want to allow users to enter a sizeable amount of free-form text, for example a comment on a review or feedback form.




