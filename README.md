# <img src="https://logowik.com/content/uploads/images/423918.logowik.com.webp" style="width: 40px; height: auto;"> This project is part of my cursus at School 42 <img src="https://logowik.com/content/uploads/images/423918.logowik.com.webp" style="width: 40px; height: auto;">

## 💡 About This Project

Pipex is a project from the 42 curriculum that focuses on recreating the UNIX pipe functionality in C. The goal is to gain a deeper understanding of process communication in a Unix-like environment, using pipes and file redirection.

The program simulates the shell command `< file1 cmd1 | cmd2 > file2`

This project strengthens skills in:
- Working with system calls like `pipe()`, `fork()`, `dup2()`, and `execve()`.
- Managing processes and file descriptors.
- Handling errors and memory leaks.

## 📋 Requirements

- Program must be written in C.
- Must comply with the 42 School Norm.
- Handle errors such as segmentation faults, memory leaks, and unexpected program exits.
- External functions authorized : `open`, `close`, `read`, `write`, `malloc`, `free`, `perror`, `strerror`, `access`, `dup`, `dup2`, `execve`, `exit`, `fork`, `pipe`, `unlink`, `wait`, `waitpid`

## 🛠️ How to use

1. `make bonus`
2. `./pipex_bonus file1 cmd1 cmd2 ... cmdx file2`

It will behave like : 
`< infile cmd1 | cmd2 | cmd3 | cmd4 > outfile`

You can also use with multiple commands and here-doc support. `./pipex_bonus here_doc LIMITER cmd1 cmd2 file`

### Example 1

1. `touch infile`
2. `./pipex_bonux infile 'ls -l' 'wc -l' outfile`

### Example 2

1. `./pipex here_doc END cat "wc -l" outfile`

## Rating

![Rating](./ressources/rating.png)
