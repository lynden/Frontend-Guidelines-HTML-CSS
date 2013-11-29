Spry Framework
==============

Spry Framework is a HTML/CSS Base Framework that I use as a **starting point** on my projects.
It is not intended to be a fully functioning design/layout guide such as Bootstrap or Foundation, but rather a set of my best practices that I have built up over time. 

I set the base for a project by including only the modules it requires and then build out all the project styles from there.

Feel free to use this, adapt it or even <a href="mailto:me@lyndendesigns.com">let me know</a> if you feel you have an approach that works better as I am always keen to hear alternative view points.

CSS/SASS styleguide
--------------------

## General Formatting

- Use tabs set to 4 spaces
- Use a space before braces ` {`
- Use a space after the `:` in property declarations
- Use lowercase class names and hyphenate where applicable

``` css
.lorem-ipsum {
	width: 5em;
}
```

## Comments
Comments are key to giving a good understanding of whats going on within a document. I adopt the following approach to comments within CSS/SASS documents.

Single line comments should us `//` where possible

``` css
// Single line comment

/*    =Section level comment
------------------------------------------------------------*/
```

## Naming Convention
- All classes and values should be defined in lowercase and hyphenated e.g. `.lorem-ipsum`. 
- Classes that are modifiers should be indicated with double hyphens e.g. `.btn--s` or `.btn--primary`. A modifier is a class that alters the styling of a base class in some way, for example setting the size or urgency of a button.

####SASS Nesting
- Classes should be separated by a blank line
- If a class has nested elements within but not any styles applied directly to the root class then a line should be left to help see this easily.

``` css
// Nested class with direct styles
.lorem-ipsum {
    width: 5em;
    
    .dolor {
        color: #333;
    }
    
    .sit {
        color: #fff;
    }
}
```

``` css
// Nested class without direct styles
.lorem-ipsum {

    .dolor {
        color: #333;
    }
    
    .sit {
        color: #fff;
    }
}
```

    
