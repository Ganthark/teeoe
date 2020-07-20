# teeoe

Launch a script and redirect stderr and stdout to log files while still showing them in the terminal.

Usage: ./teeoe: [OPTION] script
A script must be provided.
OPTIONS:
  -e  Filename for the stderr redirection (default: ./err.log)
  -o  Filename for the stdout redirection (default: ./out.log)

Any script with any number of parameters can be launched, stderr will be redirected to err.log (or specified path with -e) and stdout will be redirected to out.log (or specified path with -o). All output will still show on terminal.
