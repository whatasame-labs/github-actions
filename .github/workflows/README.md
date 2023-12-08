# Sample GitHub Actions

The following actions are available:

- [Issue and pull request labeler](./issue-and-pr-labeler.yml)
- [Hello Typescript Action](./hello-ts-action.yml)

## Issue and pull request labeler

This action labels issues and pull requests based on the title prefix. It needs a configuration file in the repository root called `.github/labeler.yml`. 

[Here](../labeler.yml) is an example configuration file and more information on the [labeler-action repository](https://github.com/jimschubert/labeler-action).

## Hello Typescript Action

This action is my first attempt at creating a GitHub Action. It is based on the [Create a GitHub Action Using TypeScript](https://github.com/actions/typescript-action). It just prints "Hello World" or "Hello" + the name of a person to greet to the log.

See more information on the [hello-ts-action repository](https://github.com/whatasame-labs/hello-ts-action)