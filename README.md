# pact-create-tag-action

Creates a tag on this version.

## Example
```yaml
# (This just saves defining these multiple times for different pact jobs)
env:
  version: "1.2.3"
  application_name: "my-api-provider"
  pact_broker: ${{ secrets.PACT_BROKER }}

jobs:
  pact-create-tag:
    runs-on: ubuntu-latest
    steps:
      - uses: roycdiscovery/pact-create-tag-action@v1.0
        env:
          tag: prod
```
