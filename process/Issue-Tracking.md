[Main](../README.md) >
[Process](./README.md)

# Issue Tracking

## The Cycle

- At the beginning of each cycle, each person on a team should feel like they
  know what the stories and priorities are for the cycle.
- Product team should not add new stories mid-cycle (except bugs caused by
  current stories) above/before stories already planned for the cycle, unless
  it's an emergency.

## Pivotal

- Each team (personal lines, commercial, cyberpolicy) determines for themselves
  how they will use Pivotal features such as stories, points, backlog, epics,
  etc.
- Developers should keep Pivotal up to date so it's clear what everyone is
  working on and which stories are available for someone to pick up.
- Likewise, product should keep Pivotal up to date if something has been added
  to the story.

## Stories / Issues / Bugs

- Whenever possible, story acceptance should happen on a demo environment and
  before release to production.
- Software developers should expect their responsibility to be writing software;
  product people should expect their responsibility to be designing product and
  making sure it follows the vision they have. If, at any point, either party
  feels like their job is veering to the other side, product and engineering
  should talk and find out what is unclear/unusable about the current state.
- A story should have as much context as reasonable.
- If a developer picks up a story and their response is "this doesn't make
  sense," the next action is not for them to seek to understand it, but rather
  to talk to the story owner. The story owner should clarify the requirements
  in the story.
- All efforts should be made to reproduce a bug before making a report. _With
  some exceptions,_ a bug report is not valid and workable without steps to
  reproduce.
- A story is not valid and workable without acceptance criteria.
- If a spec completely changes from the original direction of the story after
  development has already begun/completed, a separate ticket should be created
  with the new requirements.
- After picking up a story, a developer should add a comment referencing the
  branch they will be using to track their changes.
  - This should be added in the "code" section of the Pivotal ticket, which will
    enforce proper GitHub branch link structure.
  - Developers should push any local changes to origin at the end of each
    working day.
  - Commits and commit messages are not expected to be clean and tidy. Push up
    work in progress as is.
  - Other developers will not push on this branch without approval of the
    original developer. If you need to pick up the work, clone the branch to one
    you control and tag it in the ticket.
  - *NB*: This is to guard against worst case scenarios of work being lost or
    held up in case a developer is unable to work for health or any other
    reason. We want to be able to continue work without having to interrupt our
    teammates as they are handling their personal and medical issues OR spending
    their billions of dollars from winning the lottery! This is not meant to be
    a check on how often and when developers are committing.
