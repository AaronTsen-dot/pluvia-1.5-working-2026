# Pluvia 1.5 Working Copy

Verified working Pluvia 1.5 setup for iPhone 4 (`iPhone3,1`), including iOS 5.1.1 patched IPSW creation and restore notes for an Intel-based Mac running macOS Mojave 10.14.6.

## Verified Result

- Patched IPSW creation completed successfully for iOS 5.1.1 (`9B206`)
- Restore completed successfully to an iPhone 4 in DFU mode
- Tested on an Intel Mac running macOS Mojave 10.14.6

## Usage

### Create a patched IPSW

```bash
./make_ipsw.sh <Input_IPSW>
```

Or, if you want the jailbreak payload when supported:

```bash
./make_ipsw.sh <Input_IPSW> jailbreak
```

### Restore the patched IPSW

Put the iPhone 4 in DFU mode, then run:

```bash
./restore.sh <Patched_IPSW>
```

## Notes

- This project currently targets `iPhone3,1`
- Supported firmware range in this working copy is iOS 5.1.1 (`9B206`), 6.x, and 7.x
- During verification on Mojave, the working `tools/ipsw` binary matched the stable `tools/ipsw.prebuilt` copy
- The second Cydia launch after "Preparing Filesystem" may crash on supported jailbreak flows; rebooting the device resolves it

## Do Not Upload

- Apple IPSW files
- SHSH blobs
- Generated `work/` contents
- Device-specific logs or artifacts

## Credits

Original project credits are preserved in [`readme.txt`](./readme.txt).
