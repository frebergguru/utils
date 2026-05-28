# utils

A small collection of personal Unix shell utilities.

## Scripts

### cleanmpg

Strips metadata from all `.mp4` files in the current directory, writing the
cleaned copies to a `cleaned/` subdirectory.

**Requires:** `ffmpeg`

**Usage:**

    cd /path/to/videos
    cleanmpg

### cleanmpg_v2

Same as `cleanmpg`, but processes files in parallel and gives each
`ffmpeg` invocation 4 threads — much faster on multi-core machines with
many files.

**Requires:** `ffmpeg`, GNU `parallel`

**Usage:**

    cd /path/to/videos
    cleanmpg_v2

### delfiles

Recursively deletes a list of junk files (thumbnails, Windows/macOS
detritus, etc.) from the current directory. See
[`delfiles/README.md`](delfiles/README.md) for the full list and usage.

## License

GPL v3 — see individual script headers.
