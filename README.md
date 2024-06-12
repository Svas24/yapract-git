# Шпаргалка по материала Яндекс-практикума "Основы работы с GIT"
[Основы работы с GIT](https://practicum.yandex.ru/git-basics/?from=catalog)

---

### Rомманды git. Работа с репозиторием

_Инициализация_ git в рабочей папке проекта:

```BUSH
$ git init
```
выполняется в рабочем каталоге проекта


_Разинициализировать_: 
так как вся информация хранится в скрытом подкаталоге .git

```BUSH
$ rm -rf .git
```


Проверить _состояние_: 

```BUSH
$ git status
```


_Добавить фаqл_ в репозиторий 

```BUSH
$ git add todo.txt 
```

```BUSH
$ git add --all
```

Сохранить состояние проекта _Закоммитить_:

```BUSH
$ git commit -m "Описание"
```


Посмотреть _историю_:

```BUSH
$ git log
```


Посмотреть _состояние_:
 
```BUSH
$ git status
```


### Удаленный репозиторий 
[Github](https://github.com/) 

По умолчанию пары ключей хранятся ввиде файлов в каталоге ~/.ssh/



Использование ssh-keygen для _генерации_ ключей 

```BUSH
$ ssh-keygen -t ed25519 -C "user@email.com" 
```
_Для GitHub используется адрес электронной почты аккаунта_
Можно указать кодовую фразу для доступа к ключам. Или оставить без нее.


_Привязка_ ключа к GitHub. 

(приватным ключем ни с кем ни когда не делимся!)
содержимое файла с публичным ключем добавляем в 
Github -> "аккаунт" -> "Setting" -> "SSH and PGP keys" -> "New SSH key" 

Key type должно быть Authentication Key



_Проверить_ правильность ключа:

```BUSH
$ ssh -T git@github.com 
```
[Видеоинструкция](https://code.s3.yandex.net/git_Basic/SSH_Screencast.mp4) по генерации и привязке ключей 



_Связывание_ локального репозитория с удаленным. 

1. Перейти на страницу удаленного репозитория, выбрать "SSH", скопировать URL адрес репозитория

2. перейти в папку проекта, выполнить связывание коммандой: 

```BUSH
$ git remote add repository_NAME repository_URL 
```
repository_NAME - имя удаленного репозитория (обычно origin)
repository_URL git@github.com:%GIT_ACCOUNT_NAME%/%REPOSITORY_NAME%.git - скопированный URL репозитория  

3. ПРоверить что репозитории связанны 

```BUSH 
$ git remote -v
```

4. Отправить изменения в удаленный репозиторий - __push__

```BUSH
$ git push -u origin master
```

### Разметка README.md (маркдаун)

[шпаркалка на Github](https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c)


