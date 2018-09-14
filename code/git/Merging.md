[Main](../../README.md) >
[Technical Guidelines and Style](../README.md) >
[Git](./README.md)

# Merging

If you need to merge `master` into a shared feature branch (sometimes referred
to as "watering" your branch with `master`) then you need to open a pull request
to do that. If there are no conflicts then that pull request can be merged
without difficulty.

## Merge Conflicts

However, if your branch cannot be cleanly merged then we need to resolve merge
conflicts:

1. Cut a new branch from your feature branch with a reasonable name like
   `jq-merge-master-into-our-feature-branch-2018-04-20`.
2. From this feature branch go ahead and `git merge master`.
  - When asked to resolve conflicts, take note of all files with conflicts so
    you know where to look in the next step.
  - Simply add all files containing conflicts and commit to complete the merge.
    - Optional: Some folks may prefer to uncomment the conflicting files in the
      commit message, that's okay, but not required.
3. Fix conflicts in the files you noted and make a single new commit with all
the fixes.
4. Put up a pull request for merging this branch into master and go through the
normal pull request review process.
  - Merge conflict resolution can be tricky; as a reviewer, please be extra
    attentive to these pull requests and take a look the latest commit, which
    will contain the conflict resolutions.

The above is relevant for any merge into a branch you're sharing with another
developer(s) or where there is some reasonable chance that your attempted merge
conflict resolution would break the code. If the merge conflicts are minor *and*
there is no reasonable chance you would incorrectly resolve the merge conflict,
then you may simply resolve the merge conflict on your own. (For example, if the
merge conflict is just a conflict of dates at the top of `db/schema.rb`, then
just choose the more recent date; there is no need for the above process in such
a case.)
