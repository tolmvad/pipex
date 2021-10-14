[![eng](img/eng.png)](README.md) ![ru](img/ru.png)
# `pipex`

Цель данного проекта детальное рассмотрение UNIX механизма `pipe`.<br>
Задание можно прочитать здесь: [`pipex.subject.pdf`](subject/pipex.subject.pdf)

### Описание основной части
Программа `pipex` должна повторять поведение следующей команды оболочки
```bash
$> < file1 cmd1 | cmd2 > file2
```
и выглядеть следующим образом:
```bash
$> ./pipex file1 cmd1 cmd2 file2
```
Необходимо обрабатывать все ошибки, такие как: неправильные команды, отсутствие необходимых прав у файлов и т.д.
### Описание бонусной части
Программа должна обрабатывать несколько пайпов.
```bash
$> < file1 cmd1 | cmd2 | cmd3 | ... | cmdn > file2

$> ./pipex file1 cmd1 cmd2 cmd3 ... cmdn file2
```
Поддерживать `<<` и `>>`, когда вместо `file1` передается`here_doc`.
```bash
$> cmd1 << LIMITER | cmd2 >> file2

$> ./pipex here_doc LIMITER cmd1 cmd2 file2
```

### Оценка от moulinette

![125/100](img/125.png)
