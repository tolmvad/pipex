![eng](img/eng.png) [![ru](img/ru.png)](README.ru.md)
# `pipex`

The purpose of this project is the discovery in detail UNIX mechanism - `pipe`.<br>
You can read task: [`pipex.subject.pdf`](subject/pipex.subject.pdf)


### Discription of mandatory part
The program `pipex` should repeat the behaviour of the next shell command
```bash
$> < file1 cmd1 | cmd2 > file2
```
and looks like this:
```bash
$> ./pipex file1 cmd1 cmd2 file2
```
All errors like: wrong commands,  permission to files and etc, need be handle.
### Discription of bonus part
Program need handle multiple pipes
```bash
$> < file1 cmd1 | cmd2 | cmd3 | ... | cmdn > file2

$> ./pipex file1 cmd1 cmd2 cmd3 ... cmdn file2
```
Support `<<` and `>>`, when instead of `file1` is`here_doc`.
```bash
$> cmd1 << LIMITER | cmd2 >> file2

$> ./pipex here_doc LIMITER cmd1 cmd2 file2
```

### Evaluated by moulinette

![125/100](img/125.png)
