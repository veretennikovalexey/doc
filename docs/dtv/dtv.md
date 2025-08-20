# dtv.md

## Документ ZAK

Диспетчерская (все заказы) - Документы - Заказы торговли / ездки - Заказы за смену

Реквизит PRIM Примечание 1 _

Принято из EDI (из Xml (192) 19.08.2025 11:51:23)

## R260 Импорт/экспорт файлов

| Код | Наименование настройки |
| --- | ---------------------- |
| 192 | Прием заказов EDI (Контур) |

## Контур Заказ

z:\EDI Контур\Заказы\Принятые_01_07_2025

```xml
<?xml version="1.0" encoding="utf-8"?>
<eDIMessage id="4f1f8a26-e0de-427b-aa52-39f0f05e8a89">
  <interchangeHeader>
    <sender>4607164999995</sender>
    <recipient>4620000000235</recipient>
    <documentType>ORDERS</documentType>
    <creationDateTime>2025-07-01T19:31:59.532Z</creationDateTime>
  </interchangeHeader>
  <order number="320089P47192" date="2025-07-01">
    <contractIdentificator number="БрФ/61894/16" />
    <seller>
      <gln>4620000000235</gln>
      <organization>
        <name>АО "ДЯТЬКОВО-ХЛЕБ"</name>
        <inn>3202000249</inn>
        <kpp>324501001</kpp>
        <OKPOCode>00345093</OKPOCode>
      </organization>
      <russianAddress>
        <regionISOCode>RU-BRY</regionISOCode>
        <district>р-н Дятьковский</district>
        <city>Дятьково</city>
        <street>ул Крупской</street>
        <house>4</house>
        <postalCode>242603</postalCode>
      </russianAddress>
      <additionalIdentificator>3200000120</additionalIdentificator>
    </seller>
    <buyer>
      <gln>4607164999995</gln>
      <organization>
        <name>АО "Тандер"</name>
        <inn>2310031475</inn>
        <kpp>997350001</kpp>
      </organization>
      <russianAddress>
        <regionISOCode>RU-KDA</regionISOCode>
        <city>г. Краснодар</city>
        <street>ул. Им. Леваневского</street>
        <house>185</house>
        <postalCode>350002</postalCode>
      </russianAddress>
    </buyer>
    <invoicee>
      <gln>4607164999995</gln>
      <organization>
        <name>АО "Тандер"</name>
        <inn>2310031475</inn>
        <kpp>997350001</kpp>
      </organization>
      <russianAddress>
        <regionISOCode>RU-KDA</regionISOCode>
        <city>г. Краснодар</city>
        <street>ул. Им. Леваневского</street>
        <house>185</house>
        <postalCode>350002</postalCode>
      </russianAddress>
    </invoicee>
    <deliveryInfo>
      <requestedDeliveryDateTime>2025-07-02T00:00:00.000Z</requestedDeliveryDateTime>
      <shipTo>
        <gln>4680328057816</gln>
        <organization>
          <name>АО "Тандер" м-н Точность</name>
          <inn>2310031475</inn>
          <kpp>324545008</kpp>
        </organization>
        <russianAddress>
          <regionISOCode>RU-BRY</regionISOCode>
          <city>Сельцо г</city>
          <street>Куйбышева ул</street>
          <house>15</house>
          <postalCode>241550</postalCode>
        </russianAddress>
      </shipTo>
    </deliveryInfo>
    <lineItems>
      <currencyISOCode>RUB</currencyISOCode>
      <lineItem>
        <gtin>4603450930284</gtin>
        <internalBuyerCode>1000160844</internalBuyerCode>
        <description>Хлеб Мальцовский 580г п/уп(Дятьково-хлеб)</description>
        <requestedQuantity unitOfMeasure="PCE">2.000</requestedQuantity>
        <onePlaceQuantity unitOfMeasure="PCE">1.000</onePlaceQuantity>
        <netPrice>31.2000</netPrice>
        <netPriceWithVAT>34.3200</netPriceWithVAT>
        <vATRate>10</vATRate>
      </lineItem>
      <totalSumExcludingTaxes>62.40</totalSumExcludingTaxes>
    </lineItems>
  </order>
</eDIMessage>
```

## Контур Подтверждение заказа

z:\EDI Контур\Подтверждение заказов

```xml
<?xml version="1.0" encoding="UTF-8"?>
<eDIMessage id="169964" creationDateTime="2025-07-20T18:23:36">
	<!--идентификатор сообщения, время сообщения-->
	<!-- начало заголовка сообщения -->
	<interchangeHeader>
		<sender>4620000000235</sender>
		<!--GLN отправителя сообщения-->
		<recipient>4607081905543</recipient>
		<!--GLN получателя сообщения-->
		<documentType>ORDRSP</documentType>
		<isTest>0</isTest>
		<!--тестовый флаг-->
	</interchangeHeader>
	<orderResponse number="9881" date="2025-07-20" status="Accepted">
		<!--номер документа-респонса, дата документа-респонса, статус документа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
		<originOrder number="252908962365" date="2025-07-21"/>
		<!--номер заказа, дата заказа-->
		<blanketOrderIdentificator number=""/>
		<!--номер серии заказов-->
		<seller>
			<gln>4620000000235</gln>
			<!--gln поставщика-->
			<organization>
				<name>АО "ДЯТЬКОВО-ХЛЕБ"</name>
				<!--наименование поставщика для ЮЛ-->
				<inn>3202000249</inn>
				<!--ИНН поставщика для ЮЛ-->
				<kpp>324501001</kpp>
				<!--КПП поставщика только для ЮЛ-->
			</organization>
		</seller>
		<buyer>
			<gln>4607081905543</gln>
			<!--gln покупателя-->
			<organization>
				<name>АО "ДИКСИ Юг"</name>
				<!--наименование покупателя-->
				<inn>5036045205</inn>
				<!--ИНН покупателя для ЮЛ-->
				<kpp>503601001</kpp>
				<!--КПП покупателя только для ЮЛ-->
			</organization>
		</buyer>
		<deliveryInfo>
			<estimatedDeliveryDateTime>2025-07-21T12:00:00</estimatedDeliveryDateTime>
			<!--дата доставки-->
			<shipFrom>
				<gln>4620000000235</gln>
				<!--gln грузоотправителя-->
			</shipFrom>
			<shipTo>
				<gln>4640010204683</gln>
				<!--gln грузополучателя-->
			</shipTo>
		</deliveryInfo>
		<lineItems>
			<currencyISOCode>RUB</currencyISOCode>
			<!--код валюты (по умолчанию рубли)-->
			<lineItem status="Accepted">
				<!--статус подтверждения строки заказа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
				<gtin>4603450931199</gtin>
				<!--GTIN товара-->
				<internalBuyerCode>811</internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode>811</internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber>1</orderLineNumber>
				<!--порядковый номер товара-->
				<description>Хлеб "Мальцовский"(часть изделия) в упаковке</description>
				<!--название товара-->
				<confirmedQuantity unitOfMeasure="PCE">3.000</confirmedQuantity>
				<!--заказанное количество-->
				<netPrice>16.80</netPrice>
				<!--цена товара без НДС-->
				<netPriceWithVAT>18.48</netPriceWithVAT>
				<!--цена товара с НДС-->
				<netAmount>50.40</netAmount>
				<!--сумма по позиции без НДС-->
				<amount>55.44</amount>
				<!--сумма по позиции с НДС-->
			</lineItem>
			
			<!--сумма заявки без НДС-->
			<lineItem status="Accepted">
				<!--статус подтверждения строки заказа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
				<gtin>4603450930734</gtin>
				<!--GTIN товара-->
				<internalBuyerCode>540</internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode>540</internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber>2</orderLineNumber>
				<!--порядковый номер товара-->
				<description>Батон "Молодежный" в упаковке</description>
				<!--название товара-->
				<confirmedQuantity unitOfMeasure="PCE">7.000</confirmedQuantity>
				<!--заказанное количество-->
				<netPrice>31.08</netPrice>
				<!--цена товара без НДС-->
				<netPriceWithVAT>34.19</netPriceWithVAT>
				<!--цена товара с НДС-->
				<netAmount>217.56</netAmount>
				<!--сумма по позиции без НДС-->
				<amount>239.32</amount>
				<!--сумма по позиции с НДС-->
			</lineItem>
			<lineItem status="Accepted">
				<!--статус подтверждения строки заказа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
				<gtin>4603450931083</gtin>
				<!--GTIN товара-->
				<internalBuyerCode>669</internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode>669</internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber>3</orderLineNumber>
				<!--порядковый номер товара-->
				<description>Сдоба "Дятьковская" в упаковке</description>
				<!--название товара-->
				<confirmedQuantity unitOfMeasure="PCE">4.000</confirmedQuantity>
				<!--заказанное количество-->
				<netPrice>28.74</netPrice>
				<!--цена товара без НДС-->
				<netPriceWithVAT>31.62</netPriceWithVAT>
				<!--цена товара с НДС-->
				<netAmount>114.96</netAmount>
				<!--сумма по позиции без НДС-->
				<amount>126.46</amount>
				<!--сумма по позиции с НДС-->
			</lineItem>
			<lineItem status="Accepted">
				<!--статус подтверждения строки заказа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
				<gtin>4603450930284</gtin>
				<!--GTIN товара-->
				<internalBuyerCode>64</internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode>64</internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber>4</orderLineNumber>
				<!--порядковый номер товара-->
				<description>Хлеб "Мальцовский" в упаковке</description>
				<!--название товара-->
				<confirmedQuantity unitOfMeasure="PCE">12.000</confirmedQuantity>
				<!--заказанное количество-->
				<netPrice>31.20</netPrice>
				<!--цена товара без НДС-->
				<netPriceWithVAT>34.32</netPriceWithVAT>
				<!--цена товара с НДС-->
				<netAmount>374.40</netAmount>
				<!--сумма по позиции без НДС-->
				<amount>411.84</amount>
				<!--сумма по позиции с НДС-->
			</lineItem>
		</lineItems>
	</orderResponse>
</eDIMessage>
```

## Контур Уведомление об отгрузке

z:\EDI Контур\Уведомление об отгрузке

```xml
<?xml version="1.0" encoding="UTF-8"?>
<eDIMessage id="8312" creationDateTime="2025-01-03">
	<!--идентификатор сообщения, время сообщения-->
	<interchangeHeader>
		<sender>4620000000235</sender>
		<!--GLN отправителя сообщения-->
		<recipient>4607164999995</recipient>
		<!--GLN получателя сообщения-->
		<documentType>DESADV</documentType>
		<!--тип документа-->
		<isTest>1</isTest>
		<!--тестовый флаг-->
	</interchangeHeader>
	<despatchAdvice number="1030125106" date="2025-01-03">
		<!--номер накладной, дата накладной-->
		<originOrder number="320089P44540" date="0000-00-00"/>
		<!--номер заказа, дата заказа-->
		<blanketOrderIdentificator number=""/>
		<!--номер серии заказов-->
		<seller>
			<gln>4620000000235</gln>
			<!--gln поставщика-->
		</seller>
		<buyer>
			<gln>4607164999995</gln>
			<!--gln покупателя-->
		</buyer>
		<deliveryInfo>
			<estimatedDeliveryDateTime>2025-01-03T12:00:00</estimatedDeliveryDateTime>
			<!--дата доставки-->
			<shipTo>
				<gln>4680328057816</gln>
				<!--gln грузополучателя-->
			</shipTo>
			<transportation>
				<!--информация о машине-->
				<transportMode>roadTransport</transportMode>
				<!--режим перевозки: roadTransport (30) - автодорожный транспорт-->
				<vehicleNumber>М047РР32</vehicleNumber>
				<!--номер тарнспортного средства-->
				<vehicleBrand></vehicleBrand>
				<!--марка транспортного средства-->
				<nameOfCarrier>Новиков Андрей Юрьевич</nameOfCarrier>
				<!--имя водителя-->
			</transportation>
		</deliveryInfo>
		<lineItems>
			<currencyISOCode>RUB</currencyISOCode>
			<!--код валюты (по умолчанию рубли)-->
			<lineItem>
				<gtin>4603450930284</gtin>
				<!--GTIN товара-->
				<internalBuyerCode>64</internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode>64</internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber>1</orderLineNumber>
				<!--порядковый номер товара-->
				<description>Хлеб "Мальцовский" в упаковке</description>
				<!--название товара-->
				<despatchedQuantity unitOfMeasure="PCE">1.000</despatchedQuantity>
				<!--заказанное количество-->
				<netPrice>28.36</netPrice>
				<!--цена без НДС-->
				<netPriceWithVAT>31.20</netPriceWithVAT>
				<!--цена по позиции с НДС-->
				<netAmount>28.36</netAmount>
				<!--сумма по позиции без НДС-->
				<amount>31.20</amount>
				<!--сумма по позиции с НДС-->
				<vATRate>10</vATRate>
				<!--ставка НДС-->
				<vATAmount>2.84</vATAmount>
				<!--сумма НДС-->
			</lineItem>
			
			<!--сумма заявки без НДС-->
		</lineItems>
	</despatchAdvice>
</eDIMessage>
```

## Контур Акт приёмки

z:\EDI Контур\Акты приемки

```xml
<?xml version="1.0" encoding="utf-8"?>
<eDIMessage id="19e41255-b27a-4f47-837b-8405565e298a">
  <interchangeHeader>
    <sender>4607164999995</sender>
    <recipient>4620000000235</recipient>
    <documentType>RECADV</documentType>
    <creationDateTime>2025-01-04T08:21:09.140Z</creationDateTime>
  </interchangeHeader>
  <receivingAdvice number="88" date="2025-01-04">
    <originOrder number="320089P44544" date="2025-01-03" />
    <contractIdentificator number="БрФ/61894/16" />
    <despatchIdentificator number="88" />
    <seller>
      <gln>4620000000235</gln>
      <organization>
        <name>АО "ДЯТЬКОВО-ХЛЕБ"</name>
        <inn>3202000249</inn>
        <kpp>324501001</kpp>
        <OKPOCode>00345093</OKPOCode>
      </organization>
      <russianAddress>
        <regionISOCode>RU-BRY</regionISOCode>
        <district>р-н Дятьковский</district>
        <city>Дятьково</city>
        <street>ул Крупской</street>
        <house>4</house>
        <postalCode>242603</postalCode>
      </russianAddress>
    </seller>
    <buyer>
      <gln>4607164999995</gln>
      <organization>
        <name>АО "Тандер"</name>
        <inn>2310031475</inn>
        <kpp>997350001</kpp>
      </organization>
      <russianAddress>
        <regionISOCode>RU-KDA</regionISOCode>
        <city>г. Краснодар</city>
        <street>ул. Им. Леваневского</street>
        <house>185</house>
        <postalCode>350002</postalCode>
      </russianAddress>
    </buyer>
    <invoicee>
      <gln>4607164999995</gln>
      <organization>
        <name>АО "Тандер"</name>
        <inn>2310031475</inn>
        <kpp>997350001</kpp>
      </organization>
      <russianAddress>
        <regionISOCode>RU-KDA</regionISOCode>
        <city>г. Краснодар</city>
        <street>ул. Им. Леваневского</street>
        <house>185</house>
        <postalCode>350002</postalCode>
      </russianAddress>
    </invoicee>
    <deliveryInfo>
      <receptionDateTime>2025-01-04T00:00:00.000Z</receptionDateTime>
      <shipTo>
        <gln>4680328057816</gln>
        <organization>
          <name>АО "Тандер" м-н Точность</name>
          <inn>2310031475</inn>
          <kpp>324545008</kpp>
        </organization>
        <russianAddress>
          <regionISOCode>RU-BRY</regionISOCode>
          <city>Сельцо г</city>
          <street>Куйбышева ул</street>
          <house>15</house>
          <postalCode>241550</postalCode>
        </russianAddress>
      </shipTo>
    </deliveryInfo>
    <lineItems>
      <currencyISOCode>RUB</currencyISOCode>
      <lineItem>
        <gtin>4603450930284</gtin>
        <internalBuyerCode>1000160844</internalBuyerCode>
        <description>Хлеб Мальцовский 580г п/уп(Дятьково-хлеб)</description>
        <orderedQuantity unitOfMeasure="PCE">1.000</orderedQuantity>
        <despatchedQuantity unitOfMeasure="PCE">1.000</despatchedQuantity>
        <acceptedQuantity unitOfMeasure="PCE">1.000</acceptedQuantity>
        <onePlaceQuantity unitOfMeasure="PCE">1.000</onePlaceQuantity>
        <netPrice>28.3600</netPrice>
        <netPriceWithVAT>31.2000</netPriceWithVAT>
        <vATRate>10</vATRate>
      </lineItem>
    </lineItems>
  </receivingAdvice>
</eDIMessage>
```

## Контур УПД

z:\EDI Контур\УПД

```xml
<Document-Invoice>
	<Invoice-Header>
		<InvoiceNumber>6</InvoiceNumber>
		<InvoiceDate>2025-01-02</InvoiceDate>
		<InvoiceCurrency>RUB</InvoiceCurrency>
		<DocumentFunctionCode>O</DocumentFunctionCode>
		<MessageType>INVDOP</MessageType>
		<Documents>
			<DocumentDescription>Товары переданы</DocumentDescription>
			<Document>
				<DocumentNumber>6</DocumentNumber>
				<DocumentDate>2025-01-02</DocumentDate>
				<DocumentName>Документ</DocumentName>
			</Document>
		</Documents>
		<Order>
			<BuyerOrderNumber>717667P13568</BuyerOrderNumber>
			<BuyerOrderDate>2025-01-01</BuyerOrderDate>
		</Order>
		<Delivery>
			<DeliveryNoteNumber>         6</DeliveryNoteNumber>
			<DeliveryNoteDate>2025-01-02</DeliveryNoteDate>
			<DeliveryDate>2025-01-02</DeliveryDate>
			<ActualDeliveryDate>2025-01-02</ActualDeliveryDate>
			<ReceivingAdviceNumber></ReceivingAdviceNumber>
			<ReceivingAdviceDate></ReceivingAdviceDate>
		</Delivery>
	</Invoice-Header>
	<Invoice-Parties>
		<Buyer>
			<ILN>4607164999995</ILN>
		</Buyer>
		<Seller>
			<ILN>4620000000235</ILN>
			<TaxID>3202000249</TaxID>
			<UtilizationRegisterNumber>324501001</UtilizationRegisterNumber>
			<CodeByBuyer></CodeByBuyer>
			<Name>АО "ДЯТЬКОВО-ХЛЕБ"</Name>
			<ManagingPerson>Владимир Орлов</ManagingPerson>
			<ManagingPersonFather>Владимирович</ManagingPersonFather>
			<ContactFunction>Генеральный директор</ContactFunction>
			<InsuranceContact>5</InsuranceContact>
			<SupplierContact>1</SupplierContact>
			<AuthorityContact>Полномочия</AuthorityContact>
			<StreetAndNumber>Крупской ул, 4</StreetAndNumber>
			<CityName>Дятьковский р-н, Дятьково г</CityName>
			<ProvinceCode>32</ProvinceCode>
			<PostalCode>242603</PostalCode>
			<Country>RU</Country>
		</Seller>
		<DeliveryPoint>
			<ILN>4680328581229</ILN>
		</DeliveryPoint>
		<Consignor>
			<ILN>4620000000235</ILN>
		</Consignor>
	</Invoice-Parties>
	<Invoice-Lines>
		<Line>
			<Line-Item>
				<LineNumber>1</LineNumber>
				<OrderLineNumber>1</OrderLineNumber>
				<LineItemInformation>1</LineItemInformation>
				<EAN>4603450930284</EAN>
				<BuyerItemCode></BuyerItemCode>
				<SupplierItemCode>64</SupplierItemCode>
				<ItemDescription><![CDATA[Хлеб "Мальцовский" в упаковке]]></ItemDescription>
				<InvoiceQuantity>1.000</InvoiceQuantity>
				<UnitOfMeasure>PCE</UnitOfMeasure>
				<InvoiceUnitNetPrice>28.36</InvoiceUnitNetPrice>
				<OrderedUnitPacksize>1</OrderedUnitPacksize>
				<CountryOfOriginCode>RU</CountryOfOriginCode>
				<TaxRate>10.00</TaxRate>
				<TaxAmount>2.84</TaxAmount>
				<NetAmount>28.36</NetAmount>
				<GrossAmount>31.20</GrossAmount>
			</Line-Item>
		</Line>
	</Invoice-Lines>
	<Invoice-Summary>
		<TotalLines>1</TotalLines>
		<TotalNetAmount>28.36</TotalNetAmount>
		<TotalTaxableBasis>28.36</TotalTaxableBasis>
		<TotalTaxAmount>2.84</TotalTaxAmount>
		<TotalGrossAmount>31.20</TotalGrossAmount>
		<Tax-Summary>
			<Tax-Summary-Line>
				<TaxRate>10.00</TaxRate>
				<TaxName>процент</TaxName>
				<TaxAmount>2.84</TaxAmount>
				<TaxableBasis>28.36</TaxableBasis>
				<TaxableAmount>28.36</TaxableAmount>
				<GrossAmount>31.20</GrossAmount>
			</Tax-Summary-Line>
		</Tax-Summary>
	</Invoice-Summary>
</Document-Invoice>
```

## Контур УКД

z:\EDI Контур\УКД


