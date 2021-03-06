[Назад](README.md) | [Главная](../README.md)
---

# Запуск через Docker 

### Сборка образа

```
docker build . -t steria:latest
```

### Запуск 

По умолчанию сервер будет запущен на `5000` порту. Чтобы поменять порт нужно прописать его в переменной окружения `PORT` и передать контейнеру.

#### Запуск на порте по умолчанию

```
docker run -it --rm -p 5000:5000 steria:latest
```

#### Пользовательский порт

Для примера будет 8000 порт.

```
docker run -it --rm -e PORT=8000 -p 8000:8000 steria:latest
```

### Запуск для динамической разработки

Во время разработки хочется чтобы сервер был запущен в `docker`, но при этом код динамически обновлялся. Т.е. сервер бы обновлялся без перезапуска контейнера. Для этого можно подмонтировать директорию с исходным кодом кодом в контейнер в момент его запуска: 

```
docker run -it --rm -v “$PWD/steriaserver”:/home/app/steriaserver -p 8000:5000 steria:latest
```

# Запуск через терминал 

Подключаем виртуальное окружение и выполняем в терминале: 

```
python steria.py
```


