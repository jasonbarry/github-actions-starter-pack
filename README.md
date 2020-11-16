# GitHub Actions Starter Pack

✨ Example repo containing 5 GitHub Actions workflows! ✨

[GitHub Actions](https://docs.github.com/en/free-pro-team@latest/actions/quickstart) is the easiest way to set up a Continuous Integration pipeline for your GitHub repos. You get 2,000 minutes for free every month, so might as well use them! 

With this starter pack, you'll learn how to: 

- Run concurrent jobs within a workflow
- Lint and unit test pull requests via Continuous Integration
- Enable deployment previews on pull requests via [FeaturePeek](https://featurepeek.com)
- Make a bot apply labels on pull requests based on branch name
- Publish to npm and GitHub Container Registry when changes get merged to the main branch

**The best way to try these out on your own is to fork this repo!** You'll see the actions run every time you push a branch or open a pull request.


## Workflows

Every *action* lives inside a *workflow*. You'll find all the workflows for a given repo inside the [./github/workflows/](https://github.com/jasonbarry/github-actions-starter-pack/tree/master/.github/workflows) directory. Workflows are always represented by YAML files. 

You can name your workflow YAML files anything you want. It's generally a good idea to have multiple workflows that do one specific task than one large workflow that does multiple tasks. 

Check out the [workflows that exist in this repo](https://github.com/jasonbarry/github-actions-starter-pack/tree/master/.github/workflows), as well as the [checks on pull requests](https://github.com/jasonbarry/github-actions-starter-pack/pulls?q=is%3Apr+is%3Aclosed) to see the build logs of each action. 

## Secrets and environment variables

Some workflows reference secrets and environment variables that are required to be set. This is so that you don't need to hardcode sensitive keys and tokens into your code. In the workflows in this repo, I have the `NPM_TOKEN` and `CR_PAT` secrets set. You can encrypt a new secret in the Secrets section of your repo settings page.

These values are only available at *build-time*, not *run-time*. They're only available during the context of the Continuous Integration pipeline, so they won't show up anywhere in your built frontend assets that you deploy. 

Other environment variables like `$GITHUB_REPOSITORY` and `$GITHUB_TOKEN` are supplied by GitHub and available automatically.

## Repo info

This repo was bootstrapped from [create-next-app](https://nextjs.org/docs/api-reference/create-next-app) using the [with-typescript-eslint-jest](https://github.com/vercel/next.js/tree/canary/examples/with-typescript-eslint-jest) template. It's configured with the following tools: 

- [Typescript](https://www.typescriptlang.org/)
- Linting with [ESLint](https://eslint.org/)
- Formatting with [Prettier](https://prettier.io/)
- Linting, typechecking and formatting on by default using [`husky`](https://github.com/typicode/husky) for commit hooks
- Testing with [Jest](https://jestjs.io/) and [`react-testing-library`](https://testing-library.com/docs/react-testing-library/intro)


For learning how to use GitHub Actions, you can ignore most of the files in this repo -- they're there so a dummy frontend can build. All the interesting stuff is happening in the [.github/workflows](https://github.com/jasonbarry/github-actions-starter-pack/tree/master/.github/workflows) directory.


## Useful resources

- [Workflow syntax for GitHub Actions ](https://docs.github.com/en/free-pro-team@latest/actions/reference/workflow-syntax-for-github-actions)
- [GitHub Actions Marketplace](https://github.com/marketplace?type=actions&query=)
- [Where to Create a GitHub Personal Access Token](https://github.com/settings/tokens)
