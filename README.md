# Peyman Claims — Update Releases

This repository is used to publish signed-off Windows update packages for **سامانه پیگیری مطالبات پزشکی پیمان**.

## Update channel

- Provider: GitHub Releases
- Repository: https://github.com/navidnzrii/peyman-claims-updates
- Platform: Windows x64
- Installer format: NSIS `.exe`
- Release assets for Electron auto-updates should include the generated installer package and the metadata files produced by `electron-builder` (for example, `latest.yml` and the corresponding blockmap).

## Publishing a release

1. Increase the application version in the app's `package.json`.
2. Build the Windows NSIS target with `npm run dist`.
3. Publish the generated update artifacts to a GitHub Release whose tag matches the app version (for example, `v2.0.1`).
4. Keep the installer and updater metadata together in the same release.

## Important

- Do not upload customer databases, backups, credentials, access tokens, or private configuration files.
- Keep application data in the user's writable application-data directory, not in the installation directory, so upgrades do not overwrite user records.
- The desktop application's updater must be configured to use this repository and should verify/download updates before prompting the user to install.

This repository currently contains release-channel documentation only. No application binaries or update releases have been published yet.
