# wb_possition_telegram_bot
## Тестовое задание
Создать Телеграм-бота, который показывает на каком месте товар находится в поисковой выдаче по определенному поисковому запросу. Иными словами, вы пишите в поисковой строке Платье и артикул (идентификатор товара) - 87989388 находится, например на 10 странице на 12 месте. Бот должен это показать. Показывать место любого заданного артикула по любому заданному поисковому запросу. (до 50 страниц в поисковой выдаче).

**Описание:**
В данной работе происходит поиск позиции определенной карточки на веб-странице. Он перебирает элементы на странице, сравнивает их атрибут data-nm-id с заданным идентификатором. Когда нужная карточка найдена, код возвращает номер страницы, позицию карточки на странице и её абсолютную позицию на всей странице. После обработки всех элементов на текущей странице, код переходит к следующей странице для продолжения поиска.

Изначально в тз задания просили реализовать через официальный api wildberries (openapi.wildberries.ru), но для получения API-ключа необходимо быть продавцом на площадке. Поэтому было принятно решение реализации данной задачи, через библиотеку **Selenium**, так как страница WB является динамической. Также использовались библиотеки **Asyncio**, **Aiohttp** для реализации асинхронного выполения запросов. Асинхронность используется для выполнения операций, которые могут блокировать поток выполнения, таких как загрузка веб-страницы с помощью веб-драйвера Chrome и ожидание результата. Реализация telegram_bot осуществлялась при помощи библиотеки **telebot**, поддерживающая ассинхронность.

## Использование 

 1. /start - показать описание и инструкцию
 2. Поиск. "Поисковый запрос 'Артикул'". Например: "маска для волос 151623766". Если запрос валиден, то он поступает в обработку.


