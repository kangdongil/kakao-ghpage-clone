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

# 2.2 introduction to HTML Tag
  - Syntax: <~> ~ </~>
  - HTML Tag looks like: <~>
  - 'Content' should be position in between tags
  	`<~> ~ </~>`
  - Attribute: add additional information to tag
  - Attribute position next to tagname and seperated with whitespace
  	`<[TAGNAME] [ATTRIBUTE]>`
  - Tag doesn't require text could be 'self-closing tag'
  	`<img ~ />`

# Structure of HTML file
  1. Every HTML start with `<!DOCTYPE html>`
  2. Open HTML `<html>~</html>`
  3. `<html>` is consist of two parts:
  	- `<head>`: configures the website from backstage
	   - `<title>`: Name Website Name appeared on TabName
	- `<body>`: content which the user will see
# Common HTML Tag Example
 - title
 	- <h1> ~ <h6>
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

## Path Notation
	- ..
	- /
	