# Using [Composer require checker](https://github.com/maglnet/ComposerRequireChecker)

```yml
on:
  pull_request:
    paths-ignore:
      - 'docs/**'
      - 'README.md'
      - 'CHANGELOG.md'
      - '.gitignore'
      - '.gitattributes'
      - 'infection.json.dist'
      - 'phpunit.xml.dist'

  push:
    paths-ignore:
      - 'docs/**'
      - 'README.md'
      - 'CHANGELOG.md'
      - '.gitignore'
      - '.gitattributes'
      - 'infection.json.dist'
      - 'phpunit.xml.dist'

name: composer require checker

jobs:
  composer-require-checker:
    uses: reagordi/actions/.github/workflows/composer-require-checker.yml@master
    with:
      os: >-
        ['ubuntu-latest']
      php: >-
        ['8.2']
```
