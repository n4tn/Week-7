# Week-7
Web Development

# HTML
HyperText Markup Language - structure of a webpage,  similar to XML and has tags

anything in the head is NOT rendered by the webpage minus the title

Meta: ??
 
### **Dont use HTML for visualisation**

HTML 5:
- Made some previous features not used
- new semantic markup to give meaningful structure
- Discourages the use of inline styles and favours the use of CSS
- Supports design responsiveness
- Promotes accessibility, hence semantic tags
- has multimedia support 

[HTML5](https://html.com/html5)

Semantic elements add meaning to page elements (clearly defines its content) - dont provide functionality but are used for screen readers and other assistive tech

- link is an anchor tag

- section tag is the new version of div tag https://www.w3.org/TR/2011/WD-html5-20110525/sections.html

GitHub Pages - set up in the lesson

# CSS
Cascading Style Sheets - used to add style to our elements 

- Works off key: value pairs

3 Styles:
1. Inline - style= "key:value" - least flexible and applied last (try not to use these)
2. Style tag - defined in the head 
3. Style sheet - needs a link tag in the head 

selector: selects which elements the style grouping applies to

- id should be unique (selector is #)
- class is a custom name which we can apply to any element (selector is a .)
- Wildcard applies to everything (selector is a *)

css has several different units to express length:
- em (relative to font-size of the element)
- rem (relative to root)
- vw (view width)
- vh (view height)
- % (relative to the parent element)

Color only refers to font colour

Selectors:
- combinators (for example a class & the lists in the class)
- Flex - a way to organise the child elements of a root element 
  - https://css-tricks.com/snippets/css/a-guide-to-flexbox/ 

# JavaScript
Just in time compiled language

- weakly typed - dont have to define data types
- dynamically typed - variable can be overwritten
  
https://www.ecma-international.org/publications/standards/

## Compiled vs Interpreted:

complied has to turn code into machine code (better for computationally demanding things)

interpreted is compiled as you are running it

# Razor Pages
A server-side templating engine to generate HTML to send to the client for rendering

Razor paages include:
- HTML
- CSS
- JS
- Razor markup @page
- C# code @
- Tage Helpers

![Image](./Razor%20PageModel.PNG)

![Image](./MVC%20v%20RazorPages.PNG)

Which framework to use?
- MVC
  - Established
  - Action focussed
  - Controller can become huge
  - Controller, models and view of the same resource in different folders
  - Good for larger apps with lots of logic between the controller and models
- Razor Pages
  - New, may be favoured for futere dev
  - Page focussed
  - Many small pages
  - Compact folder structure
  - Good for small apps or ones with CRUD operations
  - Easier to understand?  

# Authentication & Authorization
- who are you and how can you prove it?
- depends on who you are if you can see this

both controlled by the middleware in the request pipeline but Authentication must be first

