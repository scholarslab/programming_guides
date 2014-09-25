# Code Review Guidelines

A guide for reviewing code and having your code reviewed.

Everyone
--------

* Accept that many programming decisions are opinions. Discuss tradeoffs, which
  you prefer, and reach a resolution quickly.
* Ask questions; don't make demands. ("What do you think about naming this
  `:user_id`?")
* Ask for clarification. ("I didn't understand. Can you clarify?")
* Avoid selective ownership of code. ("mine", "not mine", "yours")
* Avoid using terms that could be seen as referring to personal traits. ("dumb",
  "stupid"). Assume everyone is attractive, intelligent, and well-meaning.
* Be explicit. Remember people don't always understand your intentions online.
* Be humble. ("I'm not sure - let's look it up.")
* Don't use hyperbole. ("always", "never", "endlessly", "nothing")
* Don't use sarcasm.
* Keep it real. If emoji, animated gifs, or humor aren't you, don't force them.
  If they are, use them with aplomb.
* Talk in person if there are too many "I didn't understand" or "Alternative
  solution:" comments. Post a follow-up comment summarizing offline discussion.

Having Your Code Reviewed
-------------------------

* Be grateful for the reviewer's suggestions. ("Good call. I'll make that
  change.")
* Don't take it personally. The review is of the code, not you.
* Explain why the code exists. ("It's like that because of these reasons. Would
  it be more clear if I rename this class/file/method/variable?")
* Extract some changes and refactorings into future tickets/stories.
* Link to the code review from the ticket/story. ("Ready for review:
  https://github.com/organization/project/pull/1")
* Push commits based on earlier rounds of feedback as isolated commits to the
  branch. Do not squash until the branch is ready to merge. Reviewers should be
  able to read individual updates based on their earlier feedback.
* Seek to understand the reviewer's perspective.
* Try to respond to every comment.
* Wait to merge the branch until another person signs off.
* Wait to merge the branch until Continuous Integration (TDDium, TravisCI, etc.)
  tells you the test suite is green in the branch.

Reviewing Code
--------------

Understand why the code is necessary (bug, user experience, refactoring). Then:

* Communicate which ideas you feel strongly about and those you don't.
* Identify ways to simplify the code while still solving the problem.
* If discussions turn too philosophical or academic, move the discussion offline
  to a regular Friday afternoon technique discussion. In the meantime, let the
  author make the final decision on alternative implementations.
* Offer alternative implementations, but assume the author already considered
  them. ("What do you think about using a custom validator here?")
* Seek to understand the author's perspective.
* Sign off on the pull request with a :thumbsup: or "Ready to merge" comment.

Style Comments
--------------

Reviewers should comment on missed [style](../style)
guidelines. Example comment:

    [Style](../style):

    > Order resourceful routes alphabetically by name.

An example response to style comments:

    Whoops. Good catch, thanks. Fixed in a4994ec.

If you disagree with a guideline, open an issue on the guides repo rather than
debating it within the code review. In the meantime, apply the guideline.



# Code Review Checklist

## General
- [ ] The code does what is intended by the developer.
- [ ] Variables are properly defined with meaningful, consistent, and
clear names.
- [ ] All assigned variables have proper type consistency and casting.
- [ ] There are no redundant or unused variables.
- [ ] No deprecated methods/functions in the code
- [ ] There are explanations for any commented out code.
- [ ] Code has proper indentation.
- [ ] Each method/function does only one thing.
- [ ] Variables are defined before being used.
- [ ] Code uses a uniform coding standard (that is explicitly stated
somewhere).
- [ ] The code contains no premature optimizations.
- [ ] There is no code with a generic exception and custom message.
- [ ] The code is readable as written.
- [ ] The code adheres to DRY principals (across the codebase).
- [ ] Business and presentation code are separate.
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

