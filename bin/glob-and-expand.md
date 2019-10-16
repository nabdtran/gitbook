# Glob & Expand

### Glob

rm \*.md = match any number of characters

ls ?.md = matches any 1 character

ls \[fatd\] = matches any files with any of the characters in it

ls \[0123\].csv = ls \[0-3\].csv = any of the characters .csv or range of numbers .csv

ls \*.{md,csv} = anything .md or .csv

### Expand

echo \[b..f\].py = show all files from b.py to f.py

echo {b..f}.py = show all files from b.py to f.py even if they do not exist

