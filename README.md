# create-playdate-release

> A GitHub action that compiles and attaches a Playdate game to a release.

[![License](https://img.shields.io/github/license/idleberg/create-playdate-release?style=for-the-badge)](LICENSE)
[![Version](https://img.shields.io/github/v/release/idleberg/create-playdate-release?style=for-the-badge)](https://github.com/idleberg/create-playdate-release/releases)
[![Build](https://img.shields.io/github/actions/workflow/status/idleberg/create-playdate-release/default.yml?style=for-the-badge)](https://github.com/idleberg/create-playdate-release/actions)

## Usage

Configure a step that adds the `idleberg/create-playdate-release` action to your workflow. Optionally, you can pass arguments to the action.

```yaml
- uses: idleberg/create-playdate-release@v0.2.1
  with: 
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

:bulb: **Note:** For security reasons it's recommended to use the commit hash of the [release](https://github.com/idleberg/create-playdate-release/releases) as version identifier

## All options

### List of input options

Bold arguments are required

| Input              | Description                                       | Default    |
| ------------------ | --------------------------------------------------| ---------- |
| **`github_token`** | Your GitHub token `${{ secrets.GITHUB_TOKEN }}`   | –          |
| `input`            | The source directory of the project               | `"source"` |
| `output`           | The name of the build target directory            | `"build"`  |
| `compress`         | Compress output files                             | `true`     |
| `quiet`            | Quiet mode, suppresses non-error output           | `false`    |
| `strip`            | Strip debug symbols from build                    | `true`     |
| `verbose`          | Enables verbose mode                              | `true`     |
| `include_files`    | List of files to include in the release           | –          |
| `is_draft`         | Mark release is a draft                           | `false`    |
| `is_prerelease`    | Mark release is a pre-release                     | `false`    |
| `dry_run`          | Skips creation of a release                       | `false`    |

## Related

- [setup-playdate-sdk](https://github.com/marketplace/actions/setup-playdate-sdk)

## License

This work is licensed under [The MIT License](LICENSE).
