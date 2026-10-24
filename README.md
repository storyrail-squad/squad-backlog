# Squad backlog

The squad's user stories and bugs, and nothing else. Code lives in the application repos:

| Repo | What | Deployed to |
|---|---|---|
| [library-frontend](https://github.com/storyrail-squad/library-frontend) | React app + UI automation | GitHub Pages (QA) |
| [library-backend](https://github.com/storyrail-squad/library-backend) | Spring Boot API, **owns its API contract** | Render (QA) |
| [library-api-tests](https://github.com/storyrail-squad/library-api-tests) | API acceptance tests of library-backend (Cucumber + Java) | — |
| [storyrail](https://github.com/storyrail-squad/storyrail) | The agents that build a story, the live dashboard and every run's reports | — |

## Writing an issue

- **New issue → User story**: the story, numbered acceptance criteria (`AC1`, `AC2`, …) and the **Applications**: one
  line per application it changes, starting with the repo name, e.g.
  `- library-frontend (catalog app): a Reserve button, calls library-backend`. A story can touch any number of
  applications; StoryRail finds them, builds them at the same time and opens one PR in each, merged providers first.
- **New issue → Bug**: steps to reproduce, expected, actual, the application it is in, severity.

The analyst writes the issue; StoryRail never writes or changes requirements. When the product owner picks an issue
for a build, they run `/storyrail <number>` (story) or `/storyrail fix <number>` (bug) in the StoryRail workspace.

## Labels

| Label | Meaning |
|---|---|
| `user-story` | A story (set by the template) |
| `bug` | A defect (set by the template) |
| `backlog` | Not planned for the current build |

An issue is closed by StoryRail at sign-off (story) or by the fix PR in the application's repo (bug), with a comment that
links every PR and the run report.
