Introduction
============

During my ([@fd0](https://github.com/fd0)) research before starting
[restic](https://restic.github.io) I've tested a lot of different backup
programs. However, even after working in this space for a few years, I still
stumble across backup solutions I didn't know about.

In this repository, I'd like to collect backup solutions and eventually end up
with an exhaustive list of backup software. The criteria for inclusion are:

 * Free Software (not just Open Source)
 * Does not require custom network/cloud service to operate (sorry,
   [tarsnap](http://www.tarsnap.com/))
 * Works on Linux
 * Is a dedicated to backup (sorry, [camlistore](https://camlistore.org/))

If you know other backup solutions that fit the criteria above, please create a
pull request!

Note:
=====

A lot of FOSS backup solutions are merely shells on top of rsync and/or duplicity.
Perhaps these should have a category of their own, or a tag?

TODO
====

In the future we plan to provide benchmarks using [fakedatafs](https://github.com/restic/fakedatafs) and a table to sort by the tag categories.

If anyone wants to help out, please submit a PR with your contribution.

List of Backup Software
=======================

Tags used below:
- `authenticated`: Uses cryptographic signatures or MAC tags to ensure integrity
- `compression`: Storage with compression
- `dedup`: Supports deduplication
- `encrypted`: Supports encrypting data locally (stored encrypted on the backup medium)
- `error-correction`: Supports reconstructing data in scenarios x-of-n backup media are lost
- `golang`: Written in Go-lang
- `gpg`: Uses GPG for the underlying encryption
- `incremental`: Support for incremental backups (through deltas or local deduplication)
- `perl`: Written in Perl
- `python`: Written in Python
- `review`: Needs to be reviewed by the authors of this list in order to revise the tags assigned here.
- `rsync`: Uses `rsync` or `librsync`
- `rust`: Written in Rust
- `s3`: Supports Amazon S3-compatible backends
- `ssh`: Supports SFTP/SCP backends
- `unmaintained`: Looks unmaintained / dead

The following list is sorted alphabetically:

|                                                                                          | authenticated | compression | dedup | encrypted | error-correction | golang | gpg | incremental | perl | python | rsync | rust | s3 | ssh | unmaintained |  
| ---------------------------------------------------------------------------------------- | :-----------: | :---------: | :---: | :-------: | :--------------: | :----: | :-: | :---------: | :--: | :----: | :---: | :--: |:-: | :-: | :----------: |
| [attic](https://github.com/jborg/attic)                                                  | x             |             | x     | x         |                  |        |     |             |      | x      |       |      |    |     | x            |
| [areca](http://areca-backup.org)                                                         |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [Arqinator](https://github.com/asimihsan/arqinator)                                      |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [backshift](http://stromberg.dnsalias.org/~strombrg/backshift/)                          |               |             |       |           |                  |        |     |             |      |        |       |      |    | x   |              |
| [backup](https://github.com/backup/backup)                                               |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [backup2l](http://backup2l.sourceforge.net/)                                             |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [BackupPC](http://backuppc.sourceforge.net/)                                             |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [Backups-Done-Right](https://github.com/spikebike/Backups-Done-Right)                    |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [bareos](https://www.bareos.org/en/)                                                     |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [BlobSnap](https://github.com/tsileo/blobsnap)                                           |               |             | x     |           |                  | x      |     | x           |      |        |       |      |    |     |              |
| [borg](https://github.com/borgbackup)                                                    | x             |             | x     | x         |                  |        |     | x           |      | x      |       |      |    |     |              |
| [brackup](http://search.cpan.org/~bradfitz/Brackup-1.10/lib/Brackup/Manual/Overview.pod) |               |             | x     | x         |                  |        | x   |             | x    |        |       |      |    |     | x            |
| [btar](http://viric.name/cgi-bin/btar/)                                                  |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [btbrk](https://github.com/digint/btrbk)                                                 |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [bup](https://github.com/bup/bup)                                                        |               |             | x     |           | x                |        |     | x           |      |        |       |      |    |     |              |
| [burp](http://burp.grke.org/)                                                            |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [cedar-backup3](https://bitbucket.org/cedarsolutions/cedar-backup3/wiki/Home)            |               |             |       |           |                  |        |     |             |      | x      |       |      |    |     |              |
| [chop-backup/libchop](http://nongnu.org/libchop/)                                        |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [dar](http://dar.linux.free.fr/)                                                         |               | x           |       | x         |                  |        |     | x           |      |        |       |      |    |     |              |
| [ddar](https://github.com/basak/ddar)                                                    |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [deltaic](https://github.com/cmusatyalab/deltaic)                                        |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [duplicati](https://github.com/duplicati/duplicati)                                      |               |             |       | x         |                  |        | x   |             |      |        |       |      |    | x   |              |
| [duplicity](http://duplicity.nongnu.org/)                                                |               | x           |       | x         |                  |        | x   |             |      | x      | x     |      | x  | x   |              |
| [fwbackups](http://www.diffingo.com/oss/fwbackups/features)                              |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [Frost](https://github.com/X-Ryl669/Frost/)                                              |               |             | x     | x         |                  |        |     |             |      |        |       |      |    |     |              |
| [git-annex](https://git-annex.branchable.com/)                                           |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [hashbackup](http://www.hashbackup.com/)                                                 |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [hdup2](https://wiki.archlinux.org/index.php/Hdup)                                       |               |             |       |           |                  |        | x   |             |      |        |       |      |    | x   | x            |
| [hindsight](https://github.com/br0ns/hindsight)                                          |               |             |       |           |                  |        |     |             |      |        |       |      |    |     | x            |
| [kebab](https://github.com/davidlazar/kebab)                                             |               |             |       |           |                  | x      |     |             |      |        |       |      |    |     |              |
| [knoxite](https://github.com/knoxite/knoxite)                                            | x             | x           | x     | x         | x                | x      |     | x           |      |        |       |      | x  |     |              |
| [obnam](http://obnam.org/)                                                               |               |             |       | x         |                  |        | x   |             |      |        |       |      |    |     | x            |
| [ori](http://ori.scs.stanford.edu/)                                                      |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [preserve](https://github.com/cholcombe973/preserve)                                     |               |             | x     | x         |                  |        |     |             |      |        |       | x    |    |     |              |
| [pukcab](https://github.com/lyonel/pukcab)                                               |               |             |       |           |                  | x      |     |             |      |        |       |      |    |     |              |
| [PyHardLinkBackup](https://github.com/jedie/PyHardLinkBackup/)                           |               |             | x     |           |                  |        |     | x           |      | x      |       |      |    |     |              |
| [rdiff-backup](http://www.nongnu.org/rdiff-backup/)                                      |               | x           |       |           |                  |        |     | x           |      |        |       |      |    | x   | x            |
| [rdedup](https://github.com/dpc/rdedup)                                                  |               |             | x     | x         |                  |        |     |             |      |        |       | x    |    |     |              |
| [rdup](http://zbackup.org/)                                                              |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [restic](https://restic.github.io)                                                       | x             |             | x     | x         |                  | x      |     | x           |      |        |       |      | x  | x   |              |
| [rsbackup](http://www.greenend.org.uk/rjk/rsbackup/)                                     |               |             |       |           |                  |        |     |             |      |        | x     |      |    | x   |              |
| [rsnapshot](http://rsnapshot.org/)                                                       |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [scat](https://github.com/Roman2K/scat)                                                  |               |             | x     | x         | x                | x      |     |             |      |        |       |      |    |     |              |
| [shield](https://github.com/starkandwayne/shield)                                        |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [snaprd](https://gitlab.tuebingen.mpg.de/stark/snaprd)                                   |               |             |       |           |                  | x      |     |             |      |        | x     |      |    |     |              |
| [snebu](http://www.snebu.com/)                                                           |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [s3git](https://github.com/s3git/s3git)                                                  |               |             | x     |           |                  | x      |     | x           |      |        |       |      | x  |     |              |
| [storeBackup](https://savannah.nongnu.org/projects/storebackup)                          |               |             |       |           |                  |        |     |             |      |        |       |      |    |     | x            |
| [ugarit](https://www.kitten-technologies.co.uk/project/ugarit/doc/trunk/README.wiki)     |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [unison](https://www.cis.upenn.edu/~bcpierce/unison/)                                    |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [urbackup](https://www.urbackup.org/)                                                    |               |             |       |           |                  |        |     |             |      |        |       |      |    |     |              |
| [veb](https://github.com/spydez/veb)                                                     |               |             |       |           |                  | x      |     | x           |      |        |       |      |    |     |              |
| [zbackup](http://zbackup.org/)                                                           |               | x           | x     | x         |                  |        |     | x           |      |        |       |      |    |     |              |
| [zpaq](http://mattmahoney.net/dc/zpaq.html)                                              |               | x           | x     | x         |                  |        |     | x           |      |        |       |      |    |     |              |

List of wrappers or helper tools:
- [atticmatic](https://torsion.org/atticmatic/) review,attic,borg
- [backupninja](https://0xacab.org/riseuplabs/backupninja) borg([WIP](https://0xacab.org/riseuplabs/backupninja/merge_requests/1)),bup,duplicity,dsync,rdiff-backup,restic([WIP](https://0xacab.org/riseuplabs/backupninja/merge_requests/2)),rsnapshot,rsync,tar
- [deja-dup](https://wiki.gnome.org/Apps/DejaDup) review,duplicity
