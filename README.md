# teeoe

Launch a script and redirect stderr and stdout to log files while still showing them in the terminal.  
Any script with any number of parameters can be launched, stderr will be redirected to err.log (or specified path with -e) and stdout will be redirected to out.log (or specified path with -o). All output will still show on terminal.

# Usage:  
`./teeoe [OPTION] script` or `teeoe [OPTION] script`  
A script must be provided.  

# Options:  
  -e  Filename for the stderr redirection (default: ./err.log)  
  -o  Filename for the stdout redirection (default: ./out.log)  

# Installation

You can directly copy the teeoe file to your bin folder to execute it from anywhere or execute it direcly with ./teeoe or bash teeoe.
