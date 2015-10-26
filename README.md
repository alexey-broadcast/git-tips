# Git tips

## Просмотр изменений

```
git log
```

* `--author="Alex Kras"` — выводит коммиты, сделанные конкретным человеком
* `--name-only` — выводит только названия изменённых файлов
* `--oneline` — выводит сокращённые данные коммита (в виде одной строки)
* `--graph` — выводит дерево зависимостей для всех коммитов
* `--reverse` — выводит коммиты в обратном хронологическом порядке (сначала старые)
* `--after` — выводит коммиты, сделанные после определённой даты
* `--before` — выводит коммиты, сделанные до определённой даты

Вывод всех изменений в конкретном файле

```
git log -p filename
```

Посмотреть изменения в файле с 1 по 10 строку

```
git log -L 1,10:filename
```

Показать коммиты/изменения, которые еще не были смержены с веткой master

```
git log --no-merges master..
git show --no-merges master.. (git log -p --no-merges master..)
```

Посмотреть файл в ветке master, не переключаясь на нее

```
git show master:file.js
```

Cохранить файл из другой ветки

```
git show master:file.js > saved.js
```

Сравнить file.js в мастер бранче с текущим

```
git diff master file.js

```

## Отмена изменений

Добавить изменения в последний коммит, также можно отредактировать название последнего коммита

```
git commit --amend
```

Отменить все текущие изменения и вернуться на определенный коммит

```
git reset --hard {{ commit }}
```

Отменить изменения, включая новые директории

```
git clean -fd
```

Отменить изменения в одном файле

```
git checkout -- path/to/file
```
## Config
Изменить конфиг локально
```
git config user.name "John Doe"
git config user.email user@example.com
```
Вывод конфига
```
git config --list
```
## Github

Вывод конфига удаленного репозитория

```
git remote -v
```

Добавить upstream
```
git remote add upstream https://github.com/octocat/Spoon-Knife.git
```
