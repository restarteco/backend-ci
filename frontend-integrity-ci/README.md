# fontend-integrity-ci

Check frontend integrity using GraphQL typing.

usage: 
```yaml
name: CI / Test frontend integrity

on:
  push:
    branches: [ master ]
  pull_request: null

jobs:
  e2e-ci:
    runs-on: ubuntu-latest
    steps:
      - uses: restarteco/backend-ci/frontend-integrity-ci@v2
        with:
          token: ${{ secrets.ACCESS_TOKEN_RECTOR }}
          auth_json: ${{ secrets.ACCESS_AUTH }}
```
