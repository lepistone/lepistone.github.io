---
title: gnupg
layout: cheatsheet
---
# sign
- `gpg2 -ba [-u keyname] clear.txt` generate detached armored signature
- `gpg2 --verify [other.clear.txt] clear.txt.asc`

# --edit-key

## subkeys
- `key` select subkey with index N, none for none, * for all
- `addkey`
- `delkey`
- `revkey`
- `expire`
- `addcardkey` generate a subkey on a card and add it to this key
- `keytocard` move a key to a card, keep only a stub

## uids
- `uid` select uid with index N, none for none, * for all
- `adduid`
- `primary` make uid primary

## misc
- `fpr` show fingerprint
- `showpref` show preferences

# export
- `--export-secret-keys` -ao filename keyname
- `--export-secret-subkeys`
