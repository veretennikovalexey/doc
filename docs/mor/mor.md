# mor.md

## Заказы поступают с FTP сервера Kontur

`ftp://ftp-edi.kontur.ru`

Диспетчерская (все заказы) - Документы - Заказы торговли / ездки - Заказы за смену

R260 (377) Kontur 24.08.2025 19:43:29

\\\bkkmorshan\data\Fabius\EDI\Kontur

\Orders\ORDERS_0a446ca5-8106-11f0-84ee-d8cd988657a0.xml

## Планировщик заданий 

я Администратор - Настройки - Планировщик заданий

R215 План событий

| Код | Событие |
| --- | ------------ |
|  92 | Скачивание и обработка увед. о приемке EDI-RECADV. Универсальная схема по R641 |
|  93 | Скачивание и обработка заказов EDI-Orders. Универсальная схема по R641 |

## Скачивание и обработка заказов EDI-Orders. Универсальная схема по R641

```php
Import_Edi_r641('Orders',,{'*'},.t.)
```

## z:\FABIUS\Temp\LogFiles\LOG_Import_Xml

```log
>Fabius_service.exe (запуск: 25.08.2025-9:25:19)  =>  Import_Edi_R641() (запуск: 26.08.2025-7:25:20)
User: (100) Планировщик   WorkPc: 5699352197 -> 001   taskName:   taskNum: 0
   Выделено памяти: 70`922`306,  Свободно памяти: 21`731`116
   Время работы: 00:00:01 час:мин:сек (0,857сек.)
Config: r260kod=378, r641kod=6, r643kod=24, r644kod=7


378 Соединение c Ftp сервером (ftp://ftp-edi.kontur.ru)
  Прием файла  ftp://ftp-edi.kontur.ru:  /Inbox/RECADV_7c47d116-8232-11f0-9e54-1e78dd2e1a55.xml --> \\bkkmorshan\data\Fabius\EDI\Kontur\Recadv\RECADV_7c47d116-8232-11f0-9e54-1e78dd2e1a55.xml
    Файл успешно принят:  \\bkkmorshan\data\Fabius\EDI\Kontur\Recadv\RECADV_7c47d116-8232-11f0-9e54-1e78dd2e1a55.xml   в наличии на локальном сервере
      файл:  RECADV_7c47d116-8232-11f0-9e54-1e78dd2e1a55.xml   удален c ftp сервера ftp://ftp-edi.kontur.ru
```

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 378 | Прием подтв.приемки Recadv (EDI обмен)(Xml) |
