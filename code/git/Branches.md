[Main](../../README.md) >
[Technical Guidelines and Style](../README.md) >
[Git](./README.md)

# Branches

- Never delete a remote branch with unmerged commits without asking the author
  first.
- Never merge a pull request when the branch being merged to is red on Solano
  UNLESS the purpose of the pull request is to fix the test.
- Don't force push to a shared branch without approval from all involved.
- Prefix all your branch names with your initials or username. This helps
  prevent name collisions.
- Avoid using slashes (/) in branch names. Git handles these in a weird way and
  it can cause unexpected name collisions.
- Remove branches that have been merged or not necessary for reference from
  GitHub.
- If your branch has a merge conflict with master, prefer rebasing on master to
  merging, with the following caveats (in either case see
  [Merging](./Merging.md)):
  - You must merge if the branch is a shared feature branch.
  - If there are complex conflicts to be resolved, merging may make it clearer
    to resolve these.
- When a team is using a feature branch to collaborate on larger pieces of work,
  the feature branch must be protected.
    - Branch protection settings are addressed [in the
      wiki](https://github.com/coverhound/wiki/blob/master/ci/feature-branches.md).
