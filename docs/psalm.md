# Using [Psalm](https://github.com/vimeo/psalm)

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
      - 'psalm.xml'

  push:
    paths-ignore:
      - 'docs/**'
      - 'README.md'
      - 'CHANGELOG.md'
      - '.gitignore'
      - '.gitattributes'
      - 'infection.json.dist'
      - 'psalm.xml'

name: static analysis

jobs:
  psalm:
    uses: reagordi/actions/.github/workflows/psalm.yml@master
    with:
      os: >-
        ['ubuntu-latest']
      php: >-
        ['8.2']
```
