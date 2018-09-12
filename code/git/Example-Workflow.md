# Example Workflow

Here's an example workflow given a long-running feature branch `csv-uploader`.

First, an overview:
1. Cut a new branch from an up-to-date feature branch
2. Write some code
3. Commit with a small message
4. Repeat steps 2 & 3 as necessary
5. Acceptance testing
6. Squash commits and create descriptive message
7. Create GitHub PR
8. Add commits to address PR review
9. Squash again when PR is ready to be merged

# Cutting a new branch (step 1)

This is a typical workflow for starting a new branch for work on a specific
ticket:

```
# can't hurt to see where we're starting from...
$ git status
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

# switch to the feature branch, to which other devs have been merging
$ git checkout csv-uploader
Switched to branch 'csv-uploader'
Your branch is up-to-date with 'origin/csv-uploader'.

# run this before cutting a new branch to ensure you've got the latest code
$ git pull
Already up-to-date.

# name your branch descriptively including your initials and the ticket number
#along with some words describing the work that is to be done here
$ git checkout -b tp-burninate-0123456789
Switched to a new branch 'tp-burninate-0123456789'
```

# Make small and regular commits (steps 2-4)

You've got this ticket and you have a bunch of different things that need to
happen to finish the feature, so why not commit as you go along? During
development, making small, atomic commits helps you keep track of what you've
done as the changeset grows and makes it easy to roll back to previous changes
if you find your direction changing.

It helps maybe to decide on a strategy for breaking up the work ahead of time.
I like to use ticket acceptance criteria as a guide, but here's an example of
how I might split out this feature:
- Create `Peasant` model
- Create `Cottage` model
- Add `#burninate` to both `Peasant` & `Cottage`

For example:

```
# make some code changes ...
  <typing sounds>
# then add...
$ git add -p
# and commit...
$ git commit -m 'add Peasant model'

# make some code changes ...
  <typing sounds>
# then add...
$ git add -p
# and commit...
$ git commit -m 'add Cottage model'

# make some code changes ...
  <typing sounds>
# then add...
$ git add -p
# and commit...
$ git commit -m 'add Burnable module and include in Peasant & Cottage'

# make some code changes ...
  <typing sounds>
# then add...
$ git add -p
# and commit...
$ git commit -m 'set up burninate ui'
```

NOTE: The workflow above uses `git add -p` (short for `--patch`). This gives you
an interactive way of looking at the code you're about to stage for committing.
I find that this is a good place to start because it forces you to be more aware
of what it is you are committing at any time. It is also a useful tool when you
have a lot of code written, but you don't want to commit it all at once.  This
article talks about `git add -p` and how to use it both from the command line and
from within VSCode: http://codefoster.com/addpatch/

# Acceptance testing (step 5)
This happens outside of git workflow so we won't get into the details here, but
you may have to go back and commit more code before moving on.

# Squashing time! (step 6)
Now that the code's been tested and accepted we can get our branch ready for
merging! There are a few ways to do this, including the `git squash` command,
but here we'll describe using `git rebase -i` (for `--interactive`). This
allows you to review the commits to be squashed before executing a destructive
operation on the branch (trust us, this will save you more work than you think).

```
```


# Create the PR (step 7)
You know how to do this already, but the neat thing here is that since we
squashed down to only one commit, our PR title and description are automatically
filled in with the subject & message of our commit. It's like magic!

# Addressing PR feedback (steps 8-9)

