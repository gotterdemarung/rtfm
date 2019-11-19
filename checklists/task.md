# I. Must have

1. Все условия/требования в задаче выполнены.


# II. Easy mode

1. `null` нигде не возращается. В случае, если требуется вернуть значение, которого может не быть
   должен использоваться `Optional<?>`, если возвращается коллекция, то должна быть возвращена
   пустая коллекция
2. Форматирование кода соответствует гайдлайнам
3. Между компонентами бизнес-логики пробрасываются только примитивы и интерфейсы
4. Статические методы не используются. Исключениями могут быть (в редких случаях) статические
   конструкторы. `import static` запрещен.
5. Созданые компоненты и объекты с данными являются немутабельными
6. Для объектов с данными присутствуют `equals` и `hashCode`, если они пробрасываются или 
   возвращаются в бизнес логику (другими словами - имплементят интерфейс).
7. Метод `hashCode` для объектов с данными, являющимися `IdReference` должен использовать только `id`
8. Исключения в `catch` блоке либо логируются либо пробрасываются. Но не одновременно
9. Поля объектов, хранящие временной промежуток (TTL, sleep intervals) должен быть реализован
   через `Duration`. В конструкторах допускатся использование скаляров с явным указанием размерности,
   например `ttSeconds`.
10. Для работы с датой и временем используется `UnixTimestamp`
11. Заявляются коллекции минимального уровня. Нет смысла объявлять `List<?>` там, где можно
    обойтись `Collection<?>`
12. Аргументы методов проверяются на корректность если они используются внутри методов. Для
    проверки на `null` рекоммендуется использовать `@NonNull`   



### III. Hard mode

1. Все созданные API, а также методы репозитариев не содержат `n+1` проблему. В первую очередь 
   относится к функционалу, обеспечивающему чтение, для модификаций это правило опционально.
2. Новые исключения добавлены в конвертер исключений в статус коды
3. Внутри сервисов проверяется scope и permissions
4. Отсутствуют race conditions (используются `atomic` в репозитариях, SLS в компонентах)
5. Для общих обвязок написаны unit-тесты.
6. Для внутренних новых API написаны интеграционные тесты (Oscar/Lua)
7. Для изменений схемы созданы миграции. Помимо миграций изменены соответствующие `.sql` файлы.
8. Присутствуют логи и метрики