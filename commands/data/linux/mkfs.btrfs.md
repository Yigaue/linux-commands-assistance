# mkfs.btrfs

> Create a BTRFS filesystem.
> Defaults to `raid1`, which specifies 2 copies of a data block spread across 2 different devices.
> More information: <https://btrfs.readthedocs.io/en/latest/mkfs.btrfs.html>.

- Create a btrfs filesystem on a single device:

`sudo mkfs.btrfs --metadata single --data single {{/dev/sdX}}`

- Create a btrfs filesystem on multiple devices with raid1:

`sudo mkfs.btrfs --metadata raid1 --data raid1 {{/dev/sdX /dev/sdY /dev/sdZ ...}}`

- Set a label for the filesystem:

`sudo mkfs.btrfs --label "{{label}}" {{/dev/sdX /dev/sdY ...}}`
