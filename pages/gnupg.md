---
title: gnupg
---
# sign
- `gpg2 -ba [-u keyname] clear.txt` generate detached armored signature
- `gpg2 --verify [other.clear.txt] clear.txt.asc` by default, finds cleartext
  file removing `.asc`

# manage private keys
This is for gnupg 2.1 only.
- `gpg2 --delete-secret-keys`
- `gpg2 --delete-secret-and-public-keys`
- `gpg2 -K --with-keygrip` and then deleting files in `private-keys-v1.d` is
  needed in some scenarios (strip a single subkey, or delete a card-based key)

# get keystubs from a card
- fetch public key from a keyserver
- `gpg2 --card-edit`
- `gpg2 --edit-key`, `delkey` delete stripped subkeys which are not in the card

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
