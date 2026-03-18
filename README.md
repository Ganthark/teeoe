# teeoe
Launch a script and redirect stderr and stdout to log files while still showing them in the terminal.  
Any command with any number of parameters can be launched, stderr will be redirected to `<cmd>.err` and stdout to `<cmd>.out` (or specified paths with `-e`/`-o`). All output will still show in the terminal.

# Usage
`./teeoe [OPTION] command [args...]` or `teeoe [OPTION] command [args...]`  
A command must be provided. Shell builtins (e.g. `history`, `cd`) are not supported.

# Options
- `-e`  Filename for the stderr redirection (default: `./<cmd>.err`)
- `-o`  Filename for the stdout redirection (default: `./<cmd>.out`)
- `-l`  Directory to write log files into (default: current directory)

# Examples
```
teeoe grep "string" file.txt           # -> ./grep.out & ./grep.err
teeoe ./scripts/analysis/example.sh   # -> ./example.out & ./example.err
teeoe -l logs/ ./run.sh -v             # -> logs/run.out & logs/run.err
teeoe -l logs/ -e custom.err ./run.sh  # -> logs/run.out & custom.err
```

# Installation
Copy the `teeoe` file to your bin folder to execute it from anywhere, or run it directly with `./teeoe` or `bash teeoe`.
