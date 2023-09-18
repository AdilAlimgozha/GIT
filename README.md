# GIT Шпаргалка

Создание репозитория  
```bash
$git init
```  
1. Добавление на коммит одного или всех файлов  
```bash
$git add .

$git add --all

$git add
```  
2. Коммит файлов  
```bash
$git commit -m "message about changes"
```  
3. Создаем новый репозитория на Github   
4_1. Если нет SSH ключей:  
4_1_1. Создаем их  
```bash
$ ssh-keygen -t ed25519 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```  
или
```bash
$ ssh-keygen -t rsa -b 4096 -C "электронная почта, к которой привязан ваш аккаунт на GitHub"
```  
4_1_2. Где будут лежать ключи
```bash
> Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
```  
4_1_3. Кодовая фраза (оставить пустым)  
4_1_4. Чекнуть сгенерировались ли ключи
```bash
$ls -a ~/.ssh
```  
4_2. Связка SSH-ключа и GitHub-аккаунта  
4_2_1.
```bash
# скопировать содержимое ключа в буфер обмена:
$ clip < ~/.ssh/id_rsa.pub
# для ed25519:
$ clip < ~/.ssh/id_ed25519.pub
```  
4_2_2. Заходим в настройки аккаунта Github  
4_2_3. Нажимаем добавить SSH key  
4_2_4. В поле Title (англ. «заголовок») напишите название ключа. Например, Personal key (англ. «личный ключ»).  
4_2_5. В поле Key type (англ. «тип ключа») должно быть Authentication Key (англ. «ключ аутентификации»).  
4_2_6. В поле Key скопируйте ваш ключ из буфера обмена.  
4_2_7. Чек на правильность ключа  
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
4. Если SSH ключи есть:  
```bash
$git remote add origin 'Ссылка на репозиторий SSH или HTTPS'
```  
5. Чек на связку локального и удаленного  
```bash
$ git remote -v
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)
origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push) 
```  
6. Отпавляем файлы на удаленный репозиторий Github  
7_1. Если это первая отправка:  
```bash
$ git push -u origin main # Если команда приведёт к ошибке, попробуйте 
                          # заменить main на master.
```  
Флаг -u свяжет локальную ветку с одноимённой удалённой.  
7_2. Если не первая отправка:
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