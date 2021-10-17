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
  	`~~`
  - Tag doesn't require text could be 'self-closing tag'
  	`<img ~ />`

# Structure of HTML file
  1. Every HTML start with `<!DOCTYPE html>`
  2. Open HTML `<html>~</html>`
  3. `<html>` is consist of two parts:
	 - `<head>`: configures the website from backstage
	 - `<body>`: content which the user will see

# Common `<head>` HTML Tag Example
   - `<title>`: Name Website Name appeared on TabName
   - `<meta content="~" name="~" />`: describe extra information about website
   - `<meta charset="~" />`: default "utf-8"
   - `<meta lang="~" />`: default "kr"
   - set tab icon image
   	 - `<link rel="shortcut icon" href="~" />`
   - set coverimage when share link on kakaotalk
	 - `<meta property="og:image" content="~" />`

# Common `<body>` HTML Tag Example
 - text
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
		
# 2.9 class and id attrib
  - class
  - id
	- id's value should be unique in whole document
	- one id per one element
	- to use as selector, it should starts with "#[ID_NAME]"

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
		`<link href="styles.css" rel\"stylesheet" />`
  - Basic Syntax:
  	```
	[SELECTOR] {
		[PROPERTY]: [VALUE];
	}
	```
	- selector: indicate which element is selected
	- property should be in one word(dash(-) instead of whitespace)
	- value could have specific size measurement ex) px, em, pt, %
	- always add semi-colon(;) at the end
  - `Cascading` means browser read CSS code top to bottom
    - if property contradict, order between `<style>` and `<link>` determine what property finally being applied

# Common CSS property Example
  - font
    - font-size(px)
	- font-weight(per100)
	- font-style
	  - italic
  	- color
	- text-decoration
	  - underline
  - text
    - text-align
	  - center
  - container
  	- width / height
    - background-color
	
# CSS Concept 1: Blocks and Inline
  - Block: prevent other elements come next to it
    - Everything except for Inline has default as block
  - Inline: allow other elements in the same line
    - `<span>`,`<a>`, `<img>` has default as inline
	- inline doesn't have width and height
  - related CSS properties
    - display
	  - block
	  - inline

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
  - border
  - related CSS properties
    - margin / padding
	  - (one value): 10px; lrtb
	  - (two value): 20px 15px; tb lr
	  - (four value): 20px 5px 12px 15px; t l b r
	- margin-left / margin-right / margin-top / margin-bottom
	- padding-left / padding-right / padding-top / padding-bottom
	- 