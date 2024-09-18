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

## `tailscale-ssh`

```yaml
jobs:
  ssh:
    uses: sarisia/workflows/.github/workflows/tailscale-ssh.yml@main
    with:
      client-id: ${{ secrets.TAILSCALE_CLIENT_ID }}
      client-secret: ${{ secrets.TAILSCALE_CLIENT_SECRET }}
      # optional
      version: '1.72.1'
      tags: 'tag:github-actions,tag:test'
      hostname: 'actions'
```

```
$ ssh -o StrictHostKeyChecking=no runner@actions
```
