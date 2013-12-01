Frontend Guidelines (HTML/CSS)
==============

The following guidelines have been built up over the years of working on projects of varying scale and complexity, reviewing information and advice from others in the field and essentially combining all this into my workflow.

Feel free to use this, adapt it or even <a href="mailto:me@lyndendesigns.com">let me know</a> if you feel you have an approach that works better as I am always keen to hear alternative view points.

CSS/Sass styleguide
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
- Sass variables should be used when a colour is declared more than once.

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
- Try to be generic rather than specify the visual layout or style with names e.g dont use `.form-row` as this implies that it will always be a horizontal layout, instead use `.form-group` which allows flexibility in its layout.
- Classes that are modifiers should be indicated with double hyphens e.g. `.btn--s` or `.btn--primary`. A modifier is a class that alters the styling of a base class in some way, for example setting the size or urgency of a button.
- Keep class names as short as possible whilst still being meaningful.

## Selector Performance
- Dont qualify selectors unless absolutely necessary e.g. dont use `ul.nav-sub` instead simply use `.nav-sub`, this offers better performance and allows more flexibility for reusing the class on other elements.
- Selector nesting should not go deeper than 3 levels, if it does, the styles probably need refactoring or classes should be added to allow improved targeting performance.

## Comments
Comments are key to giving a good understanding of whats going on within a document. I adopt the following approach to comments within CSS/Sass documents.

- Single line comments should us `//` where possible, e.g. when using Sass.
- Section level comments are prefixed with `=` to allow easy searching within files. Their headings are also capitalised helping them stand out. The lower section comment block should be 70 characters long for consistency.
- If multiple single line comments are used within the same selector, adopt a tabbed approach to align them.

``` css
.lorem-ipsum {
	width: 20em;		// Single line comment
	background: #ccc;	// tabbed approach to align multiple single line comments
}

/*	=SECTION LEVEL COMMENT
--------------------------------------------------------------------*/

/*	=SECTION LEVEL COMMENT WITH SUB INFO
	 Sub information for the section	
--------------------------------------------------------------------*/
```

## File Structure
Below shows the general file structure used for styles. The partials vary per project but this gives a general idea. The main concept is to keep the structure as modular as possible. The partials are as follows:
- _base.scss - contains compass imports, global variables, mixins and global styles such as clearfix
- _normalize.scss - a version of Nicolas Galaghers <a href="https://github.com/necolas/normalize.css">Normalize</a> with some minor alterations
- _temp.scss - When working in larger teams sometimes quick fixes need to be made and passed onto the designer/front end dev to clean up. temp is a partial to contain these temporary styles. Contents of this file should be refactored into the other partials/main Sass before the project goes into production.
- The other partials are fairly self explanatory.

``` css
|-styles
|--- css
|--- fonts
|--- img
|--- sass
|------ partials
|--------- _base.scss
|--------- _normalize.scss
|--------- _typography.scss
|--------- _form.scss
|--------- _temp.scss
|------ screen.scss
```
