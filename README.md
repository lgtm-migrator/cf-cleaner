# cf-cleaner

[![GitHub Actions](https://github.com/un-ts/cf-cleaner/workflows/CI/badge.svg)](https://github.com/un-ts/cf-cleaner/actions/workflows/ci.yml)
[![Codecov](https://img.shields.io/codecov/c/github/un-ts/cf-cleaner.svg)](https://codecov.io/gh/un-ts/cf-cleaner)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/un-ts/cf-cleaner.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/un-ts/cf-cleaner/context:javascript)
[![type-coverage](https://img.shields.io/badge/dynamic/json.svg?label=type-coverage&prefix=%E2%89%A5&suffix=%&query=$.typeCoverage.atLeast&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fun-ts%2Fcf-cleaner%2Fmain%2Fpackage.json)](https://github.com/plantain-00/type-coverage)
[![npm](https://img.shields.io/npm/v/cf-cleaner.svg)](https://www.npmjs.com/package/cf-cleaner)
[![GitHub Release](https://img.shields.io/github/release/un-ts/cf-cleaner)](https://github.com/un-ts/cf-cleaner/releases)

[![Conventional Commits](https://img.shields.io/badge/conventional%20commits-1.0.0-yellow.svg)](https://conventionalcommits.org)
[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Code Style: Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![changesets](https://img.shields.io/badge/maintained%20with-changesets-176de3.svg)](https://github.com/atlassian/changesets)

Cleanup Confluence HTML via rehype

## TOC <!-- omit in toc -->

- [Usage](#usage)
  - [Install](#install)
  - [CLI](#cli)
  - [API](#api)
- [Changelog](#changelog)
- [License](#license)

## Usage

### Install

```sh
# npm
npm i -g cf-cleaner

# pnpm
pnpm i -g cf-cleaner

# yarn
yarn global add cf-cleaner
```

### CLI

```plain
Usage: cfc [options] [input]

Arguments:
  input                   Input HTML codes

Options:
  -V, --version           output the version number
  -i, --input <path>      Input HTML file
  -o, --output <path>     Output HTML file
  -m, --minify [boolean]  Whether to minify HTML output
  -h, --help              display help for command
```

### API

```js
import fs from 'fs'
import { cleaner } from 'cf-cleaner'

// string
const output = cleaner(html, minify, encoding)

// stream
cleaner(fs.createReadStream(htmlFile), minify).pipe(
  fs.createWriteStream(outputFile),
)
```

## Changelog

Detailed changes for each release are documented in [CHANGELOG.md](./CHANGELOG.md).

## License

[MIT][] © [JounQin][]@[1stG.me][]

[1stg.me]: https://www.1stg.me
[jounqin]: https://GitHub.com/JounQin
[mit]: http://opensource.org/licenses/MIT
