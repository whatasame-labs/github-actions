# Sample GitHub Actions

The following actions are available:

- [Link checker](./link-checker.yml)
- [Issue and pull request labeler](./issue-and-pr-labeler.yml)
- [Hello Typescript Action](./hello-ts-action.yml)

## Link checker

This action checks all links of a markdown and HTML files in the repository. 

Event types:
- `repository_dispatch`: POST request to the repository dispatch endpoint.
- `workflow_dispatch`: Trigger the action manually from the Actions tab.
- `schedule`: Trigger the action on a schedule.

    Cron syntax: `* * * * *` (Timezone is UTC, See more information on [here](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule))
    ```
    ┌───────────── minute (0 - 59)
    │ ┌───────────── hour (0 - 23)
    │ │ ┌───────────── day of the month (1 - 31)
    │ │ │ ┌───────────── month (1 - 12 or JAN-DEC)
    │ │ │ │ ┌───────────── day of the week (0 - 6 or SUN-SAT)
    │ │ │ │ │
    │ │ │ │ │
    │ │ │ │ │
    * * * * *
    ```

Fail argument is optional. If it is set to `true`, the action will fail if there is at least one broken link.

## Issue and pull request labeler

This action labels issues and pull requests based on the title prefix. It needs a configuration file in the repository root called `.github/labeler.yml`. 

[Here](../labeler.yml) is an example configuration file and more information on the [labeler-action repository](https://github.com/jimschubert/labeler-action).

## Hello Typescript Action

This action is my first attempt at creating a GitHub Action. It is based on the [Create a GitHub Action Using TypeScript](https://github.com/actions/typescript-action). It just prints "Hello World" or "Hello" + the name of a person to greet to the log.

See more information on the [hello-ts-action repository](https://github.com/whatasame-labs/hello-ts-action)