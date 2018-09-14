[Main](../../README.md) >
[Process](../README.md) >
[Code Review](./README.md)

# Adding Dependencies

When adding dependencies, we should consider downstream effects. It should be in
a separate commit, with a message that addresses as much of the below as
possible and be reviewed by **two** reviewers. Ensure that you label the PR
`dependency` to make it easier to find.

## Community Support

- How actively is it being maintained?
- How many open issues are there that went stale?
- How accepted is this project by the community?
  - Do a lot of people use this?
  - Where did you hear about it?

## What are the trade-offs?

- What are the trade-offs we're making by using this dependency vs building this
  ourselves?
- Is there overlap with an existing dependency?
- Is this critical functionality?
- Does introducing this functionality introduce new bugs or deal-breaking
  functionality?

## Is this a development or a production dependency?

Make sure to consider whether this dependency is actually needed in production.
Non-production dependencies have lower risk for maintenance.

## What's our security exposure?

- Does the dependency connect to the internet?
- Does the dependency have any parsing of strings?
- Other considerations
