# simplecov-report-action

[![build](https://github.com/nohmad/simplecov-report-action/actions/workflows/build.yml/badge.svg)](https://github.com/nohmad/simplecov-report-action/actions/workflows/build.yml)

Add summary of coverage report as comment on Pull Request.

## Usage

No need to run if not triggered by pull_request

```yaml
    - name: Coverage Report on Pull Request
      uses: nohmad/simplecov-report-action@master
      with:
        github-token: ${{ secrets.GITHUB_TOKEN }}
        simplecov-json-path: coverage/coverage.json
        ignore-error: true
      if: github.event_name == 'pull_request'
```
