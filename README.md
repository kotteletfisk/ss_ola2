# ss_ola2

### Branching Strategy

Our first idea was to select GitFlow, as we are already familiar with this framework, however it does have its drawbacks. It wont work out of the box without doing a lot of setup. Our project group also requires a strategy that allows us to push daily commits, which is slower with Gitflow due to its multi-step process with actual releases.
We decided to go with Trunk Based Development. The teams work will be done in short-lived branches, which then are frequently merged to the trunk.
We talked about maybe implementing a development branch later on, but for now will stay with a "true" Trunk Based Development strategy.

### Using Dev Containers

The dev container specifies a common environment for development and testing. This includes stuff like OS, Java environment, Build manager (Maven) and version control. It excludes stuff like IDE and personal dev preferences.

We use a simple container running a Debian Linux distribution with Java 21, Maven and Git.

To run the devcontainer, we need middlware to parse the configuration (devcontainer.json), build a docker image, and run it as our env.

**VSCode**

- Install ´Dev Containers´ plugin

- Use command palette -> Build Dev Container.

- SSH credentials gets injected into the container, so we can push commits normally.
    - On Linux, this works with `ssh-agent`. If we run into problems with invalid SSH keys, we might have to add out local keys to the agent by runnin `ssh-add` (Adds keys from default .ssh directory)

**IntelliJ**

- Use `Dev Containers` from welcome screen (requires Ultimate)

- Install `Docker` and `Dev Containers` plugin from marketplace if using community edition

- Press `Create dev container and mount resources`


### Issue metrics

We use a github workflow bot to keep track of issue metrics. 

Every weekday at 7, it runs an [Issue Metrics Action](https://github.com/marketplace/actions/issue-metrics) for the last 7 days. This measures how much time it takes us to respond to new issues, and how much time passes from open to close. Both in average time, and for specific issues.

It creates a daily report as an issue we can use to better understand our workflow. 