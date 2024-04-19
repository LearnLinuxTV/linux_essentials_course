# find

## Command examples

### Find files in the current working directory with a specific name pattern

`find . -name "*search-term*"`

### Find files less than a certain size

`find . -type f -size -10 -ls`

### Change permissions on specifically just directories or files

#### For directories:

`find /path/to/something/ -type d -exec chmod 755 {} \;`

#### For files:

`find /path/to/something/ -type f -exec chmod 644 {} \;`

### Remove files older than 90 days

`find /path/containing/files/* -mtime +90 -exec rm {} \;`

### Recursively change spaces to underscores

`find /dir -depth -name "* *" -execdir rename 's/ /_/g' "{}" \;`

### Find files older than 6 days, and compress them individually

`find . -type f -mtime +6 -exec gzip {} \;`
