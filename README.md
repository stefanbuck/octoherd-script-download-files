# octoherd-script-download-files

> An Octoherd script to download files from repositories

[![@latest](https://img.shields.io/npm/v/octoherd-script-download-files.svg)](https://www.npmjs.com/package/octoherd-script-download-files)
[![Build Status](https://github.com/stefanbuck/octoherd-script-download-files/workflows/Test/badge.svg)](https://github.com/stefanbuck/octoherd-script-download-files/actions?query=workflow%3ATest+branch%3Amain)

## Usage

Minimal usage

```js
npx octoherd-script-download-files \
  --source README.md \
  --target ./out
```

Pass all options as CLI flags to avoid user prompts

```js
npx octoherd-script-download-files \
  -T ghp_0123456789abcdefghjklmnopqrstuvwxyzA \
  -R "stefanbuck/*" \
  --ignoreArchived undefined \
  --source README.md \
  --target ./out
```

## Options

| option                                        | type             | description                                                                                                                                                                                                                                 |
| --------------------------------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `--ignore-archived` or `--no-ignore-archived` | boolean          | Ignores archive repositories                                                                                                                                                                                                                |
| `--source`                                    | string           | **Required.** Path to the destination directory                                                                                                                                                                                             |
| `--target`                                    | string           | **Required.** File path to download. Note: Directories are not supported yet                                                                                                                                                                |
| `--octoherd-token`, `-T`                      | string           | A personal access token ([create](https://github.com/settings/tokens/new?scopes=repo)). Script will create one if option is not set                                                                                                         |
| `--octoherd-repos`, `-R`                      | array of strings | One or multiple space-separated repositories in the form of `repo-owner/repo-name`. `repo-owner/*` will find all repositories for one owner. `*` will find all repositories the user has access to. Will prompt for repositories if not set |
| `--octoherd-bypass-confirms`                  | boolean          | Bypass prompts to confirm mutating requests                                                                                                                                                                                                 |

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)

## About Octoherd

[@octoherd](https://github.com/octoherd/) is project to help you keep your GitHub repositories in line.

## License

[ISC](LICENSE.md)
