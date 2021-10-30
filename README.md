# 1.3 software requirements
 - Chrome Browser
 - VSCode(>IDE)
 - GitHub Desktop(>Git cli)
 
# 1.5 Understanding HTML
  - Website is just text of code
  - Browser read the text of code and configure it
  - Website is consist of two(or three) kind of language: HTML, CSS, JavaScript
  - HTML: tells the browser how the content is structured
  - CSS: tells the borwser what the content should look like
  - JavaScript: enables interactivity
  
# 2.0 Trivial Convention
  - keep HTML filename as 'lowercase'
  - start with `index.html`
  	- `index.html` is default for most server
	- VSCODE settings
	  - set prettier as `HTML` format
	  - `!`
	  : shortcut for basic HTML structure
	  - `link:css`
	  : shortcut for connect HTML to external CSS file
  - when doublequote(`"`) finish with doublequote
  - specific attribute are only used in specific tags
  - make sure to use semantic tag to make the meaning of code more clear
  - Search HTML Tag on MDN(Mozillia Developer Network)

# 2.2 introduction to HTML Tag
  - Basic Syntax: `<[TAGNAME] [ATTRIBUTE]="[VALUE]"> ~ </[TAGNAME]>`
  - HTML Tag looks like: <~>
  - 'Content' should be position in between tags
  	`<~> ~ </~>`
  - Attribute: add additional information to tag
  - Attribute position next to tagname and seperated with whitespace
  	`<[TAGNAME] [ATTRIBUTE]>`
  - Attribute has boolean value can omit value(because it always has default enabled)
  	`<input placeholder="~" required />`
  - Tag doesn't require text could be 'self-closing tag'
  	`<img ~ />`

# Structure of HTML file
  1. Every HTML start with `<!DOCTYPE html>`
  2. Open HTML `<html>~</html>`
  3. `<html>` is consist of two parts:
	 - `<head>`: configures the website from backstage
	 - `<body>`: content which the user will see

# Common `<head>` HTML Tag Example
   - `<title>`: Name Website appeared on TabName
   - `<meta content="~" name="~" />`: describe extra information about website
   - `<meta charset="~" />`: default "utf-8"
   - `<meta lang="~" />`: default "kr"
   - set tab icon image
   	 - `<link rel="shortcut icon" href="~" />`
   - set coverimage when share link on kakaotalk
	 - `<meta property="og:image" content="~" />`

# Common `<body>` HTML Tag Example
 - text
    - `<span>` 
 	- title: `<h1> ~ <h6>`
	- paragraph: `<p>`
	- style
		- `<strong>`
		- `<sup>` or `<sub>`
 - list
 	- there are two kind of list:
		- unordered list(`<ul>`)
		- ordered list(`<ol>`)
 	- for item, `<li>`
 - hyperlink
 	- `a` stands for anchor
	- a requires href(hyperlink reference) attribute
	- `<a href="~">~</a>`
	- a can have optional attribute: target
	  - `_self`: default. replace the originial one
	  = `_blank`: appear on new tab
  - image
  	- `<img src="~"/>`
	- attribute
		- src(source): image source as link
  - forms
    - `<form> ~ </form>`
	  - attrib: action
	    - which page do you send data
	  - attrib: method
	    - what method do you handle data
		- GET / POST
  	- input: `<input type="~" />`
		- attrib: type
			- type="text"(default)
			- type="color"
			- type="file"
				- accept="[FILE_EXTENSION]"
				- For all image: "image/*"
			- type="url"
			- type="email"
			- type="date"
		- textbox
			- type="text"
			- type="password"
			- placeholder="~"
		- button
			- type="submit"
			- value="~"
		- other attribs
			- required
			- disabled
			- minlength
			- maxlength
	- label: `<label for="~">`
		- `<label>` works with `<input>`
		- make sure 'for' and 'id' value should be same
		- <label for=> & <input=id=>
		
# 2.9 class and id attributes
  - class
    - class can be used on multiple element
	  - `<span class="tomato">`
	- multiple classes can be used in single element
	  - `<span class="tomato btn top">`
	- to use as CSS selector, it should starts with ".[CLASS_NAME]"
  - id
	- id's value should be unique in whole document
	- one id per one element
	- to use as CSS selector, it should starts with "#[ID_NAME]"
	
# 6.2 BEM(Block Element Modifier)
  - accodring to BEM, every selector should be only `class`(none of `id`)
  - block component
    - `.[BLOCK] {}`
  - element that depends upon the block(sub-block)
    - `.[BLOCK]__[ELEMENT] {}`
  - modifier that changes the style of the block
    - `.[BLOCK]--[MODIFIER] {}`

# 6.4 Emmet Abbreviation
  - Shortcut create HTML element more easier
  - Abbv
  	- `.`
	  - `<div>`
	- `div>span`
	  - `<div> and inside <span>`
	- `span*5`
	  - `5 spans`
	- `[TAGNAME].[CLASS_NAME]`
	  - `<[TAGNAME] class="[CLASS_NAME]">`
  
# 2.10 Semantic Tag
  - Non-Semantic Tag
    : just a container
	  - `<div>`
	  - `<span>`
  - Semantic Tag
  	: make purpose clearly by adding name
	  - `<header>`
	  - `<main>`
	  - `<footer>`
	  - `<nav>`
	  - `<section>`

## Path Notation
	- ..
	- /
	
# 3.0 Introduction to CSS
  - CSS(Cascading Style Sheet): add properties on HTML Element to make website beautiful
  - CSS point at HTML Element and describe what properties have
  - There are two ways to add CSS into HTML:
    1. `<head> <style>`(in one file)(=inline CSS)
		
	2. Create seperate CSS file(.css)(=external CSS)
		`<link href="[PATH_TO_CSS_FILE]" rel="stylesheet" />`
  - Basic Syntax:
  	```
	[SELECTOR] {
		[PROPERTY]: [VALUE];
	}
	```
	- selector: indicate which element is selected
	  - tag name: [TAG_NAME]
	  - class: .[CLASS_NAME]
	  - id: #[ID_NAME]
	  - everything: *
	- multiple selectors use comma(,)
	- property should be in one word(dash(-) instead of whitespace)
	- value could have specific size measurement ex) px, em, pt, %, vw, vh
	- always add semi-colon(;) at the end
  - `Cascading` means browser read CSS code top to bottom
    - if property contradict, order between `<style>` and `<link>` determine what property finally being applied

  * size measurement
    - vh: viewport height
	  : % in proportion to screen size ex. 100vh
	- vw: viewport width
	
# Common CSS property Example
  - font
    - font-size(px)
	- font-weight(per100)
	- font-style
	  - italic
  	- color
	  - inherit(inherit color from parent element)
	- instead of gray color, use `opacity`
	- text-decoration
	  - underline
	  - none
	- font-family: ~;
	  - [Link](fonts.google.com)
  - text
    - text-align
	  - center
	- text-transform
	  - uppercase
  - container
  	- width / height
    - background-color
	- border-radius
	  - px, %
	  - 50% = circle
	- opacity (%, 1)
  - button
    - cursor
	  - pointer / not-allowed / progress
	
# CSS Concept 1: Blocks and Inline
  - Block: prevent other elements come next to it
    - Everything except for Inline has default as block
  - Inline: allow other elements in the same line
    - `<span>`,`<a>`, `<img>` has default as inline
	- inline doesn't have width and height
  - Inline-Block: allow block can be next to each other
    - inline block are not compatiable to responsive design
  - related CSS properties
    - display
	  - block
	  - inline
	  - inline-block

# CSS Concept 1-1: Margin / Padding / Border
  - `margin`, `padding`, `border` is one of the properties that container has
  - browser give default value to every HTML element
  - margin
  	: space from the border to the outside
	- collapsing margin
		- when inner and outer element's margin are the same, it serve as one element
  		- only happen vertical side of margin
  - padding
    : space from the border to the inside
	- border-box
	  - when width and padding exist together, element size exceed as sum of them
	  - to maintain the size of element, `box-sizing: border-box;`
  - border
    : border of the container
	[Link](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style)
	
  - related CSS properties
    - margin / padding
	  - (one value): 10px; lrtb
	  - (two value): 20px 15px; tb lr
	  - (four value): 20px 5px 12px 15px; t l b r
	- margin-left / margin-right / margin-top / margin-bottom
	- padding-left / padding-right / padding-top / padding-bottom
	- negative margin is available, `margin-top: -10px;`
	- border
		- `border: [THICKNESS] [STYLE] [COLOR];`
		  - [STYLE] always 'solid'(rarely 'dashed')
		- reset border(especially `<input>`) as `border: none;`
		- border-top / border-bottom / border-left / border-right

# 3.10 CSS Concept 2: FlexBox
  - Origin: To Fix inline block's responsive problem
  - There are some principle to be valid for flexbox:
  	1. add properties to flex container(parent) instead of items(children)
	2. main-axis is justify-content, cross-axis is align-items
	  - as default, main-axis is horizontal, cross-axis is vertical
  - to use flexbox, add property `display: flexbox;`
  - related CSS properties
    - justify-content
	- align-items
	  - center
	  - flex-start(default) / flex-end
	  - space-evenly
	  - space-around
	  - space-between
	  - stretch
	    - only works when doesn't have fixed value of height
	- flex-direction
	: invert main-axis and cross-axis
	  - row(default)
	  - column
	  - add `-reverse` at the end to invert the border
	- order
	: set order of flex-children elements
	  - default is 0
	  - the number increase, the most priority

# 3.12 CSS Concept 3: Position
  - position: modify the position of element
  - position are used with `top / bottom / left / right` to adjust in detail
  - `static` is default value
  - `fixed`
    - fixed position regardless of scrolling
	- when element fixed, it located in different layer which could effect to other element's position
	- to make other element in position, use margin-top in `<body>`
	- final position is determined on `top / right / bottom / left`
  - `relative`
    - positioned as static
	- offset relative to itself based on `top / right / bottom / left`
  - `absolute`
    - positioned to its closest relative parent element
	- without relative parent, it will be placed relative to `<body>`
	- final position is determined on `top / right / bottom / left`
  - top / bottom / left / right: 0;
    - place element from end of the screen
  - `position: none` will make element vanish
  - `z-index`
    - determine element order which come in front or back
	- applied to absolute or fixed position element
	- default is 0
	- value is integer, the value increase, the level increase 


# 3.14 CSS Concept 4: Pseudo Selector & Combinator
  - pseudo selector: help point element more specific
	  - pseudo selector starts with colon(`:`)
	  - instead of specify with class or id name, it's useful
	  - :first-child
	  - :last-child
	  - :nth-child(~)
		- [NUM] / even / odd / *n*
  - attribute selector
    - TAG:required
	- TAG:optional
	- TAG[attrib="value"]
	  - select tag that has attribute and exact value
	- TAG[attrib~="value"]
	  - select tag that has attribute and exact value with space
	- TAG[attrib*="value"]
	  - select tag that has attribute and contain value
	- TAG[attrib^="value"]
	  - select tag that has attribute and value as prefix
	- TAG[attrib$="value"]
	  - select tag that has attribute and value as suffix
  - combinator
	  - `[PARENT] [CHILD]`
		- select child element inside of parent element
	  - `[PARENT] > [CHILD]`
		- select direct child element of parent element
	  - `[ELEMENT] + [ELEMENT]`
		- select element next to sibling element
	  - `[ELEMENT] ~ [ELEMENT]`
		- select element that has sibling element(don't have to be direct)
  - etc.
	  - ::placeholder
		- give property to placeholder
	  - ::selection
		- change property of selection
	  - ::first-letter
		- give property to first letter of element
	  - not(~)
	    - exclude effect some of condition

# 3.17 All about State
  - state:
  - [ELEMENT]:active
    - when mouse is being clicked
  - [ELEMENT]:hover
    - when mouse on top
  - [ELEMENT]:focus
    - selected by keyboard
	- to remove selected sign, `outline: none;`
  - [LINK]:visited
    - when link has visited
  - [PARENT_ELEMENT]:focus-within
    - applied to parent element when child element is focused
  - [PARENT]:[STATE] [CHILD]
    - when parent as in state, child is selected
  - [PARENT]:[STATE] [CHILD]:[STATE]
    - when both parent and child are in state, child is selected

# 3.19 CSS variable(custom property)
  - 3 Color System
    - Hexadecimal(16) Color
	  - Color Code(#~);
	- RGB Color (R,G,B =< 255)
	  - rgb(Red, Green, Blue);
	- RGBa (R,G,B =< 255, 0 =< Alpha <= 1)
	  - rgba(Red, Green, Blue, Alpha);
  - save color variable in `:root`
    ```
	  :root {
	    [VARIABLE]: [COLOR_VALUE];
	  }
	```
	  - variable should starts with `--`
	  - whitespace as `-`
		- `--main-color`
	  - to use variable, `var([VARIABLE])`
	  - variable can save other stuff, too


# 4.0 Transition & Transformation & Animation
  - Transition
  : animate change one state to another
    - give property to non-state selector
	- state is needed to give effect when transition happens
	- `transition: [TARGET-PROPERTY] [DURATION] [EASING F]`
	- when transition all property, use `all`
	- [DURATION] measurement are `s`(second), ms(mili-second)
	- [EASING FUNCUNTION]
	  - linear
	  - ease-in
	  : getting faster as time pass
	  - ease-out
	  : fast at first then getting slower
	  - ease-in-out
	  : first slow, accelerate, slower at the end
	  - cubic-bezier(a,b,c,d)
	  : create custom curve
  - Transformation
  : modify element property to another(static)
    - `transform: [TRANSFORMATION F]`
	- transformation only applied to specific element, but not applied to sibiling elements
	- transformation + transition
	  - `transition: transform ~;`
	- [TRANSFORMATION_FUNCTION]
		- rotateX / rotateY / rotateZ
		- scaleX / scaleY
		- translateX 
  - Animation
    - define animation as `@keyframe`
  	- ```
	@keyframes [ANIM_NAME] {
		from { ~ }
		to { ~ }
	}
	```
	- instead of using `from` and `to`, percentage is available. (from=0%, to=100%)
	- apply animation as property
	- `animation: [ANIM_NAME] [DURATION] [EASING F] [DELAY];
	  - [DELAY]
	  - infinite
	  : repeat infinitely
	  - forwards
	  : remember last keyframes
	- animation-delay
	  `delay animation for certain amount of time`
	- will-change
	  - make rendering animation stable
	  - `will-change: transform;`
	  
# 4.5 Media Queries
  - detect screen size only with CSS
  - basic syntax:
    - `@media screen and ([CONDITION]) { [SELECTOR] }`
	- [CONDITION]
	  - max-width: ~
	  - min-width: ~
	  - min-device-width / max-device-width(only for phone)
	  - orientation: landscape
	  - orientation: portrait
	- if multiple conditions, use and in between
	- `[SELECTOR]` need `[PROPERTY]`	
  - How to experiment media queries in phone
    - `chrome - inspector - device toolbar`
  - `@screen print` could provide layout when printing
  

# 6.1 HTML Configuration Procedure
  - first, create container "<div>"
  - instead of "<div>", use semantic tags
    - <header>, <nav>, <main>
  - when element should have input, then use "<form>"
    - for button, use <input type="submit">
  - if just text, then use "<span>"
    - for title, use "<h~>"
	- for long text, use "p"
  - Q. is element used only one time or several time?
	  - when element is unique one, use `id`
	  - when element are used repeatedly, use `class`
  - to seperate container horizontally, create "column <div>"
  - Comment your plan as `<!-- -->`
  

# 6.3 Text Icon: Font-awesome
  - there are two ways to use icon,
    - First, upload icon images or svg
    - Second, import font-awesome javascript code
	  - `<script src="https://kit.fontawesome.com/6478f529f2.js" crossorigin="anonymous"></script>`
  - how to use font-awesome icons,
    - search available icon
	- copy and paste the exact tag
	  - ex. `<i class="fas fa-wifi"></i>`
	- adjust icon size
	  - add class `fa-[SIZE]` in <i>
	  - [SIZE]: xs / sm / lg / 2x / ~x

  * common icon name
    - ellipsis(horizontal three-dots)
	- hamburger(stacked 3 bars)
	- cog(gear shape)
	- angle(V-shape arrow)
	- chevron(V-shape arrow)
	- caret

# 6.6 CSS Configuration Procedure
  - mkdir `/css`
  - touch `css/styles.css`
  - `link:css` in index.html
    - `<link rel="stylesheet" href="css/styles.css">`
  - reset css
    : disable browser default CSS
    - [Link](https://meyerweb.com/eric/tools/css/reset/)
    - create `css/reset.css` and `@import` it
	- if element has repeated properties, put them in reset css
  - organize element with `display` and `position`
    - fixed element
	  - top
	  - bottom
  - give vertical and horizontal gap between element
    - give equal amount of margin to same kind of element
	- method 1: margin to one side
	  - margin-right: ~px; (horizontal)
	  - margin-bottom: ~px; (vertical)
	- method 2: margin on both side
	  - margin: 0 ~px; (horizontal)
	  - margin: ~px 0; (vertical)
  - modulize and segmentize CSS into files
    - mkdir `css/screens` and `css/components`
	- when css used repeatedly, put in `components`
	- when css used in specific screens, put in `template`
	- when css used globally(as default), put in `styles.css`
	  - font-family / font-color
	  - padding-top (if top-fixed)
	  - <body> height: 100vh;
	- `@import` them into `styles.css`
	  - `@import [PATH];`
	- import order is important: font > reset > component > template

# Useful CSS Element Example:
  - text
  - link
    - disable default browser link style
	  - `text-decoration: none;`
	  - `color: inherit;`
  - text input
    - clean text input
	  - `border: none;`
	  - `border-bottom: 1px solid rgba(0,0,0,0.2);`
	  - `padding & margin`
    - text input click effect
	  - `[INPUT]:focus` amplify value of element
	  - `transition: [ELEMENT] .3s ease-in-out;`
  - submit input
    - padding(vertical) & background-color
	- border-radius
  - splash-screen
    - create splash screen
	- animation opacity 1 to 0
	- ignore splash screen(to click other element)
	  - `visibility: hidden;`
	- delay animation for start
	  - `animation-delay: 2s;`

# 6.5 CSS Hack
  - Align middle element into center
    - flex center the container
	- width 33% for each column in container
	- middle element as flex center, last element as flex flex-end
  - Align middle element(out of 3) into center with auto
  	- flex center the container
	- first-child, margin-right: auto;
	- last-child, margin-left: auto;