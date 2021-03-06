# drop

## Drop the base, base html &amp; sass

This is a loose framework that I use to build my own projects on top of.

It is by no means perfect but is developed from a **very particular set of skills; skills I have acquired over a short career in the web.** (Read best in the voice of Liam Neeson).

This little guide covers how I like to format & structure my SCSS/CSS & HTML.

Also as with most frameworks it is a collection of bits and pieces created by myself and others, if bits are used they are credited in place.

## HTML

Nesting elements can get messy so I like to comment off my elements with HTML comments as followed.

`````css
<div class="class">
</div><!-- //.class -->
`````

### Multiple Classes

If there are load of classes on a HTML element then simply chain the closing comments as followed:

`````css
<div class="class second third">
</div><!-- //.class //.second //.third -->
`````

**This can obviously become as confusing as no comments at all if overused so use sparingly.**

## CSS

### Comments

Use comments to block out and explain sections of code, this is particularly useful when using SCSS as code is split across a range of files.

#### Document Heading

Place a file heading comment denoting the name of the file as a quick reference and any additional info such as dependencies or links to code examples or author attribution.

E.g.

`````css
/*------------------------------------*\
    $FILENAME
  * @author:
  * @version:
  * @example: 
\*------------------------------------*/
`````

#### Sections

Use comments to break up code sections within a file, as followed:


`````css
/* ==========================================================================
   Section comment block
   ========================================================================== */

/* Sub-section comment block
   ========================================================================== */

/**
 * Short description using Doxygen-style comment format
 *
 * The first sentence of the long description starts here and continues on this
 * line for a while finally concluding here at the end of this paragraph.
 *
 * The long description is ideal for more detailed explanations and
 * documentation. It can include example HTML, URLs, or any other information
 * that is deemed necessary or useful.
 *
 * @tag This is a tag named 'tag'
 *
 * TODO: This is a todo statement that describes an atomic task to be completed
 *   at a later date. It wraps after 80 characters and following lines are
 *   indented by 2 spaces.
 */

/* Basic comment */
`````

#### Declaration Order

Keep declarations consistently ordered, this helps with readability.

`````css
.selector {
    /* Positioning */
    position: absolute;
    z-index: 10;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;

    /* Display & Box Model */
    display: inline-block;
    overflow: hidden;
    box-sizing: border-box;
    width: 100px;
    height: 100px;
    padding: 10px;
    border: 10px solid #333;
    margin: 10px;

    /* Other */
    background: #000;
    color: #fff;
    font-family: sans-serif;
    font-size: 16px;
    text-align: right;
}
`````

### Naming Conventions

##### Add a space over a property's colon

`````css
position: relative;
`````

as opposed to

`````css
position:relative;
`````

#### Long Class Names

When you're using a long class name, use hypens to break up the single works e.g.

`````css
.large-class-name {}
`````

##### BEM

I'm currently adopting a BEM naming convention so all classes should follow the principle of:

`````css
.block {}
.block__element {}
.block--modifier {}
`````

You can read more on this at [B.E.M](http://bem.info/)

### Tabs & Spaces

Personal preference is tabs.

### ID's

To avoid specificity problems, avoid styling off ID's where possible.

## JS Hooks

To avoid a messy overlap of CSS & JS write set hooks for JS either ID's or Classes.

`````css
#js-
.js-
`````

### *This is a fluid document that will be updated as I go.*


