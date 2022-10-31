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

# Question Bank

## HTML & CSS
- What are the new features of HTML5?
  -  semantic markup to give meaningful structure
  - Discourages the use of inline styles and favours the use of CSS
  - Supports design responsiveness
  - Promotes accessibility, hence semantic tags
  - has multimedia support
- What is the difference between the head and header tags?
  - head is the tag at the top of your page containing your meta-tags, styles, scripts and title. headings are the h1, h2, h3 etc tags that allow you to size your text.
-  What is a nav element?
   -  represents a section of a page whose purpose is to provide navigation links, either within the current document or to other documents.
-  What does CSS stand for?
   - Cascading Style Sheets
-  what does cascading mean in css?
   1. Inline - style= "key:value" - least flexible and applied last (try not to use these)
   2. Style tag - defined in the head 
   3. Style sheet - needs a link tag in the head
- Give some examples of CSS selectors
  - id 
  - class
  - wildcards
  - combinators (for example a class & the lists in the class)
  - Flex - a way to organise the child elements of a root element
- What is the difference between an id and a class?
  - an ID is only used to identify one single element in our HTML
- What is the prefix for an id?
  - (#)
- What is the prefix for a class?
  - (.)
- What is the CSS box model?
  - essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content 
- Why are inline styles not a good idea?
  -  it does not support (or it has really poor support) for CSS features

## JavaScript
- Is Javascript statically or dynamically typed?  What does that mean?
  - dynamically, variable can be overwritten and you dont have to define data types (let)
- How do you tell if you have made a javascript error? 
  - F12 on webpage under DevTools there is a console
- What are some examples of events that javascript can respond to? (for example when button clicked then...)
  - An HTML web page has finished loading.
  - An HTML input field was changed.
  - An HTML button was clicked.
- Where is the best place to put your javascript and why?
  -  put JavaScript script tags just before the closing body tag, this is because HTML loads from top to bottom
- What is the difference between a javascript and a c# class declaration?
  - no need to define return type with function keyword in signature
- What is the DOM?
  - Document Object Model that allows programs and scripts to dynamically access and update the content (objects, properties, methods & events)
- What is Bootstrap?
  - CSS Framework for developing responsive and mobile-first websites
- What is JQuery?
  - JavaScript library. It makes things like HTML document traversal and manipulation, event handling, animation, and Ajax much simpler with an easy-to-use API that works across a multitude of browsers. 
- How can DOM elements be accessed?
  - id
  - class
  - tag
  - query selectors 

## ASP.NET Razor Pages
- What do ASP.NET API and ASP.NET Razor pages apps have in common?  What are the differences?
  - Razor Pages group together the action (now a handler) and the viewmodel (called a PageModel) in one class, and link this class to the view (called a Razor Page). 
  - Handlers behave exactly like action methods but have the HTTP verb they handle in their name
- Where does dependency injection take place in a Razor Pages application?
  - program.cs 
- Where is the database context registered with the Dependency Injection container?
  - program.cs
- What are the advantages/disadvantages of adding a service to the DI container with Singleton lifetime?
  - Creates a new Service only once during the application lifetime, and uses it everywhere, memory efficient as they are created once reused everywhere. 
  - Any memory leaks in these services will build up over time
-  What other lifetimes are available?  What is the default lifetime for a database context class?
   - Transient & scoped
   - scoped (using block) : less memory usage and has a long enough duration
- What is in the Web folder of an ASP.NET application?
  - css
  - js
  - libraries
- What actions happen on startup of an ASP.NET application?
  - x
- Where does data validation take place in Web application?
  - data validation is handled on the server although some validation can also occur on the client before data is submitted to the server
- What happens to data validation if javascript is disabled on the client browser?
  -  Validation will not work 
- How are the default web pages structured?
  - x
- How are requests routed to the correct page and method?
  - matching URLs to file paths, starting from the root Razor Pages folder, which is named Pages by default , also using razor syntax (@)
- How and why do the PageModel classes use asychronous methods?
  - through async methods using the @model:applications should be able to handle many requests simultaneously.
- Why would we want to seed the database?
  - dummy data to test

## More about Web Frameworks
- Where/when is the C# code in a Razor page executed?
  - All C# code is run when the razor view is called to produce the HTML
- Where/when is the Javascript code in a Razor page executed?
  - Once the browser loads the HTML, any JavaScript in the view will be executed
- How is C# code indicated in Razor pages?
  - (@)
- What is model binding?
  - a simplistic way to correlate C# code with an HTTP request  

