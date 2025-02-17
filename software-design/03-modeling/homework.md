В командах по два-три человека спроектировать простой интерпретатор командной строки, поддерживающий команды:

- `cat [FILE]` — вывести на экран содержимое файла;
- `echo` — вывести на экран свой аргумент (или аргументы);
- `wc [FILE]` — вывести количество строк, слов и байт в файле;
- `pwd` — распечатать текущую директорию;
- `exit` — выйти из интерпретатора.

При этом должны поддерживаться:

- одинарные и двойные кавычки (full and weak quoting);
- окружение (команды вида “имя=значение”), оператор `$`;
- вызов внешней программы, если введено что-то, чего интерпретатор не знает;
- пайплайны (оператор «`|`»).

Примеры
```
>echo "Hello, world!"
Hello, world!

> FILE=example.txt
> cat $FILE
Some example text

> cat example.txt | wc
1 3 18

> echo 123 | wc
1 1 3

> x=ex
> y=it
> $x$y
```

Решение должно удовлетворять следующим нефункциональным требованиям:

- легко добавлять новые команды;
- чёткое разграничение ответственности между элементами архитектуры;
  - это не должен быть просто клубок классов, требуется некая компонентная структура;
- наличие словесного архитектурного описания.

Задача выполняется в командах по 2-3 человека. Результатом должна являться структурная диаграмма (например, диаграмма классов UML), описывающая систему, и текстовое описание того, как спроектированное приложение должно работать. Решение сдаётся в виде .pdf/.md-файла или ссылки на документ в каком-либо из облачных сервисов. Обязательно укажите, с кем вы в команде.

Обратите внимание, реализовывать этот проект не нужно!

