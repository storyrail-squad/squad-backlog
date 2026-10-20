# Squad backlog

The squad's user stories and bugs, and nothing else. Code lives in the project repos:

| Repo | What | Deployed to |
|---|---|---|
| [library-frontend](https://github.com/storyrail-squad/library-frontend) | React app + UI automation | GitHub Pages (QA) |
| [library-backend](https://github.com/storyrail-squad/library-backend) | Spring Boot API + API automation, **owns the API contract** | Render (QA) |
| [storyrail](https://github.com/storyrail-squad/storyrail) | The agents that build a story, the live dashboard and every run's reports | — |

## Writing an issue

- **New issue → User story**: the story, numbered acceptance criteria (`AC1`, `AC2`, …) and which parts change
  (Frontend and/or Backend). One story may touch both projects; StoryRail opens one PR in each.
- **New issue → Bug**: steps to reproduce, expected, actual, where it is, severity.

The analyst writes the issue; StoryRail never writes or changes requirements. When the product owner picks an issue
for a build, they run `/storyrail <number>` (story) or `/storyrail fix <number>` (bug) in the StoryRail workspace.

## Labels

| Label | Meaning |
|---|---|
| `user-story` | A story (set by the template) |
| `bug` | A defect (set by the template) |
| `frontend` / `backend` | Optional: which project the issue touches |
| `backlog` | Not planned for the current build |

An issue is closed by StoryRail at sign-off (story) or by the fix PR in the project repo (bug), with a comment that
links every PR and the run report.
