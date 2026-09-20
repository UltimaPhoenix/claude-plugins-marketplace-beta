# UltimaPhoenix Claude Code plugins — beta channel

The **beta** [plugin marketplace](https://code.claude.com/docs/en/plugin-marketplaces) of
UltimaPhoenix: the same plugins as [claude-plugins-marketplace](https://github.com/UltimaPhoenix/claude-plugins-marketplace),
pinned to their latest **canary** build instead of their latest release. Unreleased, may break.

```bash
/plugin marketplace add UltimaPhoenix/claude-plugins-marketplace-beta
/plugin install devcoach@ultimaphoenix-beta
```

The plugin keeps its name, so a beta installs side by side with the release with the same tools,
commands and skill. **Enable one channel at a time** — both ship the same hooks, and two copies
count every interaction twice (`devcoach doctor` warns when both are on). Update with
`/plugin marketplace update ultimaphoenix-beta`.

## Plugins

| Plugin | Canary source | Release |
|--------|---------------|---------|
| **devcoach** | the plugin zip of the rolling [`next` prerelease](https://github.com/UltimaPhoenix/dev-coach/releases/tag/next), built from `develop` on every green push | [`devcoach@ultimaphoenix`](https://github.com/UltimaPhoenix/claude-plugins-marketplace) |

## Maintenance

`.claude-plugin/marketplace.json` is the catalog. Each plugin's own repo CI pins its entry to the
latest canary (an `archive` source: the prerelease zip + its sha256), with a surgical merge that
never touches other entries. Nothing here is edited by hand.
