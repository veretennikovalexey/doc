# arx.md

## Прием заказов EDI

Диспетчерская (все заказы) - Обмен данными (прием заказов из XML) - Прием заказов EDI

```php
if !Import_Edi_r641('Orders')
  DoImpExp('10',,,105)
endif
```

## R641

Диспетчерская (все заказы) - Справочники - Настройки EDI обмена - Список EDI провайдеров

| Код | Наименование провайдера |
| --- | ----------------------- |
|  1  | Exite (E-COM, Docrobot) |
|  2  | Edisoft (Ediweb.com)    |
|  3  | Leradata                |
|  4  | CISLINK                 |
|  5  | Корус (СберКорус, Корус Консалтинг, esphere-ECOD) |
|  6  | Контур (Диадок)         |

## x:\Fabius\Temp\LogFiles\LOG_Import_Xml

```
>Fabius1.exe (запуск: 19.05.2025-9:48:05)  =>  Import_Edi_R641() (запуск: 19.05.2025-10:22:46)
User: (13) Yan   WorkPc: 5470568436 -> 001
   Время работы: 00:00:03 час:мин:сек (2,58сек.)
Config: r260kod=378, r641kod=6, r643kod=24, r644kod=6


378 Соединение c Ftp сервером (ftp://ftp-edi-01.kontur.ru)
  Прием файла  ftp://ftp-edi-01.kontur.ru:  /Inbox/RECADV_e0e8ede2-d1c6-576d-4240-d656631442fe.xml --> \\Titan-fabius\programm\Fabius\EDI_IMP\RECADV\RECADV_e0e8ede2-d1c6-576d-4240-d656631442fe.xml
    Файл успешно принят:  \\Titan-fabius\programm\Fabius\EDI_IMP\RECADV\RECADV_e0e8ede2-d1c6-576d-4240-d656631442fe.xml   в наличии на локальном сервере
      файл:  RECADV_e0e8ede2-d1c6-576d-4240-d656631442fe.xml   удален c ftp сервера ftp://ftp-edi-01.kontur.ru
```

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 105 | Прием заказов(EDI обмен) «КОРУС Консалтинг» |
| 378 | Прием подтв.приемки Recadv (EDI обмен)(Xml) |

## FTP сервер

`ftp://ftp-edi-01.kontur.ru`