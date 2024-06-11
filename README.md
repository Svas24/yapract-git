### git

#### Инициализация 
git init

разинициализировать: 
rm -rf .git

проверить состояние: 
git status

#### Добавить фал в репозиторий 
git add todo.txt 
или 
git add --all

#### Коммит

git commit -m "Описание"

#### История 

git log




### Удаленный репозиторий

#### Провернка наличия SSH-ключа
Проверить наличие ключей
По умолчанию пары ключей хранятся ввиде файлов в каталоге 
```BUSH
$ dc ~/.ssh/
```
Для генерации ключей можно использовать программу 
```BUSH
$ ssh-keygen -t ed25519 -C "user@email.com" 
```
_Для GitHub используется адрес электронной почты аккаунта_

Можно указать кодовую фразу для доступа к ключам. Или оставить без нее.

#### Привязка ключа к GitHub. 
_приватным ключем ни с кем не делимся_
содержимое файла с публичным ключем добавляем в 
Github -> _аккаунт_ -> Setting -> SSH and PGP keys -> New SSH key 
Key type = Authentication Key

Проверить правильность ключа:
```BUSH
$ ssh -T git@github.com 
```
[Видеоинструкция](https://code.s3.yandex.net/git_Basic/SSH_Screencast.mp4) по генерации и привязке ключей 

#### Связывание локального репозитория с удаленным. 

1. Перейти на страницу удаленного репозитория, вибрать SSH, скопировать URL

2. перейти в папку проекта, выполнить комманду 
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
