# Vim on MacOS

## error: invalid active developer path, missing xcrun

This error normally happens after MacOS upgrade.

The simple fix is:

```bash
xcode-select --install
# sometime we need call reset:
sudo xcode-select --reset
```
