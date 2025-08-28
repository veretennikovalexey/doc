<<< **Контур EDI** [edi.kontur.ru](https://edi.kontur.ru/) **Контур EDI** >>>

# krl.md

## GUID

| Организация | GUID |
| ----------- | ---- |
| Монетка Элемент-Трейд      | 2BM-6674121179-2012052807492212777050000000000 |
| KRL                        | 2BM-5018167458-501801001-201501220135290988384 |
| Лента                      | 2BM-7814148471-2012052807203732341080000000000 |
| Глобус                     | 2BM-7743543761-2013021811033610374710000000000 |

Идентификатор участника ЭДО (GUID)

GUID (Globally Unique Identifier) — электронный уникальный идентификатор

В EDI под GUID подразумевается 

**Идентификатор участника электронного документооборота (ЭДО)**

## Документ ZAK

Диспетчерская (все заказы) - Документы - Заказы торговли / ездки - Заказы за смену

R260 (377) E-Com (Docrobot) 23.08.2025 12:49:26

\\\Fabius2020\BASE\FABIUS\Edi\Exite

\Orders\order_20250823124807_7fbb3208-c614-45a8-8af6-73d768a26866.xml

## \\\FABIUS2020\Logs\Kalin\LogFiles\LOG_Import_Xml

```java
>Fabius.exe (запуск: 25.08.2025-8:07:51)  =>  Import_Edi_R641() (запуск: 25.08.2025-13:20:38)
User: (407) Банцекина Н.В.   WorkPc: 5156714762 -> 001
   Время работы: 00:00:17 час:мин:сек (16,7сек.)
Config: r260kod=377, r641kod=1, r643kod=1, r644kod=2


377 Соединение c Ftp сервером (ftpex.e-vo.ru)
  Прием файла  ftpex.e-vo.ru:  /inbox/order_20250825132017_3c166b16-4d21-442e-afba-f0437efee972.xml --> \\Fabius2020\BASE\FABIUS\Edi\Exite\Orders\order_20250825132017_3c166b16-4d21-442e-afba-f0437efee972.xml
    Файл успешно принят:  \\Fabius2020\BASE\FABIUS\Edi\Exite\Orders\order_20250825132017_3c166b16-4d21-442e-afba-f0437efee972.xml   в наличии на локальном сервере
      файл:  /inbox/order_20250825132017_3c166b16-4d21-442e-afba-f0437efee972.xml   удален c ftp сервера ftpex.e-vo.ru
```

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 377 | Прием заказов (EDI обмен) (Xml/Excel/...) |


## Документ ZER

Диспетчерская (все заказы) - Документы - Заказы торговли / ездки - Ошибки и отказы при автоматическом приеме заказов торговли - Ошибки в заказах за месяц

## Exite

| Тип | Путь |
| --- | ---- |
| ORDERS | s:\Base\Fabius\Edi\Exite\Orders |
| ORDRSP | s:\Base\Fabius\Edi\Exite\Ordrsp |
| DESADV | s:\Base\Fabius\Edi\Exite\Desadv |
| RECADV | s:\Base\Fabius\Edi\Exite\Recadv |
| ON_NSCHFDOPPR | s:\Base\Fabius\Edi\Exite\Upd |
| ON_NKORSCHFDOPPR | s:\Base\Fabius\Edi\Exite\UKd | 

## Заказы поступают с FTP сервера Exite

```ftpex.e-vo.ru```
