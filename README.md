# addresscloud-github-actions

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

Reusable workflows for github actions.

## Table of Contents

- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contributing](#contributing)
- [License](#license)

## Usage

In another repository, add a reference to a workflow in this repository in a job. E.g. to use the terraform apply workflow, add:

```
jobs:
  terraform:
    uses: addresscloud/addresscloud-github-actions/.github/workflows/terraform.yml@main
    secrets: 
      terraform-token: <terraform-token>
    with:
      environment: dev
      terraform-action: apply
      terraform-version: 1.2.4
      working-directory: terraform
      build-artifact-name: build-output
      build-artifact-path: dist/
```

## Maintainers

[@mikeaddresscloud](https://github.com/mikeaddresscloud)

## Contributing

Pull requests are not accepted in this project.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

MIT © 2022 addresscloud
