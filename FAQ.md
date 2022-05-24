# FAQ

## Common questions

* Почему я не могу найти свои символы в _Symbol Search_?
* Символы EOD-данных в _Symbol Search_ не отображаются в подсказке. Введите в строке поиска полное название символа (`prefix:symbol_name`). Нажмите Ввод — график символа появится на _Чарте_.

* Что за вырожденный бар?
* Вырожденным баром мы называем график при таких данных: `open = close = high = low`, и `volume=0`

* А если свечами нарисовать график, будет информативно?
* Гораздо информативнее. Для этого они и нужны. Прирост — зелёный, падение — красное. Разница между `high` и `low` видна сразу.

* Как показать `open`, `close`, `high`, `low` на Чарте? А `volume`?
* Их можно включить/выключить в контекстном меню символа (в верхнем левом углу _Чарта_).

## GitHub settings

* А что лежит в репозитории? Что за скрипты и файлы?
* А там в разделе про GitHub всё написано?

* А что со вторым репозиторием?
* Pull Request c изменениями, затрагивающими что-то кроме файлов данные не будет принят. Вторая репа позволит настроить автоматическую загрузку, проверку и форматирование данных.

* Как забирать данные из приватного хранилища?
* В форкнутой репе — никак. Настроить доступ через переменные окружения во второй репе.

# Data requirements

* Где брать данные?
* ❓

* В каком виде хранить данные?
* Сами данные о ценах — в CSV-файлах: отдельный файл для каждого символа. Дополнительная информация о символах — в JSON-файле в каталоге _symbol_info_.

* Как прописать ключи доступ к хранилищу в переменных GitHub и использовать их в коде?
* В настройках репозитория создаём переменную в разделе _Secrets_, в неё пишем токен или пароль. А после — используем эту переменную в публичном коде.

* Можно интегрировать только биржевые данные?
* Платформа TradingView — удобный инструмент для работы с торговыми данными. Но, если можно интегрировать одноплотовые данные, например экономические показатели.

* Как часто обновляются данные?
* Ваши данные-на-конец-дня проверяются и загружаются в наше хранилище раз в сутки. На Чарте вы увидите данные за предыдущий день. Если данные нужно обновлять чаще, используйте REST-фид.

* Зачем регулярно обновлять данные?
* TradingView позволяет посмотреть и проанализировать данные за любой период. Если данные не обновлять, они перестают приносить пользу.

* Что будет с заброшенными данными?
* Нам не хочется держать данные, которые больше не нужны. Такие фиды мы будет отключать через три месяца?

* Почему мы предпочитаем публичные репозитории с данными?
* Нам нравится опенсорс. Благодаря этому наши инструменты помогают многим людям. Но если вы хотите подключить приватные данные — хорошо.