# Saddle

![Saddle_Logo](Saddle.png)

## Description

Saddle uses [cfn-nag](https://github.com/stelligent/cfn_nag) to validate CloudFormation templates.

## Installation

### Assumptions

Saddle assumes you have the following installed on your machine.:

- [Python](https://github.com/pyenv/pyenv)
- [Ruby](https://rvm.io/)

### Installing Dependencies

Install the ruby dependencies (cfn_nag)

```
$ gem install bundle
$ bundle install
```

## Usage

cfn-checker checks all JSON and YAML files ending with `template.json` or `template.yaml`. Arguments following the `-d` flag should be directories containing the CFN templates.

### Logging

The `-l` flag is for the directory that cfn-checker will log files to. It assumes this directory exists. If no `-l` is given, cfn-checker will dump to `stdout`.

### Sample Usage

- Checking templates in the current directory and logging them to the logs/ directory

```
$ python cfn-checker.py -d . -l logs
```

- Checking the [Unicorn-Pipeline](https://github.com/unicorn-ca/Unicorn-Pipeline) templates and logging them to `stdout`

```
$ python cfn-checker.py -d predeploy child stack
```

## Contribution

Please read our [contribution guidelines](https://github.com/unicorn-ca/Unicorn-docs/blob/master/CONTRIBUTING.md) before creating an issue or pull request!