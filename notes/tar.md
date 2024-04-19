# tar

## Examples

#### List contents of a tar or tar.gz file:

`tar -tvf tarfile.tar`

#### Extract a tar.gz archive:

`tar -xvzf tarfile.tar.gz`

#### Extract tar.bz2/bzip archives:

`tar -xvjf archivefile.tar.bz2`

#### Extract files to a specific directory or path:

`tar -xvzf tarfile.tar.gz -C /opt/folder/`

#### Extract a single file from an archive, and extract it to a specific directory:

`tar -xvf tarfile.tar root/anaconda-ks.cfg -C /tmp/`

#### Create a tar.gz archive:

`tar -cvzf tarfile.tar.gz dir/`

#### Create a tar.gz archive, but omit a file:

`tar -zcpvf myarchive.tgz /etc/ /opt/ --exclude=*.html`

#### Add files to existing archives:

`tar -rv -f tarfile.tar abc.txt`

#### Add files to compressed archives (tar.gz):

`gunzip tarfile.tar.gz`

`tar -rvf tarfile.tar ./path/to/file`

`gzip tarfile.tar`
