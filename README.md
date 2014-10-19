This repo contains a few scripts that use git to store snapshot of files.

## Installation
Simply copy the git-snap\* files to a ~/bin or add it to your PATH and git should automatically hook it up.

## Adding snapshot
`git snapadd target_file [label]`
Take a snapshot of the file

## Listing the snapshot for file
`git snaplist target_file`
List the snapshot available for the file

## Restoring file
`git snaprestore target_file <hash>`
Restore the hash for the file

The snapshot meta data is stored in .file.snapshot, and all the objects are stored in the same .git folder.
Note that all snapshot might be deleted when git does their gc, so this should be used for temporary storage.
