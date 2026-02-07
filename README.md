# KSE Labs Trusted Workflows

Centralized repository for reusable GitHub Actions workflows.

## Available Workflows

### Go Build and Docker (`go-build.yaml`)

Builds and tests Go applications, optionally building a Docker image.

**Usage:**

```yaml
jobs:
  build:
    uses: TorinKS/kse-labs-trusted-workflows/.github/workflows/go-build.yaml@main
    with:
      go-version: '1.21'
      working-directory: path/to/go/code
      image-name: my-app
```

**Inputs:**

| Input | Required | Default | Description |
|-------|----------|---------|-------------|
| `go-version` | No | `1.21` | Go version to use |
| `working-directory` | Yes | - | Directory containing Go code |
| `docker-context` | No | same as working-directory | Docker build context path |
| `image-name` | No | `app` | Docker image name |
| `build-docker` | No | `true` | Whether to build Docker image |

## Security

This repository should be protected with branch protection rules. Only trusted maintainers should have write access.
