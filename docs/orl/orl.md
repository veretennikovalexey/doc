# orl.md

Диспетчерская (все заказы) - Обмен данными (прием заказов из XML) - Прием заказов EDI

```php
if !Import_Edi_r641('Orders')
  DoImpExp('10',,,105)
endif
```

## Документ ZAK - PRIM Примечание

R260 (105) 19.08.2025 14:11:26

\\\hk-srv\export\Korus\ORDERS_c7712208-60c6-b2b5-bb9b-fb262c37b782.xml

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 105 | Прием заказов (EDI обмен) «КОРУС Консалтинг» |

## Корус ORDERS

z:\Korus

```xml
<?xml version="1.0" encoding="utf-8"?>
<Document-Order>
  <Order-Header>
    <OrderNumber>ЦЗР-092256 255504</OrderNumber>
    <OrderDate>2025-07-14</OrderDate>
    <OrderTime>00:00</OrderTime>
    <ExpectedDeliveryDate>2025-07-20</ExpectedDeliveryDate>
    <ExpectedDeliveryTime>00:00</ExpectedDeliveryTime>
    <Currency>RUB</Currency>
    <DocumentFunctionCode>O</DocumentFunctionCode>
    <CreationDateTime>2025-07-14T10:06:47.563Z</CreationDateTime>
  </Order-Header>
  <Order-Parties>
    <Buyer>
      <ILN>4680015840004</ILN>
    </Buyer>
    <Seller>
      <ILN>4607042009990</ILN>
      <TaxID>5753003842</TaxID>
      <UtilizationRegisterNumber>575301001</UtilizationRegisterNumber>
      <CodeByBuyer>1284</CodeByBuyer>
      <Name>АО «Орловский хлебокомбинат»</Name>
    </Seller>
    <DeliveryPoint>
      <ILN>4680015845504</ILN>
      <LocationName>ООО "Европа" -"Европа - 55"</LocationName>
    </DeliveryPoint>
    <Invoicee>
      <ILN>4680015840004</ILN>
    </Invoicee>
  </Order-Parties>
  <Order-Lines>
    <Line>
      <Line-Item>
        <LineNumber>1</LineNumber>
        <EAN>4607042004780</EAN>
        <BuyerItemCode>805568</BuyerItemCode>
        <ItemDescription>СУШКИ ЧАЙНЫЕ 250Г ОРЛОВСКИЙ ХЛЕБОКОМБИНАТ</ItemDescription>
        <OrderedQuantity>15.000</OrderedQuantity>
        <UnitOfMeasure>PCE</UnitOfMeasure>
        <OrderedUnitGrossPrice>46.6000</OrderedUnitGrossPrice>
        <GrossAmount>699.0000</GrossAmount>
        <TaxRate>10</TaxRate>
      </Line-Item>
    </Line>
  </Order-Lines>
  <Order-Summary>
    <TotalLines>1</TotalLines>
    <TotalOrderedAmount>15.000</TotalOrderedAmount>
    <TotalGrossAmount>699.00</TotalGrossAmount>
  </Order-Summary>
</Document-Order>
```




