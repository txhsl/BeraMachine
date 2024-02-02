﻿
# 🐻 BeraMachine

## Общая информация

Софт для отработки тестнета Berachain. Все настройки простые и понятные, ничего лишнего.
> Путь осилит идущий, а софт осилит любой деген🕵️

## Основные особенности 

* **Поддержка прокси (включая мобильные)**
* **Плотнейшее логирование, даже ваш чих залогируется**
* **Сохранение процесса для аккаунтов**
* **Повторитель (при ошибках в модулях)**
* **Сбор не отработавших кошельков**
* **Сохранение логов в файлы по дням**
* **Параллельный запуск**
* **Асинхронный ООП код**
* **EIP-1559**

## 🧩Модули

    1.  Faucet       (получение токенов с крана)                                       
    2.  BEX          (свапы $BERA в $STGUSDC, $BTC, ликвидность в пулл $BERA/$STGUSDC)
    3.  Honey        (минт $HONEY за $STGUSDC)    
    4.  Galxe        (выполнение дейлика на 5 поинтов за посещение Faucet)

## ♾️Основные функции

1.  **🚀Запуск прогона всех аккаунтов по подготовленным классическим маршрутам**

    После генерации маршрута (Пункт #3 функций), софт запустит выполнение маршрутов для всех аккаунтов.

2.  **📄Генерация классических роутов для каждого аккаунта**

    Классический генератор, работает по дедовской методике. Вам нужно указать списки модулей в настройке `CLASSIC_ROUTES_MODULES_USING` и при запуске этой функции софт соберет вам маршрут по этой настройке. Поддерживается 
    `None` как один из модулей в списке, при его попадании в маршрут, софт пропустит этот список.

3. **✅Проверка всех прокси на работоспособность**

    Быстрая проверка прокси(реально быстрая, как с цепи срывается)

## 📄Ввод своих данных

### Все нужные данные необходимо указать в таблицу `accounts_data` в папке `/data`. 
   1. **Name** - имена ваших аккаунтов, каждое название должно быть уникальным
   2. **Private Key** - приватные ключи от кошельков
   3. **Proxy** - прокси для каждого аккаунта. Если их будет меньше, софт будет брать их по кругу. Если прокси мобильные, то можно указать одну проксю.
   4. **Email address** - адрес почты для аккаунта.
   5. **Email password** - пароль от почты для аккаунта.

Вы можете установить пароль на вашу таблицу и включить настройку `EXCEL_PASSWORD = True`. При активации пароля, софт будет требовать его ввести для дальнейшей работы. Полезно при работе на сервере.

## ⚙️Настройка софта

Все настройки вынесены в файл `general_settings.py`.
Самые важные настройки продублирую здесь. 

1. Ключ `TWO_CAPTCHA_API_KEY`. Укажите ваш API ключ от **2captcha**. В файле есть ссылка на сайт, где это можно получить ключ
2. Настройка `EXCEL_PAGE_NAME`. Название листа в таблице Excel. 
3. В настройке `CLASSIC_ROUTES_MODULES_USING` указать маршрут для работы аккаунтов. 

## 🛠️Установка и запуск проекта

> Устанавливая проект, вы принимаете риски использования софта для добывания денег(потерять жопу, деньги, девственность).

Как только вы скачаете проект, **убедитесь**, что у вас Python 3.10.11

Установка проекта

```bash
  git clone https://github.com/realaskaer/BeraMachine.git
```

Для установки необходимых библиотек, пропишите в консоль

```bash
  pip install -r requirements.txt
```

Запуск проекта

```bash
  cd beramachine
  python main.py
```

## 🔗 Ссылки на установку Python и PyCharm

 - [Установка PyCharm](https://www.jetbrains.com/pycharm/download/?section=windows)
 - [Установка Python](https://www.python.org/downloads/windows/) (Вам нужна версия 3.10.11)

## ❔Куда писать свой вопрос?

- [@askaer.foundation](https://t.me/askaer) - мой канал в телеграм  
- [@askaer.chat](https://t.me/askaerchat) - ответы на любой вопрос
- [@askaer](https://t.me/realaskaer) - **при обнаружении бомбы в коде**  

## ❤️‍🔥Donate (Any EVM)

### `0x000000a679C2FB345dDEfbaE3c42beE92c0Fb7A5`
> Спасибо за поддержку❤️