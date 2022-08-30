# rector-ci

add a comment on pull request when rector request changes

usage: 
```yaml
name: PhpStan CI

on:
  pull_request: null

jobs:
  rector-ci:
    runs-on: ubuntu-latest
    # run only on commits on main repository, not on forks
    if: github.event.pull_request.head.repo.full_name == github.repository
    steps:
      - uses: restarteco/backend-ci/phpstan-ci@v1
```

## TODO

 - improve doc
 - make it more configurable
 - middle finger is to agressive ? replace with unicorn ?