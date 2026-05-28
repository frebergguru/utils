# delfiles

Recursively deletes common junk files (thumbnails, OS-generated metadata,
shortcut files) from the current directory and all subdirectories.

> **Warning:** uses `rm -rf`. Always inspect the file list before running.

## Usage

    delfiles         # prompt before deleting
    delfiles -y      # delete without prompting
    delfiles -h      # print help

## What gets deleted

- `albumart*.jpg`
- `folder.jpg`
- `thumbs.db`
- `desktop.ini`
- `*.lnk`
- `*ds_store*`
- directories named `system volume information`
- directories named `recycler`

## Versions

- **`delfiles`** — original; deletes one pattern at a time with a running
  counter persisted to `/tmp`.
- **`delfiles_v2`** — single `find` invocation; faster but no per-file
  counter.

## Installation

    ./install                    # installs to /usr/local/bin (needs sudo)
    PREFIX=~/.local ./install    # user-local install, no sudo

Uninstall with `./install uninstall`.

## License

GPL v3. This script comes with ABSOLUTELY NO WARRANTY. See the script
header for the full notice.
