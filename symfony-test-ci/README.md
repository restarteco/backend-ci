# symfony-test-ci

use php unit to test symfony application.

usage: 
```yaml
name: CI / Test symfony / php unit

on:
  pull_request: null

jobs:
  symfony-test-ci:
    runs-on: ubuntu-latest
    steps:
      - uses: restarteco/backend-ci/symfony-test-ci@v2
        with:
          es_port: 9209 # default 9209
          database_url: mysql://root:root@127.0.0.1:3306/your_database
```
