ddg-cli-py
==========

Simple command line interface to duckduckgo. Access instant answers and results from your terminal!

Example Usage
==========

You may like to export your PATH to include the path to the cloned repository. Then you could run the script without referencing its path.

`ddg "chrome" | less # query duckduckgo with the search term "chrome", pipe to less`

`ddg "freebsd" -m 10 # -m sets the max results to display to 10 `

`ddg -r 2 -b 'firefox' # access result #2 in the specified browser (opened via command line)`

`ddg -n # access the next page of results`

The script can be used as a Unix filter, meaning that it can be used as an intermediary in a command pipeline, taking input from stdin and outputting to stdout:

Say for whatever reason, you're getting this error message from mount and you want to pipe it to ddg and see if stackoverflow exists in the results:

redirect mount's  stderr to stdin, pipe to ddg setting max results to 10, grep for "stackoverflow" with 5 lines of context:
`mount /dev/sda1 /mnt 2>&1 | ddg -m 10 | grep -C 5 "stackoverflow" | less # not that you would ever do this :)`

etcetc.




