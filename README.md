# ss_ola2

### Branching Strategy

Our first idea was to select GitFlow, as we are already familiar with this framework, however it does have its drawbacks. It wont work out of the box without doing a lot of setup. Our project group also requires a strategy that allows us to push daily commits, which is slower with Gitflow due to its multi-step process with actual releases.
We decided to go with Trunk Based Development. The teams work will be done in short-lived branches, which then are frequently merged to the trunk.
We talked about maybe implementing a development branch later on, but for now will stay with a "true" Trunk Based Development strategy.

### Commit Message Conventions

- Start of each commit message with a short summary.
- Leave a blank line after the summary.
- Fill the commit body with a more detailed description of changes.
- Use a footer to reference related issues, using keywords and issue numbers. (e.g. "fixes #123", "closes #456", "resolves #789")

#### Example Commit Message

```
Add user authentication feature

Implemented user login and registration functionality using JWT for secure authentication.

fixes #42
```