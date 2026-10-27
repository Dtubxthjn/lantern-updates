# Lantern releases

This repository hosts Lantern installers and the signed in-app update manifest. File transfers remain on the local network.

## Publish a release

1. Prepare the tested Android, Windows, Linux DEB and Linux AppImage builds.
2. Run the private release-signing helper to generate stable.json. Never upload signing keys.
3. Create a non-prerelease GitHub Release using the exact tag provided by the helper.
4. Attach all four installers and stable.json, then publish. Keep installer filenames unchanged.

The initial updater-enabled release is desktop 5.2.0 / Android 3.2.0. Install it manually over the previous app once. Newer versions can then be checked and downloaded under You → App updates. Android and Linux may require normal OS confirmation. Windows installers are currently unsigned.

The app verifies the release signature and downloaded package hash before allowing installation. Android additionally checks the package identity, newer version code and matching APK signer.
