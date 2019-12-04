# Git. README.md

# NeuroStartUp

NeuroStartUp - динамически развивающийся стартап, специализирующийся на поиске с использованием новейших технологий искусственного интеллекта.

## Начало работы

При создании репозитория на Github есть возможность склонировать его в репозиторий вашего ПК.

### На странице вновь созданного репозитария GITHUB: 
  * Во вкладке <>Code:
     * В блоке Quick setup, из окна HTTPS скопировать URL проекта.
### На локальном ПК:
  1. Создаем папку с проектом.
  1. Запускаем Git (перед этим скачав и установив его с официального сайта git), а именно Git Bash.
  1. В открывшемся окне командами cd перемещаемся в папку, которую создали в пункте 1
  1. Выполняем в командной строке (в окне git'а) следующий набор команд:
   
    ``` 
    1. git config --global user.name "Ваше имя"
    2. git config --global user.email [Ваш емаил]
    3. git config --global core.editor NANO
    
    ```
#### Выше указанные команды выполняются только один раз на протяжение всей работы с GIT'ом.
  Далее, продолжаем выполнять команды:
  
    ``` 
    4. git clone [URL проекта из GITHUB]    клонируем репозиторий с GITHUB на локальный ПК
    5. cd [имя папки с проектом]    переходим в склонированную директорию  
    6. git remote -v    проверяем привязку локального репозитория с удаленным репозиторием GITHUB'а
    
    ```
#### При выполнение команды №6 в командной строке должно отобразиться:
  ``` 
  origin [URL проекта из GITHUB] (fetch)
  origin [URL проекта из GITHUB] (push) 
  ```
#### Теперь можно в папку проекта на локальном пк добавлять файлы и папки.
#### Помещаем файлы под VCS-отслеживание командой (git add)
  ``` 
  git add [имя файла] добавляет только выбранный файл
  git add *   добавляет все файлы и папки из директории проекта
  ```
#### Фиксируем (коммитим) изменения (git commit)
  ``` 
  git commit -m "Вводим комментарий"  
  ```
#### Заливаем (пушим) их на удалённое хранилище (git push)
  ``` 
  git push -u origin master    в последующих командах push флаг -u origin master неиспользуется.
  ```
#### Вводим логин и пароль аккаунта GITHUB'а
#### Все готово, теперь копия проекта с комитом в удаленном репозитории GITHUB'а. 

### Prerequisites

#### Нужно установить на ПК для использования Git: (https://git-scm.com/downloads) и любой интернет браузер.
```
Загрузите установщик с официального сайта https://git-scm.com/downloads. Загрузка начнется автоматически.
```
### Установка и запуск
Пошаговый процесс установки и запуска
#### Запустите на исполнение загруженный файл. Дождитесь появления экрана установки.
#### Git Setup
Укажите путь до каталога в который будет установлен Git.

#### Select Destination Location
Чтобы на рабочем столе была иконка Git, на следующем шаге отметьте галочкой “On the Desktop”.

#### Select Components
Введите имя директории, которая будет создана в Start Menu. При необходимости можно изменить путь с помощью кнопки Browse.

#### Select Start Menu Folder
Выберете способ использования из командной строки:
Use Git from Git Bash only - использование только из командной строки Bash.
Use Git from the Windows Command Prompt - использование командной строки Bash, а также минимальный набор команд Git из консоли Windows.
Use Git and optional Unix tools from the Windows Command Prompt - использование Git и утилит Unix из командной строки Windows, в этом случае будут перезаписаны некоторые утилиты Windows, например find и sort.

#### Adjusting your PATH environment
Выберете библиотеку, которая будет использована при подключении по протоколу HTTPS:
OpenSSL - сертификаты сервера будут проверяться с использованием Unix-файла ca-bundle.crt.
Windows Secure Channel - сертификаты сервера будут проверяться с использованием стандартной библиотеки Windows.

#### Choosing HTTPS transport backend
Убедитесь, что вы выбрали способ обработки окончания строк «Checkout Windows-style, commit Unix-style line endings». Это значение гарантирует, что Git преобразует LF в CRLF при проверке текстовых файлов. При выполнении текстовых файлов CRLF также преобразуется в LF. Это мера совместимости для защиты новых строк в текстовых файлах, что позволяет легко работать с текстовыми файлами в Windows и на платформах Unix.
Примечание: LF и CRLF - управляющий символ для переноса строки в Unix и Windows соответственно.
Configuration the line ending conversions

#### Далее необходимо сконфигурировать используемый терминал:
MinTTY - терминал Unix;
Windows - стандартный терминал Windows.
Configuring the terminal emulator to use with Git Bash
Отметьте галочками нужные вам дополнительные функции:
File system caching - кэширование файловой системы.
Git Credential Manager - включить менеджер учетных данных.
Symbolic links - разрешить символьные ссылки.
Нажмите кнопку Install.
Configuring the terminal emulator to use with Git Bash
Начнется процесс установки.
Configuring extra options

#### Подключение к удаленному репозиторию
Откройте каталог с файлами, которые необходимо отслеживать в системе контроля версий и выложить на GitHub. В пустую часть каталога нажмите правой кнопкой мыши и выберете Git Bash Here.

#### Git Bash Here
Перед вами откроется приглашение командной строки в зависимости от настроек.

#### Консоль
Для настройки необходимо указать ваше имя и электронную почту:
  ```
  git config --global user.email "you@example.com"
  git config --global user.name "Ваше имя"
  ```
Для того чтобы начать отслеживать содержимое папки в системе, выполните команды:
  ``` 
  git init
  git add
  ```
Выполните первый коммит:
  ```
  git commit -m "Init"
  ```
Чтобы добавить изменения, например, на github выполните действие:
  ```
  git remote add origin https://github.com/пользователь/репозиторий.git
  git push -u origin master
  ```
Перед вами откроется окно входа (консольное или стандартное окно Windows). В качестве пользователя укажите ваш логин на GitHub, репозиторий - название существующего репозитория.

## Лицензия

Опишите условия лицензии.