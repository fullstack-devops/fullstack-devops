# release

## Overview

```bash
awesome-ci release <subcommand> [subcommand-option]
```

### Subcommands

| Subcommand | Description                                                                |
| ---------- | -------------------------------------------------------------------------- |
| `create`   | creates an release, but doesn't publish it                                 |
| `publish`  | publishes an existing release with an given release id or makes an new one |

| Subcommand option | Description                                                                                      |
| ----------------- | ------------------------------------------------------------------------------------------------ |
| `-version`        | overrides any version from git and, or patches the given string                                  |
| `-patchLevel`     | overrides the patchLevel. make shure your following the alias definition.                        |
| `-dry-run`        | doesn't create a release. Prints out what it would do and check permissions                      |
| `-body`           | add a text (markdown) to the release body eg.: `./release-template-md`                           |
| `-merge-sha`      | specify the merge sha                                                                            |
| `-release-branch` | set release branch (default: git default)                                                        |
| `-assets`         | (only available in publish) uploads the given Artifacts to a release. Eg.: `file=out/awesome-ci` |
| `-releaseid`      | (only available in publish) publishes an early defined release                                   |

#### -version and -patchLevel

The `-version` option can overwrite the evaluated version.
This can be useful in connection with `-patchLevel` when creating a manual release.

```bash
awesome-ci createRelease -version 0.1.0
```

#### -assets

The `-assets` option can updload a single or multiple artifacts.

However, you must choose the format of the artefacts.

eg.: `-assets "file=path/to/file,file=path/to/second/file"`

#### -body

Send a custom release description. the input can be either a string or a path to a file.

![Release Body with Asstes](../pictures/release-assets-readme.png "Release Body with Asstes")

... more documentation to be done ;)
