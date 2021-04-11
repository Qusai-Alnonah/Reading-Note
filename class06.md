# Sumary of reading
at what we read in java WHAT IS AN OBJECT Objects group together a set of variables and functions to create a model
of a something you would recognize from the real world. In an object,
variables and functions take on new names. 
we can criat an object and accses yo it  and we can use it later also we can crate lot of object
in the other waye The Document Object Model (DOM) specifies
how browsers should create a model of an HTML
page and how JavaScript can access and update the
contents of a web page while it is in the browser window. 
WORKING WITH THE DOM TREE and how to diel whith SELECTING AN ELEMENT
FROM A NODELIST use a looping thro a nodelist by using  play 
and we can use XSS: VALIDATION & TEMPLATES Make sure that your users can only input characters they need to use
and limit where this content will be shown on the page.
for exsample
II ADDING ITEMS TO START AND ENO OF LIST
var list = document .get El ementsByTagName( ' ul ')[OJ; II Get the <u l> el ement
II ADD NEW ITEM TO END OF LIST
var newitemLast = document . createElement('li '); II Create element
var newTextLast = document .createTextNode{'cream'); II Create text node
newitemLast.appendChild(newTextLast);
list.appendChild(newitemLast);
II Add text node to element
II Add element end of list
II ADD NEW ITEM START OF LIST
var newitemFirst = document . createElement('li ') ;
var newTextFirst = document.createTextNode('kale');
newitemFirst.appendChild(newTextFirst);
list . insertBefore(newitemFirst, list . firstChild);
II Create element
II Create text node
II Add text node to element
II Add element to list

* The browser represents the page using a DOM tree.
DOM trees have four types of nodes: document nodes,
element nodes, attribute nodes, and text nodes.
You can select element nodes by their id or cl ass
attributes, by tag name, or using CSS selector syntax.
Whenever a DOM query can return more than one
node, it will always return a Nadel i st.
From an element node, you can access and update its
content using properties such as textContent and
i nnerHTML or using DOM manipulation techniques.
An element node can contain multiple text nodes and
child elements that are siblings of each other.
In older browsers, implementation of the DOM is
inconsistent (and is a popular reason for using jQuery).
Browsers offer tools for viewing the DOM tree .