# bradfordwagner.ansible-role-wiz

## Updating the version

Version is controlled by `wiz_ver` in `defaults/main.yml`.

```yaml
wiz_ver: X.Y.Z
```

Wiz CLI does not have a public GitHub releases page. Check the latest version in the
[Wiz release notes](https://docs.wiz.io/wiz-docs/docs/wizcli-changelog) or by logging
into your Wiz tenant and checking the CLI download page.

Renovate reads versions from `https://downloads.wiz.io/v1/wizcli/manifest.json` (custom datasource `wizcli` in `renovate.json`).

Downloads are served from: `https://downloads.wiz.io/v1/wizcli/<version>/wizcli-<os>-<arch>`

## Renovate

Renovate (`bradfordwagner/renovate`, preset `ansible-role`) opens PRs for the version pins marked `# renovate:`, `meta/requirements.yml`, `config.yaml`'s `upstream.tag` and GitHub Actions. A merged PR labeled `release` is tagged with the next patch version and published to Galaxy by `.github/workflows/release.yml`.
