![Logo of the project](./.assets/media/img/logo.sample.png)

# `archetype-party`

[![Swagger Validity][swagger-validity-image]][swagger-validity-url]
[![Build Status][travis-image]][travis-url] [![Sonar coverage][sonar-coverage-img]][sonar-coverage-url] [![Quality Gate][sonar-gate-img]][sonar-gate-url] [![Complexity][sonar-complexity-img]][sonar-complexity-url] <br>[![NSP Status][nsp-img]][nsp-url] [![Dependency Status][daviddm-image]][daviddm-url] [![devDependencies Status][daviddm-dev-image]][daviddm-dev-url]<br>[![NPM version][npm-image]][npm-url] [![Readme Score][readme-score-img]][readme-score-url] [![PRs Welcome][makeapullrequest-image]][makeapullrequest-url] [![FOSSA Status][fossa-image]][fossa-url]  [![Coverage percentage][coveralls-image]][coveralls-url]

> The Party archetype represents an identifiable, addressable entity that may have legal status and normally has autonomous control over (at least some of) its actions.

## Table of contents

<!-- toc -->

- [Installation](#installation)
- [Usage](#usage)
- [Quality gates, reports, and documentation](#quality-gates-reports-and-documentation)
  * [Swagger validation and badge](#swagger-validation-and-badge)
  * [Javascript callout source code analysis](#javascript-callout-source-code-analysis)
  * [Javascript callout test execution and code coverage](#javascript-callout-test-execution-and-code-coverage)
  * [API documentation and complexity reports](#api-documentation-and-complexity-reports)
- [Semantic version and CHANGELOG](#semantic-version-and-changelog)
- [Contributing to `archetype-party`](#contributing-to-archetype-party)
- [License](#license)

<!-- tocstop -->

## Installation

Open a Terminal and run this command:

```sh
$ npm install --save archetype-party
```

If your team prefers Yarn:

```sh
$ yarn add archetype-party
```

## Usage

```js
const { Party } = require('archetype-party')

let p = new Party()
```

## Quality gates, reports, and documentation

This repository demonstrates best practices for an API Proxy that uses custom Javascript API policies to adapt a "flat", proprietary contact info service into the expected Cordova Contacts API.

Therefore, we need to enforce Swagger quality; Javascript quality; and Javascript unit tests and code coverage.

### Swagger validation and badge
> :trophy: `archetype-party` validates Swagger docs with [`swagger-cli`][swagger-cli-url].

[`swagger-cli`][swagger-cli-url] validation runs before every test execution:

```bash
# These two npm-scripts run lint automatically:
$ npm run pretest

$ npm test

# Lint Javascript callouts and Swagger *.yml or *.json docs:
$ npm run lint

# You can also validate your Swagger docs independently with:
$ npm run swagger:lint

```

[`swagger-api/validator-badge`](https://github.com/swagger-api/validator-badge)s display whether there are syntactic issues with you Swagger/OpenAPI 2.0 document.

### Linting
> :closed_lock_with_key: :bath: :ocean: `archetype-party` lints source code; checks for vulnerabilities; assesses dependency drift; and executes quality gates with `BitHound`, `eslint`, `nsp`, and `SonarQube`/`sonarcloud`.
>
> The results are displayed real-time with README badges.

```bash
# Code quality analysis runs before every test execution:
$ npm test

# Validate Swagger and analyze Javascript callouts:
$ npm run lint

# Only run ESLint for a CLI summary:
$ npm run eslint:stylish

# Generate an HTML report with links to errors and warnings:
$ npm run eslint:html
```

### Test execution and code coverage
> :100: `archetype-party` uses `jest` for BDD spec execution and code coverage analysis.
>
> The results are displayed real-time with README badges.

Generate detailed code coverage reports at `coverage/lcov-report/index.html` and `lcov.info` and `clover.xml` files  (which you can send to CI test coverage services like  Coveralls and  [OneSonarQube][one-sonar-url] or [SonarCloud][sonarcloud-url]):

```bash

$ npm test

```

### API documentation and complexity reports
> :page_facing_up: `archetype-party` automatically generates API docs with
> * [`jsdoc-to-markdown`][jsdoc2md-url],
> * [`complexity-report`][complexity-report-url]s, and Git-friendly
> * [`swagger-markdown`][swagger-markdown-url]
>
> You can view the [complexity report][complexity-report-url],
> [Javascript callout API docs][js-callout-docs-url], and
> [Swagger API docs][swagger-api-docs-url] in the `docs/` directory.

To generate API docs, Swagger docs, and Complexity reports in the `lib` directory, run:

```bash
# Generate all docs
$ npm run docs

# Only create static Swagger API docs:
$ npm run docs:swagger

# Only generate Javascript callout API docs:
$ npm run docs:api

# Only generate complexity reports:
$ npm run docs:complexity
```

## Semantic version and CHANGELOG

The latest version of `archetype-party` is `vtrue`. View the [CHANGELOG][changelog-url] for details.

## Contributing to `archetype-party`

![Alt text](https://camo.githubusercontent.com/f96261621753dacf526590825b84f87ccb1db0e6/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f5052732d77656c636f6d652d627269676874677265656e2e7376673f7374796c653d666c6174 "Pull Request") We welcome contributors and pull requests. Check out the guidelines for [contributing to `archetype-party`][contributing-url] and our [Contributor Covenant Code of Conduct][code-of-conduct-url].

Contributions are stories with a beginning, a middle, and an end, all told through issues, comments, and pull requests.

 * [Peruse open issues][issues-url] or
 * [Open a new pull request (PR)][pr-url]

## License

Apache-2.0 © [Greg Swindle](https://githbub.com/gregswindle)


[changelog-url]: ./CHANGELOG.md
[code-of-conduct-url]: ./CODE_OF_CONDUCT.md
[complexity-report-url]: ./docs/COMPLEXITY.md
[contributing-url]: ./CONTRIBUTING.md
[daviddm-image]: https://david-dm.org//archetype-party.svg?theme=shields.io
[daviddm-url]: https://david-dm.org//archetype-party
[js-callout-docs-url]: ./docs/JSCAPIS.md
[jsdoc-url]: http://usejsdoc.org/
[jsdoc2md-url]: https://github.com/jsdoc2md/jsdoc-to-markdown
[npm-image]: https://badge.fury.io/js/archetype-party.svg
[npm-url]: https://npmjs.org/package/archetype-party
[nsp-image]: https://nodesecurity.io/orgs//projects/REPLACE-THIS-WITH-YOUR-NSP-UUID/badge
[nsp-sign-up-url]: https://nodesecurity.io/signup
[nsp-url]: https://nodesecurity.io/orgs//projects/REPLACE-THIS-WITH-YOUR-NSP-UUID
[one-sonar-url]: http://onesonar.verizon.com/
[sonarcloud-url]: https://sonarcloud.io
[swagger-api-docs-url]: ./docs/SWAGGER.md
[swagger-cli-url]: https://github.com/BigstickCarpet/swagger-cli
[swagger-io-url]: http://swagger.io
[swagger-logo-20-image]: .assets/media/img/swagger-logo-20.png
[swagger-markdown-url]: https://github.com/syroegkin/swagger-markdown
[swagger-validity-image]: https://img.shields.io/swagger/valid/2.0/PROTOCOL/HOSTNAME/PATHNAME/openapi.json.svg
[swagger-validity-url]: http://online.swagger.io/validator/debug?url=http://HOSTNAME/PATHNAME/openapi.json
[travis-image]: https://travis-ci.org//archetype-party.svg?branch=master
[travis-url]: https://travis-ci.org//archetype-party
[coveralls-image]: https://coveralls.io/repos//archetype-party/badge.svg
[coveralls-url]: https://coveralls.io/r//archetype-party
