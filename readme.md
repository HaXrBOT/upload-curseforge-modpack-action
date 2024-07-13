# Upload CurseForge Modpack

This action uploads Minecraft modpacks to [CurseForge](https://www.curseforge.com/minecraft/modpacks).

## Useful links

- [Example Usage](https://github.com/henkelmax/delivery-inc/blob/master/.github/workflows/release.yml)

## Inputs

| Name                    | Description                                                   | Required |
| ----------------------- | ------------------------------------------------------------- | -------- |
| `api-token`           | The CurseForge API token                                      | Yes      |
| `project-id`          | The ID of the project                                         | Yes      |
| `modpack-path`        | The path to the modpack zip                                   | Yes      |
| `modpack-server-path` | The path to the modpack server zip                            | No       |
| `changelog-path`      | The path to the changelog file                                | No       |
| `changelog-format`    | The changelog format (`text`/`html`/`markdown`)         | No       |
| `game-version`        | The game version                                              | No       |
| `display-name`        | The display name of the file                                  | Yes      |
| `server-display-name` | The display name of the server file                           | No       |
| `release-type`        | The release type of the file (`alpha`/`beta`/`release`) | Yes      |

## Example usage

```yml
uses: HaXrBOT/upload-curseforge-modpack-action@v1.2.0
with:
  api-token: "<YOUR TOKEN>"
  project-id: "1234"
  modpack-path: "./modpack.zip"
  modpack-server-path: "./modpack-server.zip" # Optional
  changelog-path: "changelog.md" # Optional
  changelog-format: "markdown" # Optional
  game-version: "1.20.1" # Optional
  display-name: "My Awesome Modpack"
  server-display-name: "My Awesome Modpack Server" # Optional
  release-type: "beta"
```
