# Code Standards for C++

Make code formatting changes into their own seperate commit before or
after your work

## Line lengths
* Hard quota  
  Hard stop at 120 maybe  
* Soft quota  
  Don't start a new word after this  

## Magic String Literals, characters and Numbers
* Magic is bad
* Define them to something and comment on significance

## Naming Things
* General rule:
  * functions are verbs
  * variables are nouns

* Files
  * Naming  
    Should main be 'main' or the appname contain main
     * Class name should be name otherwise unless its collection of utils
  * Extentions
     * .cpp : implementation
     * .h : headers  
       maybe use . hpp
     * what about inlines files  
       maybe use .ipp
* Preprocessor Macros
  * Defines
  * Conditionals
  * Functions
     * Functions should be written so that it requires user to provide the terminating ';'
* Globals
  * Variables  
    All Caps and underscores: FOO_BAR
  * Functions  
    Ideas?
* Locals
  * Variables  
    we seem to use rptype notation and camel casing or underscores
  * Functions  
    lower first letter for functions
    CamelCasing/Underscores?
* Classes  
  First letter capitalized, camel casing
  * Variables  
     rps style
     * Do we differ naming statics vs instance
     * Do we seperate private from public?
  * Functions
     * Do we differ naming statics vs instance  
       suggest upper case first letter for static and lowercase first letter for instance
     * Do we seperate private from public?
     * Virtual should only appear when declaring base virtual method
        * Override keyword should be used elsewhere

## Whitespace
* Spaces/tabs
  Spaces only ( except for makefiles )
* Trailing  
  No trailing spaces
* Leading ( Indent )  
  Indent by two's
* Lines between constructs
  * Between Classes  
  2 lines
  * Between Class function def's  
  1 line
* Operators
  * One space before and after a binary operator
  * One space after comma  
  'a + b' not 'a+b'
  * One space after parenthesis before arguments and before closing  
  '( x, y )'
  * exception : initializer lists
* After keywords
  * Insert a space  
  i.e. 'for (' not 'for('
* Functions
  * No space between function and opening parenthesis  
  'foo(..)' not 'foo (..)'

## Includes
* Ordering
  1. Header for file
  1. Std system includes
  1. Project includes
* Quotes vs. angle brackets
* Contents
  * Include anything used in file
     * Don't rely on other files to pull in needed includes
  * Avoid unneeded includes
     * forward declare when possible
