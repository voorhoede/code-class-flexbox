#Code Class Flexbox
## What is flexbox?

Relative new layout mode in CSS

**The block layout**  
designed for laying out documents. The block layout contains document-centric features, like the ability to float elements or to lay them out over multiple columns.  

**The inline layout**  
designed for laying out text.  

**The table layout**  
designed for laying out tables.

**The positioned layout**  
designed for positioning elements without much interaction with other elements.

**The flexible box layout**    
designed for laying out complex pages that can be resized smoothly. 
The grid layout designed for laying out elements relative to a fixed grid.

## Why Flexbox?

Flexbox provides tools to allow rapid creation of complex, flexible layouts, and features that historically proved difficult with CSS.

Floats and positioning are limited:

- Vertically centering a block of content inside its parent.
- Making all the children of a container take up an equal amount of the available height
- Making all columns in a multiple column layout adopt the same height


## How to flexbox

The old 2009 spec  — `display:box`  
Is no longer relevant

The 2011 "tweener" spec — `display:flexbox`  
Was a draft spec, only implemented in IE10. 

The final 2012 spec — `display:flex`

### Start
A Flexbox layout consists of a **flex container** that holds **flex items**.

`display: flex`  like a block element  
`display: inline-flex` like an inline-block element

Children are automatically **flex items**

### Flex direction
 The flex container can be laid out horizontally or vertically. This is referred to as the **main axis**

`flex-direction: row`   
Default horizontal layout. Flex-items (Children) height is 100% of container

`flex-direction: column`  
Vertical layout. Flex-items (Children) width is 100% container

**cross axis**  
Is the axis cross of main axis.     
So vertical with `flex-direction: row` and horizontal with `flex-direction: column`

Oposite direction:  
`flex-direction: row-reverse`  
`flex-direction: column-reverse`


> question: what happes with the cross axis when you add `row-reverse`

### Element wrapping
By default, flex items will all try to fit onto one line and stretches **cross-axis**

`flex-wrap: nowrap` Default

`flex-wrap: wrap`  
Uses actual width/height set on flex-item and breaks on multiple lines. Also stretches on **cross-axis** 
<!-- exercise 1 -->

### Ordering
Set on flex children  
Default: `order: 0`  
Works kinda like z-index

### Justify-content
How are the flex-items aligned on the main axis?
Set on flex container

`justify-content: flex-start` Default  
`justify-content: flex-end`  
`justify-content: center`  
`justify-content: space-between`  
`justify-content: space-around`  

### Align-items
How are the flex-items aligned on the cross axis on the *current-line*  
Set on flex container  

`align-items: stretch` Default  
`align-items: center`   
`align-items: flex-start`  
`align-items: flex-end`  
`align-items: baseline`  

<!-- exercise 2 -->

### Align-content
What happes with the extra space on the cross axis?
Set on flex container.
Works only when items are on *multiple lines*. 
For example:  
`flex-wrap: wrap` and a width set on the flex-items

`align-content: stretch;` Default  
`align-content: flex-start;`  
`align-content: flex-end;`  
`align-content: flex-center;`  
`align-content: space-between;`  
`align-content: space-around;`

### Align-self
Overwrite of the `align-items` property set on a flex item  

`align-self: auto;` Default   
`align-self: stretch;`  
`align-self: center;`   
`align-self: flex-start;`  
`align-self: flex-end;`  
`align-self: baseline;` 


### Flex property
Property set on flex items (children).  
Shorthand for 3 separate properties: 
`flex-basis`, `flex-grow`, `flex-shrink`
How should the extra space, or lack of it, be divided between the flex items.

**flex-basis**
Basis size before dividing extra space with flex-grow and flex-shrink  

**flex-grow**     
When there is extra space, how should we divide it among every flex-item that is on the same line.   

`flex-grow: <number>;` default 0
Which means don't do anything with the extra space.

`flex-grow: 1`  
If set on every flex item, extra space is divided equally between every flex item. 

If set on one item, then that item one takes all the extra space.

if you set on one item `flex-grow: 1` and on a second item `flex-grow: 10` then the second item uses ten times more of the extra space.

**flex-shrink**
When there is not enough space, how should we extract that from every flex-item.

`flex-shrink: <number>;` default 1
Which means: extract space from every item equally.

`flex-shrink: 0` stay the same size. 

`flex-shrink: 10` when set on one item then that item gets 10 times more space extract compared to the other flex items
 

<!-- exercise 3 -->



  























