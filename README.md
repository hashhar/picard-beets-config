# Music Organisation Config

This holds [MusicBrainz Picard](https://picard.musicbrainz.org/) config file, file
renaming script, other taggerscripts and my
[beets](https://github.com/beetbox/beets) config.

## Workflow

I currently have a workflow like:

1. Add tags, move and rename files using MusicBrainz Picard.
1. Run beets on the files with the writing, tagging and renaming options
disabled.
1. The keys which are left empty in the yaml need to be provided by a local
config file like `beets -c secrets.yaml`. A sample secret file can be seen
[here](./beets/sample_secrets.yaml).

This means that I can still use beets to do things like fetching lyrics (but
not writing to ID3 tags), creating smart-playlists, updating my MusicBrainz
collections etc.

Due to this workflow you might find that the beets config is lacking a lot of
plugins and configuration that would allow it to replace MusicBrainz Picard
like the chroma plugin, fetchart etc.
