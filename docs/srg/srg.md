# srg.md

## Корус ORDERS

* Заказ R260->KOD **283** Импорт заказов EDI Эдисофт, Корус

\\\fabius\d$\fabius\EDI_Korus\IN\ORDERS

y:\Fabius\Edi_Korus\IN\ORDERS

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

## Корус ORDRSP

y:\Fabius\Edi_Korus\Out\ORDRSP

```xml
<?xml version="1.0" encoding="WINDOWS-1251"?>
	<Document-OrderResponse>
		<OrderResponse-Header>
			<OrderResponseNumber>10929</OrderResponseNumber>
			<OrderResponseDate>2025-08-20</OrderResponseDate>
			<ExpectedDeliveryDate>2025-08-20</ExpectedDeliveryDate>
			<ExpectedDeliveryTime>12:40</ExpectedDeliveryTime>
			<OrderNumber />
			<OrderDate>2025-08-20</OrderDate>
			<ResponseType>29</ResponseType>
		</OrderResponse-Header>
		<OrderResponse-Parties>
			<Buyer>
				<ILN />
			</Buyer>
			<Seller>
				<ILN>4607816029995</ILN>
			</Seller>
			<DeliveryPoint>
				<ILN />
			</DeliveryPoint>
		</OrderResponse-Parties>
		<OrderResponse-Lines>
			<Line>
				<Line-Item>
					<LineNumber>1</LineNumber>
					<EAN />
					<LineItemStatus>5</LineItemStatus>
					<BuyerItemCode>1520</BuyerItemCode>
					<SupplierItemCode>1520</SupplierItemCode>
					<ItemDescription>Хлеб пшен.из муки высшего сорта форм.(0,5)</ItemDescription>
					<OrderedQuantity>21.000</OrderedQuantity>
					<QuantityToBeDelivered>21.000</QuantityToBeDelivered>
					<UnitPacksizeToBeDelivered>16.000</UnitPacksizeToBeDelivered>
					<UnitOfMeasure>PCE</UnitOfMeasure>
					<Currency>RUB</Currency>
					<OrderedUnitNetPrice>45.18</OrderedUnitNetPrice>
					<OrderedUnitGrossPrice>49.70</OrderedUnitGrossPrice>
					<TaxRate>10</TaxRate>
					<NetAmount>948.82</NetAmount>
					<GrossAmount>1043.70</GrossAmount>
					<TaxAmount>94.88</TaxAmount>
				</Line-Item>
			</Line>
			<Line>
				<Line-Item>
					<LineNumber>2</LineNumber>
					<EAN />
					<LineItemStatus>5</LineItemStatus>
					<BuyerItemCode>42</BuyerItemCode>
					<SupplierItemCode>42</SupplierItemCode>
					<ItemDescription>Хлеб "Прибрежный" (0,3)</ItemDescription>
					<OrderedQuantity>17.000</OrderedQuantity>
					<QuantityToBeDelivered>17.000</QuantityToBeDelivered>
					<UnitPacksizeToBeDelivered>24.000</UnitPacksizeToBeDelivered>
					<UnitOfMeasure>PCE</UnitOfMeasure>
					<Currency>RUB</Currency>
					<OrderedUnitNetPrice>36.59</OrderedUnitNetPrice>
					<OrderedUnitGrossPrice>40.25</OrderedUnitGrossPrice>
					<TaxRate>10</TaxRate>
					<NetAmount>622.05</NetAmount>
					<GrossAmount>684.25</GrossAmount>
					<TaxAmount>62.20</TaxAmount>
				</Line-Item>
			</Line>
		</OrderResponse-Lines>
		<OrderResponse-Summary>
			<TotalLines>2</TotalLines>
			<TotalNetAmount>1570.87</TotalNetAmount>
			<TotalGrossAmount>1727.95</TotalGrossAmount>
			<TotalTaxAmount>157.08</TotalTaxAmount>
		</OrderResponse-Summary>
	</Document-OrderResponse>
```