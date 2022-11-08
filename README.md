# Sparse checkout

Sparse checkout a git repository like [actions/checkout](https://github.com/actions/checkout).

## Usage

```yml
name: 'Checkout mono repository'
on:
  push:

jobs:
  checkout:
    runs-on: ubuntu-20.04
    steps:
      - uses: snow-actions/sparse-checkout@v1.2.0
        with:
          patterns: |
            .github
```

## Inputs

See [action.yml](action.yml).

|name|required|description|default value|
|---|---|---|---|
|patterns|required|Write a set of patterns to the sparse-checkout file.|-|
|repository|optional|Same as actions/checkout|`${{ github.repository }}`|
|ref|optional|Same as actions/checkout|`''`|
|token|optional|Same as actions/checkout|`${{ github.token }}`|
|path|optional|Same as actions/checkout|`'.'`|
|filter|optional|filter-spec to omit objects/blobs when fetching |`''`|

## Supported

### Events

- Any

### Runners

[![Test](https://github.com/snow-actions/sparse-checkout/actions/workflows/test.yml/badge.svg)](https://github.com/snow-actions/sparse-checkout/actions/workflows/test.yml)

* `ubuntu-*`
* `windows-*`
* `macos-*`
