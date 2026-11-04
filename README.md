# unix-shell

A small Unix shell written in C for a systems programming course.

```
[/home/jimmy]>ls -l | grep .c > c_files.txt
```

## Features

- Runs programs with `fork` + `execvp`
- **Pipelines** of any length (`cmd1 | cmd2 | cmd3`) using `pipe` and `dup2`
- **I/O redirection** with `<` and `>`
- Built-in commands: `cd <dir>`, `export NAME=value`, and `q` to quit
- **Signal handling**: Ctrl+C / Ctrl+\ stop the running command, not the shell (`sigaction`, `sigprocmask`, `sigsetjmp` / `siglongjmp`)
- Prompt shows the current working directory

## Build & run (Linux / macOS)

```bash
gcc -o ush ush.c
./ush
```

## Credits

Built on the `ush` examples from Robbins & Robbins, *UNIX Systems Programming*. I added the `cd` and `export` built-ins and the working-directory prompt.
