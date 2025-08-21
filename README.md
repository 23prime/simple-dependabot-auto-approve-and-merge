# Simple Dependabot Auto Approve and Merge Action

A simple GitHub Action that [Dependabot](https://github.com/dependabot) approve and merge the Pull request.

## Usage (Example)

Add the following to your workflow:

```yaml
jobs:
  your-job:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v5

      - name: Auto Approve and Merge
        uses: 23prime/simple-dependabot-auto-approve-and-merge@v1
        with:
          pr-url: ${{ github.event.pull_request.html_url }}
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

### Parameters

| Name           | Required | Default Value | Description      |
|----------------|----------|---------------|------------------|
| `pr-url`       | Required | None          | Pull request URL |
| `github-token` | Required | None          | GitHub token.    |

## For Developers

### Requirements

- [Taskfile](https://taskfile.dev/)
- [mise](https://mise.jdx.dev/)

### Quick Start

1. Set up tools

    ```bash
    task setup
    ```

2. Check

    ```bash
    task check
    ```

### Release

Create and push a release tag.

Example: To release `v1`

```bash
task tag:1
```
