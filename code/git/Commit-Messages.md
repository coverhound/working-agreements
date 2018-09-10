# Commit Messages

Good commit messages provide invaluable context when one is attempting to
understand the thought process leading to decisions that they may not, at this
moment understand, i.e. when debugging a hard to trace error in code written
months or even years ago. To this end, we follow the [Seven Rules of a Good
Commit Message](https://chris.beams.io/posts/git-commit/).

1. Separate subject from body with a blank line
1. Limit the subject line to 50 characters
1. Capitalize the subject line
1. Do not end the subject line with a period
1. Use the imperative mood in the subject line
1. Wrap the body at 72 characters
1. Use the body to explain what and why vs. how

For an example of what that would look like, we have copied the example commit
from the link.

```
Summarize changes in around 50 characters or less

More detailed explanatory text, if necessary. Wrap it to about 72
characters or so. In some contexts, the first line is treated as the
subject of the commit and the rest of the text as the body. The
blank line separating the summary from the body is critical (unless
you omit the body entirely); various tools like `log`, `shortlog`
and `rebase` can get confused if you run the two together.

Explain the problem that this commit is solving. Focus on why you
are making this change as opposed to how (the code explains that).
Are there side effects or other unintuitive consequences of this
change? Here's the place to explain them.

Further paragraphs come after blank lines.

 - Bullet points are okay, too

 - Typically a hyphen or asterisk is used for the bullet, preceded
   by a single space, with blank lines in between, but conventions
   vary here

If there is a Pivotal ticket for this change, reference it like this:

[#123456789]
OR
[Delivers #123456789]
OR
[Finishes #123456789]
```

The link goes over every item in detail, in addition to providing more articles
for further context and explanation.
