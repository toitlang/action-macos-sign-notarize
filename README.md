# Codesign and Notarize

A Github Action to codesign and notarize a macOS executable.

This action only runs on macOS.

## Inputs

All inputs are required.

| Name | Description | Example Value |
| ---- | ----------- | ------------- |
| certificate | The certificate for signing | `${{ secrets.CERTIFICATE }}` |
| certificate-password | The password for the certificate | `${{ secrets.CERTIFICATE_PASSWORD }}` |
| username | The Apple ID username to use for notarization | `${{ secrets.APPLE_ID_USERNAME }}` |
| password | The Apple ID password to use for notarization | `${{ secrets.APPLE_ID_PASSWORD }}` |
| apple-team-id | The Apple Team ID to use for signing and notarization | `33DS2ZRDST` |
| app-path | The path to the application to sign and notarize | `build/my_app` |

## Usage

```yaml
- name: Sign and notarize the release build
  uses: toitlang/action-macos-sign-notarize@v1
  with:
    certificate: ${{ secrets.CERTIFICATE }}
    certificate-password: ${{ secrets.CERTIFICATE_PASSWORD }}
    username: ${{ secrets.APPLE_ID_USERNAME }}
    password: ${{ secrets.APPLE_ID_PASSWORD }}
    apple-team-id: 33DS2ZRDST
    app-path: build/my_app
```
