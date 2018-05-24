# Copy GitHub Labels CLI

CLI tool to copy GitHub labels from one repository to another.

[![Build Status](https://travis-ci.org/jvandemo/copy-github-labels-cli.svg?branch=master)](https://travis-ci.org/jvandemo/copy-github-labels-cli)

![octocat](https://cloud.githubusercontent.com/assets/1859381/5422531/40186cf0-8287-11e4-941c-96cabdb3fb24.jpg)

> If you only want to copy GitHub labels in a script and don't need a CLI, please use [copy-github-labels](https://github.com/jvandemo/copy-github-labels) to avoid unnecessary dependencies.

## Installation

```bash
$ npm install -g copy-github-labels-cli
```

## Usage

```bash
$ copy-github-labels -t <token> <source-repo> <destination-repo>
```

## Example

To copy all labels from `angular/angular` to `jvandemo/test`:

```bash
$ copy-github-labels -t e7ac7612021979b8884f6f11236c65e7723da8c1 angular/angular jvandemo/test
```

> The token above is just an example token, not a real token. You should [generate your own token](https://help.github.com/articles/creating-an-access-token-for-command-line-use/).

The output shows whether or not the copy failed for each label individually:

![copy-github-labels](https://cloud.githubusercontent.com/assets/1859381/10329347/702b3700-6cc0-11e5-9513-de309d44e314.png)

## FAQ

#### Where can I get a token?

Check out the GitHub guide: [Creating an access token for command-line use](https://help.github.com/articles/creating-an-access-token-for-command-line-use/).

#### I'm getting an error "Unknown label: failed (Bad credentials)"

This happens when your token is not valid.

#### I'm getting an error "Unknown label: failed (Validation Failed)"

This happens when GitHub refuses to copy the label because it is already present in the destination repository.

#### I'm getting an error "Unknown label: failed (Not Found)"

This happens when the destination repository cannot be found.

## License

MIT

## Change log

### 1.1.0

- added `-f` force option to overwrite label if exists.
- improve error to show label in error.
- copies description.

### 1.0.0

- Released production version

### 0.2.0

- Added error handling
- Updated documentation

### 0.1.0

- Initial version
