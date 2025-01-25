# gh start extension

This extension will give you the ability to create a new branch by providing a jira, redmine or github issue id.

Depending on the issue tracker you are using, you will need to setup different env vars for authentication.

## Installation

You can install these plugins following the [official installation instructions](https://cli.github.com/manual/gh_extension_install).

A simple way is:
- clone this repository
- `cd` to the plugin you want to install folder
- run `gh extension install .`

## Configuration

- `MECHA_GH_START_GITHUB_TOKEN`: the token to authenticate with GitHub.
- `MECHA_GH_START_JIRA_BASE_URL`: the base URL of your Jira instance.
- `MECHA_GH_START_JIRA_EMAIL`: the email to authenticate with Jira.
- `MECHA_GH_START_JIRA_TOKEN`: the token to authenticate with Jira.
- `MECHA_GH_START_REDMINE_BASE_URL`: the base URL of your Redmine instance.
- `MECHA_GH_START_REDMINE_TOKEN`: the token to authenticate with Redmine.

## Examples

`gh start github 1234` will create `feature/1234-some-amazing-new-thing`

`gh start github 5678 --use-prefix --type=hotfix` will create `hotfix/gh-5678-nasty-bug`


`gh start redmine 1234` will create `feature/1234-some-amazing-new-thing`

`gh start redmine 5678 --use-prefix --type=hotfix` will create `hotfix/rm-5678-nasty-bug`


`gh start jira ABC-1234` will create `feature/ABC-1234-some-amazing-new-thing`

`gh start jira ABC-5678 --use-prefix --type=hotfix` will create `hotfix/ji-ABC-5678-nasty-bug`
