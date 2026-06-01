# Shellex Repos

Public Limax registry for official Shellex app repositories.

This repository does not contain Shellex OS and does not contain app source code. It only lists public `elmirok/shellex-*` app repositories that expose a `package.sapp.json` file for browser-only Limax installs and updates.

## Use With Limax

Inside Shellex OS Shell:

```txt
limax repo sync https://github.com/elmirok/shellex-repos
limax repos
limax install W3
limax install Filella
limax update
```

If no URL is provided, Shellex uses this registry as the default:

```txt
limax repo sync
```

## Registry File

Limax reads:

```txt
repos.json
```

Each listed app repo should expose:

```txt
package.sapp.json
```

on `main` or `master`. Each registry entry may include `expectedSha256`; Limax uses it to reject a package whose fetched SHA-256 does not match the official registry pin.

## Trust Pins

The official registry records SHA-256 pins for current app packages. When app packages are released, update the app repo first, then update `repos.json` with the new package hash.

## Privacy

This registry contains only public repository metadata. It does not contain vault data, user files, app data, telemetry, accounts, or secrets.
