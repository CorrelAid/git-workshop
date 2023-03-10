# Basis-IT-Training

This is the repository for the basis IT Training. If you're a participant,
go to the [Wiki](https://gitlab.internal.d-fine.dev/trainings/basis-it-training/-/wikis/home).
Contributors should read this readme first.

## How it works

The training materials consists of quite some markdown files that you can find
in this repository. On merge to master, a CI job will deploy them to the wiki.
Before a merge happens, a Linter is executed in the CI. Find details on
this below.

## Definition of Done

- Each section should include:
  - A goal description
  - Explanation of the relevant content
  - Links to further reading
  - Short exercise(s) such that the student can test their understanding and
    receive a review for it.
  - Example solutions in the corresponding git repository

## Contributing

### Approvals

Merge requests should only be merged once they received at least **2** prior
approvals.

### Coding style

A proper coding style is enforced via markdownlint.

To install markdownlint:

```bash
apt install npm
npm install -g markdownlint-cli2 markdownlint-cli2-formatter-junit
```

You can pre check your changes using  
`markdownlint-cli2-config .markdownlint-cli2.yaml "**/*.md"` which will produce an xml file containing the check results.

An overview over possible errors and how to fix them can be found
[here](https://github.com/DavidAnson/markdownlint/blob/main/doc/Rules.md).

Auto-fixing can be attempted by running
`markdownlint-cli2-fix "**/*.md"`.

### Example Solutions

The example solutions need to be updated if exercises change

### You can perform your edits and look at your changes online

Via the GitLab WebIDE (works quite well). It is important though, that you pay
attention to the coding style (see above) when you do so, since you cannot run
markdownlint when doing changes online.
