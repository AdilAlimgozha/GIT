# GIT Шпаргалка

Создание репозитория  
```bash
$git init
```  
Добавление на коммит одного или всех файлов  
```bash
$git add .

$git add --all

$git add
```  
Коммит файлов  
```bash
$git commit -m "message about changes"
```  
Создаем нового репозитория на Github   
Если нет SSH ключей:  
Создаем их  
```bash
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```  
или
```bash
$ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```  
Где будут ледать ключи
```bash
> Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
```  
Кодовая фраза (оставить пустым)  
Чекнуть сгенерировались ли ключи
```bash
$ls -a ~/.ssh
```  
Связка SSH-ключа и GitHub-аккаунта  
```bash
# скопировать содержимое ключа в буфер обмена:
$ clip < ~/.ssh/id_rsa.pub
# для ed25519:
$ clip < ~/.ssh/id_ed25519.pub
```  
Заходим в настройки аккаунта Github  
Нажимаем добавить SSH key  
В поле Title (англ. «заголовок») напишите название ключа. Например, Personal key (англ. «личный ключ»).  
В поле Key type (англ. «тип ключа») должно быть Authentication Key (англ. «ключ аутентификации»).  
В поле Key скопируйте ваш ключ из буфера обмена.  
Чек на правильность ключа  
```bash
$ ssh -T git@github.com
```  
Если это первый раз, когда вы используете Git, чтобы поделиться проектом на GitHub, появится похожее предупреждение.  
```bash
The authenticity of host 'github.com (140.82.121.4)' can't be established. ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU. This key is not known by any other names. Are you sure you want to continue connecting (yes/no/[fingerprint])?
```  
yes
```bash
Hi %ВАШ_АККАУНТ%! You've successfully authenticated, but GitHub does not provide shell access.
```  
Если SSH ключи есть:  
```bash
$git remote add origin 'Ссылка на репозиторий SSH или HTTPS'
```  
Чек на связку локального и удаленного  
```bash
$ git remote -v
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push) 
```  
Отпавляем файлы на удаленный репозиторий Github  
Если это первая отправка:  
```bash
$ git push -u origin main # Если команда приведёт к ошибке, попробуйте 
                          # заменить main на master.
``` Флаг -u свяжет локальную ветку с одноимённой удалённой.  
Если не первая отправка:
```bash
$ git push
```




Возможности GIT
История коммитов
```bash
$git log
```
Чтобы папка перестала быть репозиторием
```bash
$rm -rf .git
```