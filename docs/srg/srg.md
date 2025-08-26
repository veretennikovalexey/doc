# srg.md

## \\\192.168.101.253\d$\fabius\regs\LogFiles\LOG_Import_Xml

```c
>Fabius_for_service.exe (запуск: 02.08.2025-1:00:04)  =>  Import_Edi_R641() (запуск: 02.08.2025-6:35:04)
User: (160) Планировщик   WorkPc: 3023686385 -> 001   taskName:   taskNum: 0
   Выделено памяти: 71`541`846,  Свободно памяти: 17`181`760
   Время работы: 00:00:03 час:мин:сек (3сек.)
Config: r260kod=283, r641kod=5, r643kod=5, r644kod=1


283 Соединение c Ftp сервером (ftp://ftp.esphere.ru)
  Прием файла  ftp://ftp.esphere.ru:  /P/outbound/ORDERS/3108472863_ORDERS_4607816029995_P.xml --> \\fabius\d$\fabius\EDI_Korus\IN\ORDERS\3108472863_ORDERS_4607816029995_P.xml
    Файл успешно принят:  \\fabius\d$\fabius\EDI_Korus\IN\ORDERS\3108472863_ORDERS_4607816029995_P.xml   в наличии на локальном сервере
      файл:  3108472863_ORDERS_4607816029995_P.xml   удален c ftp сервера ftp://ftp.esphere.ru
```

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 283 | Импорт заказов EDI Эдисофт, Корус |


## Корус ORDERS

\\\fabius\d$\fabius\EDI_Korus\IN\ORDERS

y:\Fabius\Edi_Korus\IN\ORDERS

3124019258_ORDERS_4607816029995_P.xml

[wiki.sftserv.ru/index.php/ORDERS](https://wiki.sftserv.ru/index.php/ORDERS) описание всех тегов по-русски

## Корус ORDRSP

y:\Fabius\Edi_Korus\Out\ORDRSP

