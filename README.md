# action-pr-title

GitHub action that validates PR titles meets our guidelines.

## Usage

```yaml

name: 'PR Title Check'
on:
  pull_request:
    # check when PR
    # * is created,
    # * title is edited, and
    # * new commits are added (to ensure failing title blocks merging)
    types: [ opened, reopened, edited, synchronize ]

jobs:
  title-check:
    runs-on: ubuntu-latest
    steps:
      - uses: submitty/action-pr-title@master
```
