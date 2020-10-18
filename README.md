# commands
Linux &amp; Other Commands


## Vim

### Find in File within Vim

#### Normal:
`:vim[grep][!] /{pattern}/[g][j] {file} ...`
#### Recursive:
`:vim[grep][!] /{pattern}/[g][j] {file} ...`
#### More Info:
https://vim.fandom.com/wiki/Find_in_files_within_Vim
 

## Find Command

### Find File
`find /home/username/ -name "*.err"`

### Find in Files

#### All the folders:
`find / -type f -exec grep -H 'find this text' {} \;`

#### Subtree folder we are there:
`find . -type f -exec grep -H 'find this text' {} \;`

#### Color
`find . -type f -exec grep -H --color 'find this text' {} \;`

## Grep Command 

#### Find text in files
`grep -rnw '/path/to/somewhere/' -e 'pattern'`

#### Find in current folder
`grep -rnw '.' -e 'pattern'`

#### Find including some file extensions
`grep --include=\*.{c,h,py} -rnw '.' -e 'pattern'`

#### Find excluding some file extensions
`grep --exclude=\*.{c,h,py} -rnw '.' -e 'pattern'`

#### Only Matching (too much text in files use this...)
`grep -rnwo '.' -e 'pattern'`

#### Researching (in progress) Limit the output string (to 10)
`grep -rnw '.' -E '^.{,100}$'`
`egrep -Rso '.{0,40}wp-content.{0,40}' *.sh`
`grep -rnw '.' -e 'pattern' .|cut -c -40`


