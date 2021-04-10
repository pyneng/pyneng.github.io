---
title: "Работа с заданиями"
permalink: /docs/pyneng/
excerpt: "pyneng"
---

## Где решать задания

Все задания по курсу находятся в каталоге exercises в вашем приватном репозитории.
Задания надо выполнять в подготовленных файлах.

Например, в разделе 04_data_structures есть задание 4.3. Чтобы выполнить его надо открыть файл exercises/04_data_structures/task_4_3.py и выполнять задание прямо в этом файле после описания задания.


## Скрипт pyneng

[Установка и подготовка к работе с pyneng](https://pyneng.github.io/docs/pyneng-prepare/)

Этапы работы с заданиями:

1. Выполнение заданий
2. Проверка, что задание отрабатывает как нужно ``python task_4_2.py`` или запуск скрипта в редакторе/IDE
3. Проверка заданий тестами ``pyneng 1-5``
4. Если тесты проходят, смотрим варианты решения ``pyneng 1-5 -a``
5. Сдача заданий на проверку ``pyneng 1-5 -c`` 


> Второй шаг очень важен, потому что на этом этапе намного проще найти ошибки в синтаксисе
> и подобные проблемы с работой скрипта, чем при запуске кода через тест на 3 этапе.

## Проверка заданий тестами

После выполнения задания, его надо проверить с помощью тестов.
Для запуска тестов, надо вызвать pyneng в каталоге заданий.
Например, если вы делаете 4 раздел заданий, надо находиться в каталоге exercises/04_data_structures/
и запустить pyneng одним из способов, в зависимости от того какие задания на проверять.

[Примеры вывода тестов с пояснениями](https://pyneng.github.io/docs/pyneng-output/)

Запуск проверки всех заданий текущего раздела:

```
pyneng
```

Запуск тестов для задания 4.1:

```
pyneng 1
```

Запуск тестов для заданий 4.1, 4.2, 4.3:

```
pyneng 1-3
```

Если есть задания с буквами, например, в 7 разделе, можно запускать так,
 чтобы запустить проверку для заданий 7.2a, 7.2b (надо находиться в каталоге 07_files):

```
pyneng 2a-b
```

или так, чтобы запустить все задания 7.2x с буквами и без:

```
pyneng 2*
```


## Получение ответов

Если задания проходят тесты, можно посмотреть варианты решения заданий.

Для этого к предыдущим вариантам команды надо добавить ``-a``.
Такой вызов значит запустить тесты для заданий 1 и 2 и скопировать ответы, если тесты прошли:

```
pyneng 1-2 -a
```

Тогда для указанных заданий запустятся тесты и для тех заданий из них,
которые прошли тесты, скопируются ответы в файлы answer_task_x.py в текущем каталоге.

Ответы по желанию, можно добавлять в репозиторий с помощью git.

## Сдача заданий на проверку

> Для сдачи задания на проверку, надо сгенерировать токен на Github.
> Как это сделать написано в инструкции [Подготовка к работе с заданиями](https://pyneng.github.io/docs/pyneng-prepare/)

После того как задания прошли тесты и вы посмотрели варианты решения заданий,
можно сдавать задания на проверку.

Для этого надо добавить ``-c`` к вызову pyneng:
Такой вызов значит запустить тесты для заданий 1 и 2 и сдать их на проверку, если тесты прошли:

```
pyneng 1-2 -c
```

При добавлении ``-c`` pyneng делает git add файлам заданий, которые прошли тесты, делает commit,
и git push. После этого пишет комментарий на github, что задания такие-то сданы на проверку.
 