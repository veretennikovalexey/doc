# srg.md

## Корус

* Заказ R260->KOD **283** Импорт заказов EDI Эдисофт, Корус

\\fabius\d$\fabius\EDI_Korus\IN\ORDERS\

y:\Fabius\Edi_Korus\IN\ORDERS\

3124019258_ORDERS_4607816029995_P.xml

[wiki.sftserv.ru/index.php/ORDERS](https://wiki.sftserv.ru/index.php/ORDERS) описание всех тегов по-русски

```xml
<Document-Order>
   <Order-Header>
      <OrderNumber>7605373549</OrderNumber>
      <OrderDate>2025-08-14</OrderDate>
      <ExpectedDeliveryDate>2025-08-15</ExpectedDeliveryDate>
      <ContractNumber>9999999999</ContractNumber>
      <CorrectionNumber>1</CorrectionNumber>
      <Currency>RUB</Currency>
      <DocumentFunctionCode>O</DocumentFunctionCode>
      <GeneralInformation/>
   </Order-Header>
   <Order-Parties>
      <Buyer>
         <ILN>4606038001260</ILN>
         <Name>ООО "АГРОТОРГ"</Name>
      </Buyer>
      <Seller>
         <ILN>4607816029995</ILN>
         <CodeByBuyer>7000068753</CodeByBuyer>
      </Seller>
      <DeliveryPoint>
         <ILN>4606038419300</ILN>
      </DeliveryPoint>
   </Order-Parties>
   <Order-Lines>
      <Line>
         <Line-Item>
            <LineNumber>1</LineNumber>
            <EAN>4607816020442</EAN>
            <BuyerItemCode>4386567</BuyerItemCode>
            <SupplierItemCode>1542</SupplierItemCode>
            <ItemDescription>СУРГУТ.ХЗ Тесто ДЛЯ ПИЦЦЫ дрож.охл.500г</ItemDescription>
            <OrderedQuantity>10</OrderedQuantity>
            <OrderedUnitPacksize>1.000</OrderedUnitPacksize>
            <UnitOfMeasure>PCE</UnitOfMeasure>
            <OrderedUnitNetPrice>43.68</OrderedUnitNetPrice>
            <OrderedUnitGrossPrice>48.05</OrderedUnitGrossPrice>
            <GrossAmount>480.48</GrossAmount>
            <TaxRate>10.0</TaxRate>
         </Line-Item>
      </Line>
   </Order-Lines>
   <Order-Summary>
      <TotalLines>1</TotalLines>
      <TotalOrderedAmount>10</TotalOrderedAmount>
      <TotalGrossAmount>480.48</TotalGrossAmount>
   </Order-Summary>
</Document-Order>
```