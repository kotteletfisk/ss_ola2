# ss_ola2

### Made By


### About the Project

This project acts as a template for future projects within our group. It sets standardized rules for development and collaboration strategies.
It provides common dev container environments, automated label creation for issues, and Weekly DORA metrics.


### Branching Strategy

Our first idea was to select GitFlow, as we are already familiar with this framework, however it does have its drawbacks. It wont work out of the box without doing a lot of setup. Our project group also requires a strategy that allows us to push daily commits, which is slower with Gitflow due to its multi-step process with actual releases.
We decided to go with Trunk Based Development. The teams work will be done in short-lived branches, which then are frequently merged to the trunk.
We talked about maybe implementing a development branch later on, but for now will stay with a "true" Trunk Based Development strategy.

### Getting started

If you want to use this project as a template for your own work, you can click "Use this template" on GitHub, and create your own reposiotory based on this project.

Are you looking to contribute? Read the guidelines in [CONTRIBUTING.md](CONTRIBUTING.md) first.

### Automation Workflows

The template is meant to encourage CI workflow. We do this by not restricting push access to the mainline branch, and automate updates to issues based on branch creation and merges. This helps us keep overview on the progress of the project, while eliminating much manual work normally required by a kanban board.


### Issue metrics

We use a github workflow bot to keep track of issue metrics. 

Every weekday at 7, it runs an [Issue Metrics Action](https://github.com/marketplace/actions/issue-metrics) for the last 7 days. This measures how much time it takes us to respond to new issues, and how much time passes from open to close. Both in average time, and for specific issues.

It creates a daily report as an issue we can use to better understand our workflow. 

### License

[GNU General Public License](LICENSE)
