# Телеграм-бот: поиск отелей и ресторанов
## Описание бота

Разработанный телеграм-бот позволяет пользователю производить поиск
отелей и ресторанов в большинстве городов мира! 

Вся информация, которая будет выводиться пользователю в чат берется
исключительно с сайта [tripadvisor](https://www.tripadvisor.ru/).

## Установка

1) Сначала вам понадобиться token бота. Если у вас его нет, то нужно
его получить у [BotFather](https://telegram.me/BotFather).
2) На сайте [rapidapi](https://rapidapi.com/hub) необходимо 
зарегистрировать новый аккаунт (или войти в существующий) и 
вбить в поисковую строку `Travel Advisor`. Затем нажимаете на вкладку
`Pricing` и выбираете тот план, который подходит для вас.
3) Для того, чтобы узнать свой API-ключ, вам необходимо нажат на вкладку
`Apps`, что слева от вашего профиля, затем `My Apps` и иконку щита с галочкой
под надписью `Authorization`.
4) В файл [.env.template](.env.template) ваv необходимо будет вставить токен,
полученный вами от BotFather, а также API-ключ.

## Функционал

- ### Команда `/start`
Для запуска бота в первый раз следует использовать данную команду.

- ### Команда `/help`
При вводе данной команды пользователю высвечиваются 
все команды, которые поддерживает бот.

- ### Команда `/low`
Данная команда отвечает за вывод результатов поиска,
ссылаясь на данные, указанные пользователем. В данной команде сортировка
производится по следующему правилу: если пользователь ищет `отель`, то
сортировка результатов происходит от минимальной к максимальной цене;
если `ресторан`, то по дешевой кухне ($).

- ### Команда `/high`
Аналогична команде `/low` с 1 исключением: `отели` сортируются
по популярности, `рестораны` по высокой кухне (`$$$$`).

- ### Команда `/custom`
Если в командах выше уже были включены определенные
правила для сортировки результатов, то в этой пользователь сам
решает, по каким критериям будет проходить сортировка результатов.

- ### Команда `/history`
Данная команда отвечает за вывод истории запросов пользователя 
(последние 10 запросов).

## Дополнительный функционал

- ### Команда `/hello_world`
При вводе данной команды бот поздоровается с миром :)

- ### Функция `echo`
Если пользователь введет слово или фразу вне выполнения какой-либо
команды, ему вернется его же сообщение.