# AISH Shell (Aditi's Interactive SHell)

## Introduction
The "Aish" shell, short for Aditi's Interactive Shell, is a Unix-like shell implemented in C. It offers a range of features, including inbuilt shell commands, piping, redirection, job control, and additional functionalities. "Aish" is designed to provide a user-friendly interface and helpful error messages for incorrect syntax or invalid commands.

## Getting Started
To use Aish, follow these simple steps:
1. Run the `make` command in your terminal to compile the source code, generating an executable file named "aish."
2. Execute the shell by running the command `./aish`.

## Functionalities
Aish provides the following built-in commands and features:

- **cd Command**: Change the current directory. If no path is given, it defaults to the home directory.
- **pwd**: Display the present working directory.
- **echo**: Print text on the shell.
- **ls Command**: List files in a given directory. Supports flags like `-l` (detailed file information) and `-a` (show hidden files).
- **pinfo [pid]**: Print information about a process, including its process ID, status, memory usage, and executable path.
- **clear**: Clear the console.
- **exit**: Exit the shell.
- **repeat [n] [command]**: Execute a given instruction "n" times.
- **Background Process**: Run a command in the background by appending `&` at the end.
- **Redirection**: Handle input and output redirection using `<`, `>`, and `>>`.
- **Piping**: Implement command pipelines using `|`.
- **jobs**: List all currently running background processes, displaying their job number, process ID, and state (running or stopped). Accepts flags like `-r` (running) and `-s` (stopped).
- **sig [job_number] [signal]**: Send a signal to a job with a specified job number.
- **fg [job_number]**: Bring a background job specified by the given job number to the foreground.
- **bg [job_number]**: Change the state of a stopped background job to running in the background.
- **Signal Handling**: Respond to signals such as Ctrl+C (SIGINT), Ctrl+D (shell exit), and Ctrl+Z (push foreground job into the background).
- **Replay Command**: Execute a given command at fixed time intervals for a specified period.
- **All Other Commands**: Any commands not explicitly handled by "Aish" are executed through the `execvp` function, allowing for flexibility in command execution.

## File Structure
- `main.c`: Contains the main loop, input parsing, and signal handling.
- `execute.c`: Parses and executes commands, including built-in commands like `cd`, `echo`, and `pwd`.
- `pinfo.c`: Prints information about a process.
- `bg.c`: Manages the execution of background processes.
- `ls.c`: Handles the `ls` command with flags (-a, -l, -la, -al, -a -l).
- `ls_file.c`: Manages the `ls` command for files.
- `display.c`: Displays the shell prompt.
- `replay.c`: Handles the replay command.
- `sig2.c`: Manages the `bg`, `fg`, and `sig` commands.
- `jobs.c`: Manages the jobs command.
- `piping.c`: Handles piping.
- `redirection.c`: Manages redirection.
- `shell.h`: Contains function declarations, global variables, and defined constants.

## Documentation
This `README.md` file serves as documentation for the "Aish" shell, providing valuable information about its usage, features, and code structure. It aims to assist users and developers in understanding the project better.

## Structure Explanation
This section gives an overview of the project's structure, explaining the organization of different components in the codebase.

## Signal Handling
Here, we describe how "Aish" handles various signals, ensuring proper control over processes and user interactions.

## Replay Command
An explanation of the "replay" command is provided, outlining its functionality and usage.

## Handling Other Commands
It is noted that any commands not explicitly handled by "Aish" are executed through the `execvp` function, allowing for flexibility in command execution.
