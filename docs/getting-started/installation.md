---
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# 📥 Installation

Create a file in your project :

```
touch /.github/workflows/validations.yml
```

Then copy this code part :

```
name: Github actions validations

on:
  push:
    branches:
      - "**"
  pull_request:
    types:
      - opened

jobs:
...
  validation-{target}:
    name: Validation {target}
    uses: alexis-gss/github-workflows/.github/workflows/{validation name in the repo}@master
...
```

Finnally, you can **adapt the jobs section** depending to the technologies used in your project like this :

```
validation-php:
    name: Validation php
    uses: alexis-gss/github-workflows/.github/workflows/validation-php.yml@master
```

You can now use the [Github Workflows](https://github.com/alexis-gss/github-workflows).
