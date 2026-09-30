# C Shell — Unix Shell Implementation

A Unix-like command-line shell implemented in **C**, focusing on process management, command execution, pipelines, signals, background processes, file-system navigation, and persistent command history.

## Features

- Interactive custom shell prompt
- Execution of external commands
- Foreground and background process execution
- Process and activity management
- Command pipelines using `|`
- Input/output redirection
- Signal handling and process control
- Persistent command history using `pastevents`
- File-system navigation and inspection
- Custom commands such as `warp`, `peek`, `seek`, `proclore`, and `neonate`
- Modular implementation using separate C source and header files
- Execution-time reporting for long-running commands

## System Concepts

The implementation uses core Unix/Linux concepts including:

- `fork()` and `exec()` for process creation and command execution
- Pipes for inter-process communication
- Signals for process control
- File descriptors and I/O redirection
- Foreground/background process management
- File and directory operations
- Persistent file-based command history

## Build & Run

### Prerequisites

- GCC
- `make`
- Linux/Unix environment

### Build

```bash
make
```

### Run

```bash
./a.out
```

### Clean Build

```bash
make clean
```

## Project Structure

```text
.
├── main.c
├── prompt.c / prompt.h
├── system.c / system.h
├── warp.c / warp.h
├── peek.c / peek.h
├── seek.c / seek.h
├── proclore.c / proclore.h
├── pipe.c / pipe.h
├── signal.c / signal.h
├── FgBg.c / FgBg.h
├── activites.c / activites.h
├── pastevents.c / pastevents.h
├── iman.c / iman.h
├── neonate.c / neonate.h
├── makefile
└── pastevents.txt
```

## Command History

The `pastevents` functionality stores command history in `pastevents.txt`, allowing commands to be maintained across shell sessions.

## Input Handling

The shell supports bounded command input, including limits on overall input size, commands separated by `;` and `&`, command length, words per command, word length, and path length.

## Course Project

**Operating Systems and Networks (OSN) — Unix Shell Implementation**

This project was developed as an individual course assignment using the required module and file naming convention.
