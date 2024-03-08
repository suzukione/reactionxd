# TEA
Testnet https://app.tea.xyz/


## Требования от tea
Для успешного прохожения задания OSS необходимо создать два проекта.

У проектов должна быть минимум одна зависимость от других пакетов. А так же минимум ваш пакет должен быть зависим для других проектов

Поэтому будем создать минимум 3 пакета. Два из которых мы зарегистрируем на tea. Третий должен быть зависим от двух других


## Требования к установке
1. Иметь установленную версию python не ниже 3.6, скачать можно [тут](https://www.python.org/downloads/)

2. Нужно быть зарегистрированным на [pipy](https://pypi.org/account/register/), включить двухфакторку

3. Создать [токен](https://pypi.org/manage/account/token/) и дать доступ(scope) для всех проектов

4. Создать файл [pypirc](https://packaging.python.org/en/latest/specifications/pypirc/#using-a-pypi-token) и добавить в него созданных токен


## Установка
1. Импортируем проект на [github](https://github.com/new/import), в качестве клонируемого проекта указываем https://github.com/madest92/teaxyz, проект ОБЯЗАТЕЛЬНО должен быть public

2. Устанавливаем зависимости через pip
```
pip install -r requirements.txt
```

3. Редактируем файл setup.py

3.1. Заменяем **project_urls, url** на свою ссылку

3.2. ШАГ ТОЛЬКО для третьего проекта. Добавляем в зависимость свои пакеты в **install_requires**

4. Запускаем установку проекта
```
python setup.py sdist
twine upload dist/*
```

5. Повторить шаги по установке, должно быть 3 проекта
