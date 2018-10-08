[Main](../../README.md) >
[Process](../README.md) >

# Code Review

This section is about reviewing code that has been committed and pushed to
GitHub. For general Git guidelines and practices, see
[Git](../../code/git/README.md)

### General

- All pull requests must satisfy the following requirements:
    - An approved review
    - Passing on Solano
    - Passing on Code Climate
- If the author feels either of the automated analysis failures are
  illegitimate, they should highlight that in a comment on the pull request.
    - Code Climate infractions can be ignored individually or the level of the
      entire pull request.
    - A failing build on Solano will require administrator override to merge.
      All Tech Leads are GitHub admins and will have the power to do so.
- Don't merge someone else's pull request without their approval.
- Keep additional commits for addressing code review separate for ease of review.
    - These should be squashed after PR approval.
- pull requests should include tests if possible, but whether to practice strict
  TDD (whether to write the tests before or after the code) is up to the author.
- If your pull request is waiting on something other than code review, close it
  and reopen it when it's ready for code review or to be merged.
    - Avoid leaving pull requests open and inactive for more than 2 business days.
    - Use labels such as "pending product approval" and "pending settings" to
      indicate what is needed before merging is acceptable.
- Code review is a tremendous learning opportunity. If someone shows you
  something new, call it out and thank them!
- Similarly, if there is something in the code that is especially well done or
  will improve things for the rest of the team, point it out to the author.
- When commenting on a pull request, distinguish between blocking and
  non-blocking comments if it's unclear.

### The Review

Code review is not to make sure something works; it is to make sure it is
workable going forward. Acceptance testing should have been handled previously.
It is, however, reasonable and expected that the reviewer will make sure the
author has automated tests covering the functionality added, and that they have
verified that the feature works.

As a reviewer, begin from the standpoint that the code in front of you works.
If something about the author's design, implementation, or style confuses you,
ask them questions that will help remove that confusion.

Don't +1 something that you don't understand. Code review is the one time that
someone will be reading this code before it is committed. It is a special time
because it will be fresh in the author's head, and thus are very well-suited to
field questions from the reviewer. Code review is a partnership between author
and reviewer to make sure that going forward, this code is clear and usable for
the next time someone has to touch it when the details have become fuzzy from
the fog of time.

As a reviewer, if you have worries about the code in its current state, seek to
back those up with something other than your gut feeling. Use documentation,
sample code, writing from members of the community, etc. to back up what you're
saying.

Discussions of the style guide are to be limited to the style guide. Code review
is not an opportunity for reviewers to enforce personal feelings of theirs not
covered in the style guide.

### Assigning Reviewers

- Use Github's "Assign Reviewer" feature to call out specific engineers who
  would be most helpful in reviewing a given pull request
- If you need someone to review a pull request, try to ask someone on your team before
  going to others.

### Adding Dependencies

When adding dependencies, please follow the guidelines in [Adding
Dependencies](./Adding-Dependencies.md).
