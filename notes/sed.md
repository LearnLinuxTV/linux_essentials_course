# sed

## Examples

#### Remove lines that contain a specific string

sed '/stringtoremove/d' file.txt

#### Find and replace a string in a file

`sed -i 's/foo/bar/g' file.txt`

#### Append a line after the matched line

`sed -i '/line that exists/a new line to be added` \*.txt

#### Find and replace a string in files (recursive)

`find . -type f -exec sed -i 's/foo/bar/g' {} +`

#### Find and replace a string in files (recursive, but avoid hidden files)

`find . -type f -not -path '*/\.*' -exec sed -i 's/foo/bar/g' {} +`

#### Example of using the find command with sed, but with a different separator

`find . -type f -exec sed -i 's_https://www.oldurl.com/blog_https://www.newurl.com/blog_g' {} +`

#### Remove a line from a file (when the line contains slashes)

`sed '\|^/dev/xvdb|d' /etc/fstab`

Note: When you use a non-standard delimeter, the delimeter needs to be escaped
