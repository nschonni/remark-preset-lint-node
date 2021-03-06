# remark-preset-lint-node

[![Build Status](https://github.com/nodejs/remark-preset-lint-node/workflows/Tests/badge.svg)](https://github.com/nodejs/remark-preset-lint-node/actions?workflow=Tests)

remark preset to configure remark-lint with settings for nodejs/node

## Install

```console
npm install remark-preset-lint-node
```

## Test

```console
npm test
```

## Add new language or grammar

### Adding the language to the documentation style guide

1. PR the [nodejs/node](https://github.com/nodejs/node) repo adding the language/grammar to the [documentation style guide](https://github.com/nodejs/node/blob/master/doc/guides/doc-style-guide.md)

### Adding the language to the linter

1. PR this repo adding the language/grammar
1. Bump this package version, publish it
1. In [node-lint-md-cli-rollup](https://github.com/nodejs/node/tree/master/tools/node-lint-md-cli-rollup), bump the `remark-preset-lint-node` dependency 
1. In the `nodejs/node` repo, rebuild the Markdown linter (`make lint-md-rollup`)
1. PR the `nodejs/node` repo with the updated linter
