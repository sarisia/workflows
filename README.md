# workflows
Collection of GitHub Actions reusable workflows

## `update-devcontainer`

```yaml
jobs:
  build:
    uses: sarisia/workflows/.github/workflows/update-devcontainer.yml@main
    permissions:
      contents: read
      packages: write
```
