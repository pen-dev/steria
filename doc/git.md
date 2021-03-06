[Назад](README.md) | [Главная](../README.md)
---

Для разработки будем использовать `GitHub flow`.

## Литература

[GitHub Flow](https://habr.com/ru/post/346066/)
* обязательна к ознакомлению


## Разработка в git

Используется одна главная ветка - `master`. Код с этой ветки
 всегда в `production`, это значит что тут должен быть только
 работающий код.

### Используемые ветки

#### master

Главное правило:   
> всё, что находится в `master` —
> гарантированно стабильно и готово к деплою в любой момент.



### Когда делать `commit?`

> Создав ветвь, начинайте вносить в неё изменения.
> Добавляя, редактируя или удаляя файлы, не забывайте
> делать новые фиксации (commits) в ветви. Последовательность
> фиксаций образует в конечном счёте прозрачную историю работы
> над вашей задачей, по которой остальные смогут понять что вы
> делали и почему.

Если коротко - чем больше коммитов тем лучше. Особенно важно
 писать толковые комментарии к коммиту. Чтобы лучше понять качество
 комментария следует помнить что этот комментарий будет написан
 при просмотре строки кода, т.е. комментарий должен отвечать на
 вопрос `Зачем здесь эта строка?`.
 
[из статьи](https://habr.com/ru/company/softmart/blog/316686/)  
> Сообщение коммита должно описывать ваши намерения,
> а не пересказывать содержимое кода — его и так несложно
> посмотреть. Важно то, зачем вы сделали этот коммит.

Пример хорошего сообщения: «Скомбинировать шаблоны, чтобы разгрузить интерфейс пользователя».
 
Вот хороший плагин для git [gittoolbox](https://plugins.jetbrains.com/plugin/7499-gittoolbox)


### Когда делать `push`?
Лучше в конце рабочего дня. Не думаю что хранить ветки локально
 хорошая идея, так как можно легко потерять данные.


### Когда делать `merge requests`?

Pull request - другое название этому явлению

Если коротко то порядок такой:
 - Делаем себе ветку и разрабатываем в ней
 - Когда есть что показать (прототип задачи) - открываем мердж-реквест
 чтобы другие могли начать оценивать работу, делать замечания и тестировать.
 - По мере изменения в ветке нужно обновлять ее на сервере командой `push`
 - Когда ветка готова ее еще раз посмотрят и примут решение о слиянии
 
У нас будет обоюдное код ревью.

[Как его делать](https://docs.gitlab.com/ee/user/project/merge_requests/)   
[Gitlab flow](https://habr.com/ru/company/softmart/blog/316686/) -
 тут есть немного информации про работу с `merge-request`
 

### Работа с задачами  

[из статьи](https://habr.com/ru/company/softmart/blog/316686/)   
> В сообщении коммита, либо в описании мерж-реквеста можно
> упомянуть задачу по её номеру, используя слово-триггер,
> например: fixes \#14, closes \#67. При этом GitLab публикует
> в упомянутой задаче комментарий с обратной ссылкой на коммит
> или реквест. А в мерж-реквесте появляется список связанных
> задач. Когда вы замержите код в основную ветку, связанные
> задачи будут отмечены как выполненные. Обратите внимание:
> триггеры распознаются только на английском, то есть fixes
> \#14 сработает, а исправляет \#14 — нет.


Предлагаю попробовать для задач проекта использовать встроенные
 менеджер задач.

