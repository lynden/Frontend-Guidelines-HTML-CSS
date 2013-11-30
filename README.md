Spry Framework
==============

Spry Framework is a HTML/CSS Base Framework that I use as a **starting point** on my projects.
It is not intended to be a fully functioning design/layout guide such as Bootstrap or Foundation, but rather a set of my best practices that I have built up over time. 

I set the base for a project by including only the modules it requires and then build out all the project styles from there.

Feel free to use this, adapt it or even <a href="mailto:me@lyndendesigns.com">let me know</a> if you feel you have an approach that works better as I am always keen to hear alternative view points.

CSS/SASS styleguide
--------------------

## General Formatting

- Use tabs set to 4 spaces.
- Use a space before braces ` {`.
- Use multiline declarations.
- Properties are grouped by type and in order of importance.
- Use a space after the `:` in property declarations.
- Use lowercase class names and hyphenate where applicable.
- Colour declarations in hex unless rgba value is required.
- Use short hex format where possible e.g. `#CCC`.

``` css
.lorem-ipsum {
	width: 5em;
}
```

##SCSS Formatting
- Use SCSS syntax.
- Selectors should be separated by a blank line.
- Should a selector have nested elements within but no direct property declarations, a blank line should be left before the nested selector, this gives visual separation allowing easier scanning.
- Selectors without direct property declarations should be kept to a minimum.

``` css
// Parent selector with property declarations and nested selectors
.lorem-ipsum {
    width: 5em;
    
    .dolor {
        color: #333;
    }
    
    .sit {
        color: #fff;
    }
}

// Parent selector without property declarations and nested selectors
.lorem-ipsum {

    .dolor {
        color: #333;
    }
    
    .sit {
        color: #fff;
    }
}
```

## Naming Convention
- All classes and values should be defined in lowercase and hyphenated where applicable e.g. `.lorem-ipsum`. 
- Classes that are modifiers should be indicated with double hyphens e.g. `.btn--s` or `.btn--primary`. A modifier is a class that alters the styling of a base class in some way, for example setting the size or urgency of a button.
- Keep class names as short as possible whilst still being meaningful.


## Comments
Comments are key to giving a good understanding of whats going on within a document. I adopt the following approach to comments within CSS/SASS documents.

Single line comments should us `//` where possible, e.g. when using SASS.

Section level comments are prefixed with `=` to allow easy searching within files. Their headings are also capitalised helping them stand out.

``` css
// Single line comment

/*    =SECTION LEVEL COMMENT
------------------------------------------------------------*/
```

## File Structure
Below shows the general file structure used for styles. The partials vary per project but this gives a general idea. The partials are as follows:
- base.scss - contains all the compass import, all variables and mixins
- normalize.scss - a version of Nicolas Galaghers <a href="https://github.com/necolas/normalize.css">Normalize</a> with some minor alterations

``` css
 - styles
    - css
    - fonts
    - img
    - sass
      - partials
      	- _base.scss
      	- _normalize.scss
      	- _typography.scss
      	- _form.scss
      	- _temp.scss
      - screen.scss
```



    
