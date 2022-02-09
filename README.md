# rector-commit-comment

add a comment on pull request when rector request changes

usage: 
```yaml
name: Rector CI

on:
  pull_request: null

jobs:
  rector-ci:
    runs-on: ubuntu-latest
    # run only on commits on main repository, not on forks
    if: github.event.pull_request.head.repo.full_name == github.repository
    steps:
      - uses: restarteco/rector-commit-comment@v1.2
        with:
          # Must be used to trigger workflow after push
          token: ${{ secrets.ACCESS_TOKEN_RECTOR }}
          auth_json: ${{ secrets.ACCESS_AUTH }}
```