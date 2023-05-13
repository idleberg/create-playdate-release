# create-playdate-release

> A GitHub action that compiles and attaches a Playdate game to a release.

[![License](https://flat.badgen.net/github/license/idleberg/create-playdate-release)](LICENSE)
[![Version](https://flat.badgen.net/github/release/idleberg/create-playdate-release)](https://github.com/idleberg/create-playdate-release/releases)
[![Status](https://flat.badgen.net/github/checks/idleberg/create-playdate-release/?label=build)](https://github.com/idleberg/create-playdate-release/actions)

## Usage

Configure a step that adds the `idleberg/create-playdate-release` action to your workflow. Optionally, you can pass arguments to the action.

```yaml
- uses: idleberg/create-playdate-release@v0.1.2
  with: 
    github_token: ${{ secrets.GITHUB_TOKEN }}
```

## All options

### List of input options

Bold arguments are required

| Input              | Description                                       | Default  |
| ------------------ | --------------------------------------------------| -------- |
| **`github_token`** | Your GitHub token (`${{ secrets.GITHUB_TOKEN }}`) | –        |
| `input`            | The source directory of the project               | `source` |
| `output`           | The name of the build target directory            | `build`  |
| `include_files`    | List of files to include in the release           | –        |
| `is_draft`         | Mark release is a draft                           | `false`  |
| `is_prerelease`    | Mark release is a pre-release                     | `false`  |
| `dry_run`          | Skips creation of a release                       | `false` |

## Related

- [setup-playdate-sdk](https://github.com/marketplace/actions/setup-playdate-sdk)

## License

This work is licensed under [The MIT License](LICENSE).
