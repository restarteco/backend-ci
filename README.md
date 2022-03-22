# backend-ci

Repo containing every backend CI gh-actions:
- [rector-ci](./rector-ci)
- [frontend-integrity-ci](./frontend-integrity-ci)

Check them to see how to use.

## Publish an update

After updating code you have to publish it by creating a new release.

Then update every CI uses with latest version.

```yaml
    ...
    - uses: restarteco/backend-ci/frontend-integrity-ci@v2  # replace with v2.1, v3, etc...
    ...

```
