# Git commit message

Source: https://github.com/joelparkerhenderson/git_commit_message

To write a great git commit message, take a look at these guidelines and suggestions.


## Summary

Begin with a short summary line a.k.a. message subject:

  * Start with an imperative present active verb: Add, Drop, Fix, Refactor, Optimize, etc.

  * Use up to 50 characters; this is the git official preference.
  
  * Finish without a sentence-ending period.


## Body Description

Continue with a longer description a.k.a. message body:

  * Add a blank line after the summary line, then write as much as you want.
  
  * Use up to 72 characters per line for typical text for word wrap.

  * Use as many characters as needed for atypical text, such as URLs, terminal output, formatted messages, etc.

  * Include any kind of notes, links, examples, etc. as you want.


## Summary keywords

We recommend these summary keywords because they use imperative mood, present tense, active voice, and are verbs:

  * **Add**: Create a capability e.g. feature, test, dependency.

  * **Drop**: Delete a capability e.g. feature, test, dependency.

  * **Fix**: Fix an issue e.g. bug, typo, accident, misstatement.

  * **Bump**: Increase the version of something e.g. a dependency.

  * **Make**: Change the build process, or tools, or infrastructure.

  * **Start**: Begin doing something; e.g. enable a toggle, feature flag, etc.

  * **Stop**: End doing something; e.g. disable a toggle, feature flag, etc.

  * **Optimize**: A change that MUST be just about performance, e.g. speed up code.

  * **Document**: A change that MUST be only in the documentation, e.g. help files.

  * **Refactor**: A change that MUST be just refactoring.

  * **Reformat**: A change that MUST be just formatting, e.g. change spaces.

  * **Rearrange**: A change that MUST be just arranging, e.g. change layout.

  * **Redraw**: A change that MUST be just visual, e.g. change a graphic, image, icon, etc.

  * **Reword**: A change that MUST be just textual, e.g. change a comment, label, doc, etc.


## Usage

Put the template file here:

     ~/.git_commit_template.txt

Configure git to use the template file by running:

     git config --global commit.template ~/.git_commit_template.txt

Add the template file to our ~/.gitconfig file:

    [commit]
      template = ~/.git_commit_template.txt

If you prefer other file locations or ways of working,
you can freely adjust the usage as you like.


## Real-world examples

Real-world examples show how we use imperative mood, present tense, active voice, and verbs:

  * [**Add**] feature for a user to like a post

  * [**Drop**] feature for a user to like a post

  * [**Fix**] association between a user and a post

  * [**Bump**] dependency library to current version

  * [**Make**] build process use caches for speed

  * [**Start**] feature flag for a user to like a post

  * [**Stop**] feature flag for a user to like a post

  * [**Optimize**] search speed for a user to see posts

  * [**Document**] community guidelines for post content

  * [**Refactor**] user model to new language syntax

  * [**Reformat**] home page text to use more whitespace

  * [**Rearrange**] buttons so OK is on the lower right

  * [**Redraw**] diagram of how our web app works

  * [**Reword**] home page text to be more welcoming


## Reasoning

We primarily care that our team communicates effectively with our shared understanding. 

We secondarily like these verbs above because they're easy to read, easy to type, and clear in many cultures.

If you and your team prefer other words, that's fine too; use what works for you.


## Reject these formats

We reject git commit message styles that put meta-information into the summary line.

Example:

  * [bug] ...

  * (release) ...

  * \#12345 ...

  * docs: ...

  * JIRA-666 #time 1w 2d 4h 30m #comment Task completed ahead of schedule #resolve

We reject the git commit message style of projects such as Angular, Commitizen defaults, etc.

  * Because these use a leading tag that is sometimes a word, sometimes an abbreviation, sometimes a plural noun, etc. 

  * Examples are using "feat" for feature, "docs" for document, "perf" for performance improvement, etc.

  * Instead we use "Add" for adding a feature, "Document" for documenting help, "Optimize" for performance improvement, etc. 

  * Active verbs are easier to skim, and easier to use for people from other cultures who may be less-comfortable using English.

We reject using a ticket id number in the summary line.

  * Instead, we use fully-qualified URLs in the commit message body.

  * This is because many of our projects use multiple tracking systems, and multiple ways of launching a URL. 

  * We want URL tracking to be easy to use by a wide range of systems, scripts, and teams.

We reject using a time tracking syntax in the summary line.

  * Instead, if you want time tracking, put the info in the commit message body.

  * This is because your personal time tracking is irrelevant to most other developers.

  * If you must use time tracking, we recommend the format of ISO 8601 and UTC, such as "YYYY-MM-DDTHH:MM:SSZ"


## Optional: use contact email addresses

We sometimes have more than one person working on a commit. For example, we do do pair programming.

To keep track of this, we write a git commit message body that lists each person. We use the person's name and the email address. We use one person per line because this is easy to parse.

    Co-authored-by: Alice Adams <alice@eaxmple.com>
    Co-authored-by: Bob Brown <bob@example.com>
    Co-authored-by: Carol Curtis <carol@example.com>

To make this easy, we use a [git commit template].


## Optional: use task tracking links

We sometimes connect a git commit to a task tracking system or web page that explains more. For example, we use GitHub, Trello, Jira, and many other bug tracking systems and project management software systems.

To keep track of these, we use a git commit message body that lists each URL, one per line, because this is easy to parse.

Example:

    Add feature foo

    See: https://github.com/user/repo/issues/789
    See: https://jira.com/tasks/123
    See: https://wikipedia.com/quicksort

If we want to provide link names, then we use Markdown links, such as:

    See: [Request for help with sign in](https://github.com/user/repo/issues/789)
    See: [Add feature foo](https://jira.com/tasks/123)
    See: [Wikipedia Quicksort](https://wikipedia/quicksort)

To make this easy in practice, we use a git template that helps fill in this info.


## Optional: use resource tracking metrics

We sometimes connect a git commit to a resource tracking system or metrics scripts. For example, we work on some projects where the project managers must keep track of work hours spent on a commit, or story point estimates per feature branch, or cost of hiring a developer to fix a bug.

To keep track o these, we use a git commit message body that lists each item, one per line, because this is easy to parse.

Example:

    Add feature foo

    Time: 7 staff hours
    Cost: $700
    Points: 7

