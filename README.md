# Code Review Checklists

## General
- [ ] The code does what is intended by the developer.
- [ ] Variables are properly defined with meaningful, consistent, and
clear names.
- [ ] All assigned variables have proper type consistency and casting.
- [ ] There are no redundant or unused variables.
- [ ] No deprecated methods/functions in the code
- [ ] There are explinations for any commented out code.
- [ ] Code has proper indentation.
- [ ] Each method/function does only one thing.
- [ ] Variables are defined before being used.
- [ ] Code uses a uniform coding standard (that is explicitly stated
somewhere).
- [ ] The code contains no premature optimizations.
- [ ] There is no code with a generic exception and custom message.
- [ ] The code is readable as written.
- [ ] The code adheres to DRY principals (across the codebase).
- [ ] Business and presentation code are seperate.
- [ ] The code does not use shortcut syntax.
- [ ] Reasonable error conditions are handled.

## JavaScript
- [ ] No functions or variables in the global namespace
- [ ] Do not append to the DOM in a loop
- [ ] Styles are kept in CSS

## Ruby
- [ ] Class is no longer than 100 lines of code.
- [ ] Methods are no longer than 5 lines long.
- [ ] No more than 4 parameters are passed to a method; no hashes.
- [ ] Rails controllers only instantiate 1 object
- [ ] Rails views only know about 1 instance variable


## PHP
- [ ] A function/method shall not be longer than 40 lines.
- [ ] There are no *magic numbers*.
- [ ] Recursive functions have lots of tests...

## SCSS
- [ ] Generated CSS is valid.

## HTML
- [ ] HTML generally conforms to HTML5 standard.

## Web Applications
- [ ] Copy has been proofed for grammer/syntax.
- [ ] Latest versions of dependencies are being used.
- [ ] No passwords are in the source code.
- [ ] Images are compressed.
- [ ] JavaScript is concatenated and compressed.
- [ ] Dependencies for building are declared (e.g. `Gemfile`, `package.json`, `bower.json`, `composer.json`)
- [ ] Server dependencies are explicitly noted.
- [ ] Everyone knows who to call when something breaks.
- [ ] Everyone (who is supposed to) can deploy the web application.


## Security
- [ ] XSS has been tested.
- [ ] Login forms (and password reset forms) are secure.

