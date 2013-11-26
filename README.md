Spry Framework
==============

Spry Framework is a HTML/CSS Base Framework that I use as a **starting point** on my projects.
It is not intended to be a fully functioning design/layout guide such as Bootstrap or Foundation, but rather a set of my best practices that I like to use. 
I set the base for a project by including the modules that it requires and then build out the styles that the project requires from there.

Feel free to use this, adapt it or even <a href="mailto:me@lyndendesigns.com">let me know</a> if you feel you have an approach that works better as I am always keen to hear alternative view points.

CSS/SASS styleguide
--------------------

### Naming Convention
- All classes and values should be defined in lowercase and hyphenated e.g. `.lorem-ipsum`. 
- Classes that are modifiers should be indicated with double hyphens e.g. `.btn--s` or `.btn--primary`. A modifier is a class that alters the styling of a base class in some way, for example setting the size or urgency of a button.

### Spacing

####General

A space should always follow an attribute before the value is defined, for example `width: 5em;`. Styles should be indented
 using 1 tab with the spacing set to 4 spaces.

``` 
.lorem-ipsum {
    width: 5em;
}
```

####SASS Nesting
- Nesting follows the 4 space tab approach
- Classes should be separated by a blank line
- If a class has nested elements within but not any styles applied directly to the root class then a line should be left to help see this easily.

``` 
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

// Nested class without direct styles
.nested-class-without-direct {

    .dolor {
        color: #333;
    }
    
    .sit {
        color: #fff;
    }
}
```

    
