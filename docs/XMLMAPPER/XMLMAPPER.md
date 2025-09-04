# XMLMAPPER.md

## KonturOrdrsp.xsd

```xml
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="eDIMessage" type="eDIMessageType"/>
  <xs:complexType name="eDIMessageType">
    <xs:sequence>
      <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
      <xs:element name="orderResponse" type="orderResponseType"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:string"/>
    <xs:attribute name="creationDateTime" type="xs:string"/>
  </xs:complexType>
  <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
  <xs:complexType name="interchangeHeaderType">
    <xs:sequence>
      <xs:element name="sender" type="senderType"/>
      <xs:element name="recipient" type="recipientType"/>
      <xs:element name="documentType" type="documentTypeType"/>
      <xs:element name="isTest" type="isTestType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="sender" type="senderType"/>
  <xs:simpleType name="senderType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="recipient" type="recipientType"/>
  <xs:simpleType name="recipientType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="documentType" type="documentTypeType"/>
  <xs:simpleType name="documentTypeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="isTest" type="isTestType"/>
  <xs:simpleType name="isTestType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderResponse" type="orderResponseType"/>
  <xs:complexType name="orderResponseType">
    <xs:sequence>
      <xs:element name="originOrder" type="originOrderType"/>
      <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
      <xs:element name="seller" type="sellerType"/>
      <xs:element name="buyer" type="buyerType"/>
      <xs:element name="deliveryInfo" type="deliveryInfoType"/>
      <xs:element name="lineItems" type="lineItemsType"/>
    </xs:sequence>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="originOrder" type="originOrderType"/>
  <xs:complexType name="originOrderType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
  </xs:complexType>
  <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
  <xs:complexType name="blanketOrderIdentificatorType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
  </xs:complexType>
  <xs:element name="seller" type="sellerType"/>
  <xs:complexType name="sellerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="name" type="nameType"/>
  <xs:simpleType name="nameType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="inn" type="innType"/>
  <xs:simpleType name="innType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="kpp" type="kppType"/>
  <xs:simpleType name="kppType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="buyer" type="buyerType"/>
  <xs:complexType name="buyerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="deliveryInfo" type="deliveryInfoType"/>
  <xs:complexType name="deliveryInfoType">
    <xs:sequence>
      <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
      <xs:element name="shipFrom" type="shipFromType"/>
      <xs:element name="shipTo" type="shipToType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
  <xs:simpleType name="estimatedDeliveryDateTimeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipFrom" type="shipFromType"/>
  <xs:complexType name="shipFromType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipTo" type="shipToType"/>
  <xs:complexType name="shipToType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItems" type="lineItemsType"/>
  <xs:complexType name="lineItemsType">
    <xs:sequence>
      <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
      <xs:element name="lineItem" type="lineItemType" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
  <xs:simpleType name="currencyISOCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItem" type="lineItemType"/>
  <xs:complexType name="lineItemType">
    <xs:sequence>
      <xs:element name="gtin" type="gtinType"/>
      <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
      <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
      <xs:element name="orderLineNumber" type="orderLineNumberType"/>
      <xs:element name="description" type="descriptionType"/>
      <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
      <xs:element name="orderedQuantity" type="orderedQuantityType"/>
      <xs:element name="netPrice" type="netPriceType"/>
      <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
      <xs:element name="netAmount" type="netAmountType"/>
      <xs:element name="amount" type="amountType"/>
    </xs:sequence>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="gtin" type="gtinType"/>
  <xs:simpleType name="gtinType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
  <xs:simpleType name="internalBuyerCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
  <xs:simpleType name="internalSupplierCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderLineNumber" type="orderLineNumberType"/>
  <xs:simpleType name="orderLineNumberType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="description" type="descriptionType"/>
  <xs:simpleType name="descriptionType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
  <xs:complexType name="confirmedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="orderedQuantity" type="orderedQuantityType"/>
  <xs:complexType name="orderedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="netPrice" type="netPriceType"/>
  <xs:simpleType name="netPriceType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
  <xs:simpleType name="netPriceWithVATType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netAmount" type="netAmountType"/>
  <xs:simpleType name="netAmountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="amount" type="amountType"/>
  <xs:simpleType name="amountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
  <xs:simpleType name="totalSumExcludingTaxesType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
</xs:schema>
```

## KonturOrdrspXmlToDp.xtr

```xml
<XmlTransformation Version="1.0"><Transform Direction="ToCds" DataEncoding="utf-8"><SelectEach dest="DATAPACKET\ROWDATA\ROW" from="\eDIMessage"><Select dest="@id" from="@id"/><Select dest="@creationDateTime" from="@creationDateTime"/><Select dest="@sender" from="\interchangeHeader\sender"/><Select dest="@recipient" from="\interchangeHeader\recipient"/><Select dest="@documentType" from="\interchangeHeader\documentType"/><Select dest="@isTest" from="\interchangeHeader\isTest"/><Select dest="@number1" from="\orderResponse@number"/><Select dest="@date1" from="\orderResponse@date"/><Select dest="@status" from="\orderResponse@status"/><Select dest="@number2" from="\orderResponse\originOrder@number"/><Select dest="@date2" from="\orderResponse\originOrder@date"/><Select dest="@number3" from="\orderResponse\blanketOrderIdentificator@number"/><Select dest="@seller_gln" from="\orderResponse\seller\gln"/><Select dest="@organization_name1" from="\orderResponse\seller\organization\name"/><Select dest="@organization_inn1" from="\orderResponse\seller\organization\inn"/><Select dest="@organization_kpp1" from="\orderResponse\seller\organization\kpp"/><Select dest="@buyer_gln" from="\orderResponse\buyer\gln"/><Select dest="@organization_name2" from="\orderResponse\buyer\organization\name"/><Select dest="@organization_inn2" from="\orderResponse\buyer\organization\inn"/><Select dest="@organization_kpp2" from="\orderResponse\buyer\organization\kpp"/><Select dest="@estimatedDeliveryDateTime" from="\orderResponse\deliveryInfo\estimatedDeliveryDateTime"/><Select dest="@shipFrom_gln" from="\orderResponse\deliveryInfo\shipFrom\gln"/><Select dest="@shipTo_gln" from="\orderResponse\deliveryInfo\shipTo\gln"/><Select dest="@currencyISOCode" from="\orderResponse\lineItems\currencyISOCode"/><Select dest="@totalSumExcludingTaxes" from="\orderResponse\lineItems\totalSumExcludingTaxes"/><SelectEach dest="lineItem\ROWlineItem" from="\orderResponse\lineItems\lineItem"><Select dest="@status" from="@status"/><Select dest="@gtin" from="\gtin"/><Select dest="@internalBuyerCode" from="\internalBuyerCode"/><Select dest="@internalSupplierCode" from="\internalSupplierCode"/><Select dest="@orderLineNumber" from="\orderLineNumber"/><Select dest="@description" from="\description"/><Select dest="@confirmedQuantity" from="\confirmedQuantity"/><Select dest="@unitOfMeasure" from="\confirmedQuantity@unitOfMeasure"/><Select dest="@orderedQuantity" from="\orderedQuantity"/><Select dest="@unitOfMeasureOrdered" from="\orderedQuantity@unitOfMeasure"/><Select dest="@netPrice" from="\netPrice"/><Select dest="@netPriceWithVAT" from="\netPriceWithVAT"/><Select dest="@netAmount" from="\netAmount"/><Select dest="@amount" from="\amount"/></SelectEach></SelectEach></Transform><XmlSchema RootName="eDIMessage"><![CDATA[<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="eDIMessage" type="eDIMessageType"/>
  <xs:complexType name="eDIMessageType">
    <xs:sequence>
      <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
      <xs:element name="orderResponse" type="orderResponseType"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:string"/>
    <xs:attribute name="creationDateTime" type="xs:string"/>
  </xs:complexType>
  <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
  <xs:complexType name="interchangeHeaderType">
    <xs:sequence>
      <xs:element name="sender" type="senderType"/>
      <xs:element name="recipient" type="recipientType"/>
      <xs:element name="documentType" type="documentTypeType"/>
      <xs:element name="isTest" type="isTestType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="sender" type="senderType"/>
  <xs:simpleType name="senderType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="recipient" type="recipientType"/>
  <xs:simpleType name="recipientType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="documentType" type="documentTypeType"/>
  <xs:simpleType name="documentTypeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="isTest" type="isTestType"/>
  <xs:simpleType name="isTestType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderResponse" type="orderResponseType"/>
  <xs:complexType name="orderResponseType">
    <xs:sequence>
      <xs:element name="originOrder" type="originOrderType"/>
      <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
      <xs:element name="seller" type="sellerType"/>
      <xs:element name="buyer" type="buyerType"/>
      <xs:element name="deliveryInfo" type="deliveryInfoType"/>
      <xs:element name="lineItems" type="lineItemsType"/>
    </xs:sequence>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="originOrder" type="originOrderType"/>
  <xs:complexType name="originOrderType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
  </xs:complexType>
  <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
  <xs:complexType name="blanketOrderIdentificatorType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
  </xs:complexType>
  <xs:element name="seller" type="sellerType"/>
  <xs:complexType name="sellerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="name" type="nameType"/>
  <xs:simpleType name="nameType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="inn" type="innType"/>
  <xs:simpleType name="innType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="kpp" type="kppType"/>
  <xs:simpleType name="kppType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="buyer" type="buyerType"/>
  <xs:complexType name="buyerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="deliveryInfo" type="deliveryInfoType"/>
  <xs:complexType name="deliveryInfoType">
    <xs:sequence>
      <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
      <xs:element name="shipFrom" type="shipFromType"/>
      <xs:element name="shipTo" type="shipToType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
  <xs:simpleType name="estimatedDeliveryDateTimeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipFrom" type="shipFromType"/>
  <xs:complexType name="shipFromType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipTo" type="shipToType"/>
  <xs:complexType name="shipToType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItems" type="lineItemsType"/>
  <xs:complexType name="lineItemsType">
    <xs:sequence>
      <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
      <xs:element name="lineItem" type="lineItemType" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
  <xs:simpleType name="currencyISOCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItem" type="lineItemType"/>
  <xs:complexType name="lineItemType">
    <xs:sequence>
      <xs:element name="gtin" type="gtinType"/>
      <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
      <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
      <xs:element name="orderLineNumber" type="orderLineNumberType"/>
      <xs:element name="description" type="descriptionType"/>
      <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
      <xs:element name="orderedQuantity" type="orderedQuantityType"/>
      <xs:element name="netPrice" type="netPriceType"/>
      <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
      <xs:element name="netAmount" type="netAmountType"/>
      <xs:element name="amount" type="amountType"/>
    </xs:sequence>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="gtin" type="gtinType"/>
  <xs:simpleType name="gtinType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
  <xs:simpleType name="internalBuyerCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
  <xs:simpleType name="internalSupplierCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderLineNumber" type="orderLineNumberType"/>
  <xs:simpleType name="orderLineNumberType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="description" type="descriptionType"/>
  <xs:simpleType name="descriptionType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
  <xs:complexType name="confirmedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="orderedQuantity" type="orderedQuantityType"/>
  <xs:complexType name="orderedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="netPrice" type="netPriceType"/>
  <xs:simpleType name="netPriceType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
  <xs:simpleType name="netPriceWithVATType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netAmount" type="netAmountType"/>
  <xs:simpleType name="netAmountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="amount" type="amountType"/>
  <xs:simpleType name="amountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
  <xs:simpleType name="totalSumExcludingTaxesType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
</xs:schema>]]></XmlSchema><CdsSkeleton/><XslTransform/><Skeleton><![CDATA[<?xml version="1.0"?><DATAPACKET Version="2.0"><METADATA><FIELDS><FIELD attrname="id" fieldtype="string" WIDTH="9"/><FIELD attrname="creationDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="sender" fieldtype="string" WIDTH="13"/><FIELD attrname="recipient" fieldtype="string" WIDTH="13"/><FIELD attrname="documentType" fieldtype="string" WIDTH="6"/><FIELD attrname="isTest" fieldtype="string" WIDTH="1"/><FIELD attrname="number1" fieldtype="string" WIDTH="10"/><FIELD attrname="date1" fieldtype="string" WIDTH="10"/><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="number2" fieldtype="string" WIDTH="20"/><FIELD attrname="date2" fieldtype="string" WIDTH="10"/><FIELD attrname="number3" fieldtype="string" WIDTH="10"/><FIELD attrname="seller_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name1" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn1" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp1" fieldtype="string" WIDTH="9"/><FIELD attrname="buyer_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name2" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn2" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp2" fieldtype="string" WIDTH="9"/><FIELD attrname="estimatedDeliveryDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="shipFrom_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="shipTo_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="currencyISOCode" fieldtype="string" WIDTH="3"/><FIELD attrname="totalSumExcludingTaxes" fieldtype="string" WIDTH="9"/><FIELD attrname="lineItem" fieldtype="nested"><FIELDS><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="gtin" fieldtype="string" WIDTH="13"/><FIELD attrname="internalBuyerCode" fieldtype="string" WIDTH="12"/><FIELD attrname="internalSupplierCode" fieldtype="string" WIDTH="12"/><FIELD attrname="orderLineNumber" fieldtype="string" WIDTH="3"/><FIELD attrname="description" fieldtype="string" WIDTH="150"/><FIELD attrname="confirmedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasure" fieldtype="string" WIDTH="3"/><FIELD attrname="orderedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasureOrdered" fieldtype="string" WIDTH="3"/><FIELD attrname="netPrice" fieldtype="string" WIDTH="9"/><FIELD attrname="netPriceWithVAT" fieldtype="string" WIDTH="9"/><FIELD attrname="netAmount" fieldtype="string" WIDTH="9"/><FIELD attrname="amount" fieldtype="string" WIDTH="9"/></FIELDS><PARAMS/></FIELD></FIELDS><PARAMS/></METADATA><ROWDATA/><METADATA><FIELDS><FIELD attrname="id" fieldtype="string" WIDTH="9"/><FIELD attrname="creationDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="sender" fieldtype="string" WIDTH="13"/><FIELD attrname="recipient" fieldtype="string" WIDTH="13"/><FIELD attrname="documentType" fieldtype="string" WIDTH="6"/><FIELD attrname="isTest" fieldtype="string" WIDTH="1"/><FIELD attrname="number1" fieldtype="string" WIDTH="20"/><FIELD attrname="date1" fieldtype="string" WIDTH="10"/><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="number2" fieldtype="string" WIDTH="20"/><FIELD attrname="date2" fieldtype="string" WIDTH="10"/><FIELD attrname="number3" fieldtype="string" WIDTH="10"/><FIELD attrname="seller_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name1" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn1" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp1" fieldtype="string" WIDTH="9"/><FIELD attrname="buyer_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name2" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn2" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp2" fieldtype="string" WIDTH="9"/><FIELD attrname="estimatedDeliveryDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="shipFrom_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="shipTo_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="currencyISOCode" fieldtype="string" WIDTH="3"/><FIELD attrname="totalSumExcludingTaxes" fieldtype="string" WIDTH="9"/><FIELD attrname="lineItem" fieldtype="nested"><FIELDS><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="gtin" fieldtype="string" WIDTH="13"/><FIELD attrname="internalBuyerCode" fieldtype="string" WIDTH="12"/><FIELD attrname="internalSupplierCode" fieldtype="string" WIDTH="12"/><FIELD attrname="orderLineNumber" fieldtype="string" WIDTH="3"/><FIELD attrname="description" fieldtype="string" WIDTH="150"/><FIELD attrname="confirmedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasure" fieldtype="string" WIDTH="3"/><FIELD attrname="orderedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasureOrdered" fieldtype="string" WIDTH="3"/><FIELD attrname="netPrice" fieldtype="string" WIDTH="9"/><FIELD attrname="netPriceWithVAT" fieldtype="string" WIDTH="9"/><FIELD attrname="netAmount" fieldtype="string" WIDTH="9"/><FIELD attrname="amount" fieldtype="string" WIDTH="9"/></FIELDS><PARAMS/></FIELD></FIELDS><PARAMS/></METADATA><ROWDATA/></DATAPACKET>
]]></Skeleton></XmlTransformation>
```

## KonturOrdrspDpToXml.xtr

```xml
<XmlTransformation Version="1.0"><Transform Direction="ToXml" DataEncoding="utf-8"><SelectEach from="DATAPACKET\ROWDATA\ROW" dest="\eDIMessage"><Select from="@id" dest="@id"/><Select from="@creationDateTime" dest="@creationDateTime"/><Select from="@sender" dest="\interchangeHeader\sender"/><Select from="@recipient" dest="\interchangeHeader\recipient"/><Select from="@documentType" dest="\interchangeHeader\documentType"/><Select from="@isTest" dest="\interchangeHeader\isTest"/><Select from="@number1" dest="\orderResponse@number"/><Select from="@date1" dest="\orderResponse@date"/><Select from="@status" dest="\orderResponse@status"/><Select from="@number2" dest="\orderResponse\originOrder@number"/><Select from="@date2" dest="\orderResponse\originOrder@date"/><Select from="@number3" dest="\orderResponse\blanketOrderIdentificator@number"/><Select from="@seller_gln" dest="\orderResponse\seller\gln"/><Select from="@organization_name1" dest="\orderResponse\seller\organization\name"/><Select from="@organization_inn1" dest="\orderResponse\seller\organization\inn"/><Select from="@organization_kpp1" dest="\orderResponse\seller\organization\kpp"/><Select from="@buyer_gln" dest="\orderResponse\buyer\gln"/><Select from="@organization_name2" dest="\orderResponse\buyer\organization\name"/><Select from="@organization_inn2" dest="\orderResponse\buyer\organization\inn"/><Select from="@organization_kpp2" dest="\orderResponse\buyer\organization\kpp"/><Select from="@estimatedDeliveryDateTime" dest="\orderResponse\deliveryInfo\estimatedDeliveryDateTime"/><Select from="@shipFrom_gln" dest="\orderResponse\deliveryInfo\shipFrom\gln"/><Select from="@shipTo_gln" dest="\orderResponse\deliveryInfo\shipTo\gln"/><Select from="@currencyISOCode" dest="\orderResponse\lineItems\currencyISOCode"/><Select from="@totalSumExcludingTaxes" dest="\orderResponse\lineItems\totalSumExcludingTaxes"/><SelectEach from="lineItem\ROWlineItem" dest="\orderResponse\lineItems\lineItem"><Select from="@status" dest="@status"/><Select from="@gtin" dest="\gtin"/><Select from="@internalBuyerCode" dest="\internalBuyerCode"/><Select from="@internalSupplierCode" dest="\internalSupplierCode"/><Select from="@orderLineNumber" dest="\orderLineNumber"/><Select from="@description" dest="\description"/><Select from="@confirmedQuantity" dest="\confirmedQuantity"/><Select from="@unitOfMeasure" dest="\confirmedQuantity@unitOfMeasure"/><Select from="@orderedQuantity" dest="\orderedQuantity"/><Select from="@unitOfMeasureOrdered" dest="\orderedQuantity@unitOfMeasure"/><Select from="@netPrice" dest="\netPrice"/><Select from="@netPriceWithVAT" dest="\netPriceWithVAT"/><Select from="@netAmount" dest="\netAmount"/><Select from="@amount" dest="\amount"/></SelectEach></SelectEach></Transform><XmlSchema RootName="eDIMessage"><![CDATA[<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="eDIMessage" type="eDIMessageType"/>
  <xs:complexType name="eDIMessageType">
    <xs:sequence>
      <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
      <xs:element name="orderResponse" type="orderResponseType"/>
    </xs:sequence>
    <xs:attribute name="id" type="xs:string"/>
    <xs:attribute name="creationDateTime" type="xs:string"/>
  </xs:complexType>
  <xs:element name="interchangeHeader" type="interchangeHeaderType"/>
  <xs:complexType name="interchangeHeaderType">
    <xs:sequence>
      <xs:element name="sender" type="senderType"/>
      <xs:element name="recipient" type="recipientType"/>
      <xs:element name="documentType" type="documentTypeType"/>
      <xs:element name="isTest" type="isTestType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="sender" type="senderType"/>
  <xs:simpleType name="senderType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="recipient" type="recipientType"/>
  <xs:simpleType name="recipientType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="documentType" type="documentTypeType"/>
  <xs:simpleType name="documentTypeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="isTest" type="isTestType"/>
  <xs:simpleType name="isTestType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderResponse" type="orderResponseType"/>
  <xs:complexType name="orderResponseType">
    <xs:sequence>
      <xs:element name="originOrder" type="originOrderType"/>
      <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
      <xs:element name="seller" type="sellerType"/>
      <xs:element name="buyer" type="buyerType"/>
      <xs:element name="deliveryInfo" type="deliveryInfoType"/>
      <xs:element name="lineItems" type="lineItemsType"/>
    </xs:sequence>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="originOrder" type="originOrderType"/>
  <xs:complexType name="originOrderType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
    <xs:attribute name="date" type="xs:string"/>
  </xs:complexType>
  <xs:element name="blanketOrderIdentificator" type="blanketOrderIdentificatorType"/>
  <xs:complexType name="blanketOrderIdentificatorType">
    <xs:sequence/>
    <xs:attribute name="number" type="xs:string"/>
  </xs:complexType>
  <xs:element name="seller" type="sellerType"/>
  <xs:complexType name="sellerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="name" type="nameType"/>
  <xs:simpleType name="nameType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="inn" type="innType"/>
  <xs:simpleType name="innType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="kpp" type="kppType"/>
  <xs:simpleType name="kppType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="buyer" type="buyerType"/>
  <xs:complexType name="buyerType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
      <xs:element name="organization" type="organizationType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="organization" type="organizationType"/>
  <xs:complexType name="organizationType">
    <xs:sequence>
      <xs:element name="name" type="nameType"/>
      <xs:element name="inn" type="innType"/>
      <xs:element name="kpp" type="kppType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="deliveryInfo" type="deliveryInfoType"/>
  <xs:complexType name="deliveryInfoType">
    <xs:sequence>
      <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
      <xs:element name="shipFrom" type="shipFromType"/>
      <xs:element name="shipTo" type="shipToType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="estimatedDeliveryDateTime" type="estimatedDeliveryDateTimeType"/>
  <xs:simpleType name="estimatedDeliveryDateTimeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipFrom" type="shipFromType"/>
  <xs:complexType name="shipFromType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="shipTo" type="shipToType"/>
  <xs:complexType name="shipToType">
    <xs:sequence>
      <xs:element name="gln" type="glnType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="gln" type="glnType"/>
  <xs:simpleType name="glnType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItems" type="lineItemsType"/>
  <xs:complexType name="lineItemsType">
    <xs:sequence>
      <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
      <xs:element name="lineItem" type="lineItemType" minOccurs="0" maxOccurs="unbounded"/>
      <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
    </xs:sequence>
  </xs:complexType>
  <xs:element name="currencyISOCode" type="currencyISOCodeType"/>
  <xs:simpleType name="currencyISOCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="lineItem" type="lineItemType"/>
  <xs:complexType name="lineItemType">
    <xs:sequence>
      <xs:element name="gtin" type="gtinType"/>
      <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
      <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
      <xs:element name="orderLineNumber" type="orderLineNumberType"/>
      <xs:element name="description" type="descriptionType"/>
      <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
      <xs:element name="orderedQuantity" type="orderedQuantityType"/>
      <xs:element name="netPrice" type="netPriceType"/>
      <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
      <xs:element name="netAmount" type="netAmountType"/>
      <xs:element name="amount" type="amountType"/>
    </xs:sequence>
    <xs:attribute name="status" type="xs:string"/>
  </xs:complexType>
  <xs:element name="gtin" type="gtinType"/>
  <xs:simpleType name="gtinType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalBuyerCode" type="internalBuyerCodeType"/>
  <xs:simpleType name="internalBuyerCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="internalSupplierCode" type="internalSupplierCodeType"/>
  <xs:simpleType name="internalSupplierCodeType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="orderLineNumber" type="orderLineNumberType"/>
  <xs:simpleType name="orderLineNumberType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="description" type="descriptionType"/>
  <xs:simpleType name="descriptionType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="confirmedQuantity" type="confirmedQuantityType"/>
  <xs:complexType name="confirmedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="orderedQuantity" type="orderedQuantityType"/>
  <xs:complexType name="orderedQuantityType">
    <xs:sequence/>
    <xs:attribute name="unitOfMeasure" type="xs:string"/>
  </xs:complexType>
  <xs:element name="netPrice" type="netPriceType"/>
  <xs:simpleType name="netPriceType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netPriceWithVAT" type="netPriceWithVATType"/>
  <xs:simpleType name="netPriceWithVATType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="netAmount" type="netAmountType"/>
  <xs:simpleType name="netAmountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="amount" type="amountType"/>
  <xs:simpleType name="amountType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
  <xs:element name="totalSumExcludingTaxes" type="totalSumExcludingTaxesType"/>
  <xs:simpleType name="totalSumExcludingTaxesType">
    <xs:restriction base="xs:string"/>
  </xs:simpleType>
</xs:schema>]]></XmlSchema><CdsSkeleton><![CDATA[<DATAPACKET Version="2.0"><METADATA><FIELDS><FIELD attrname="id" fieldtype="string" WIDTH="9"/><FIELD attrname="creationDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="sender" fieldtype="string" WIDTH="13"/><FIELD attrname="recipient" fieldtype="string" WIDTH="13"/><FIELD attrname="documentType" fieldtype="string" WIDTH="6"/><FIELD attrname="isTest" fieldtype="string" WIDTH="1"/><FIELD attrname="number1" fieldtype="string" WIDTH="20"/><FIELD attrname="date1" fieldtype="string" WIDTH="10"/><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="number2" fieldtype="string" WIDTH="20"/><FIELD attrname="date2" fieldtype="string" WIDTH="10"/><FIELD attrname="number3" fieldtype="string" WIDTH="10"/><FIELD attrname="seller_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name1" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn1" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp1" fieldtype="string" WIDTH="9"/><FIELD attrname="buyer_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name2" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn2" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp2" fieldtype="string" WIDTH="9"/><FIELD attrname="estimatedDeliveryDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="shipFrom_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="shipTo_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="currencyISOCode" fieldtype="string" WIDTH="3"/><FIELD attrname="totalSumExcludingTaxes" fieldtype="string" WIDTH="9"/><FIELD attrname="lineItem" fieldtype="nested"><FIELDS><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="gtin" fieldtype="string" WIDTH="13"/><FIELD attrname="internalBuyerCode" fieldtype="string" WIDTH="12"/><FIELD attrname="internalSupplierCode" fieldtype="string" WIDTH="12"/><FIELD attrname="orderLineNumber" fieldtype="string" WIDTH="3"/><FIELD attrname="description" fieldtype="string" WIDTH="150"/><FIELD attrname="confirmedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasure" fieldtype="string" WIDTH="3"/><FIELD attrname="orderedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasureOrdered" fieldtype="string" WIDTH="3"/><FIELD attrname="netPrice" fieldtype="string" WIDTH="9"/><FIELD attrname="netPriceWithVAT" fieldtype="string" WIDTH="9"/><FIELD attrname="netAmount" fieldtype="string" WIDTH="9"/><FIELD attrname="amount" fieldtype="string" WIDTH="9"/></FIELDS><PARAMS/></FIELD></FIELDS><PARAMS/></METADATA><ROWDATA/><METADATA><FIELDS><FIELD attrname="id" fieldtype="string" WIDTH="9"/><FIELD attrname="creationDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="sender" fieldtype="string" WIDTH="13"/><FIELD attrname="recipient" fieldtype="string" WIDTH="13"/><FIELD attrname="documentType" fieldtype="string" WIDTH="6"/><FIELD attrname="isTest" fieldtype="string" WIDTH="1"/><FIELD attrname="number1" fieldtype="string" WIDTH="20"/><FIELD attrname="date1" fieldtype="string" WIDTH="10"/><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="number2" fieldtype="string" WIDTH="20"/><FIELD attrname="date2" fieldtype="string" WIDTH="10"/><FIELD attrname="number3" fieldtype="string" WIDTH="10"/><FIELD attrname="seller_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name1" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn1" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp1" fieldtype="string" WIDTH="9"/><FIELD attrname="buyer_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="organization_name2" fieldtype="string" WIDTH="50"/><FIELD attrname="organization_inn2" fieldtype="string" WIDTH="12"/><FIELD attrname="organization_kpp2" fieldtype="string" WIDTH="9"/><FIELD attrname="estimatedDeliveryDateTime" fieldtype="string" WIDTH="19"/><FIELD attrname="shipFrom_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="shipTo_gln" fieldtype="string" WIDTH="13"/><FIELD attrname="currencyISOCode" fieldtype="string" WIDTH="3"/><FIELD attrname="totalSumExcludingTaxes" fieldtype="string" WIDTH="9"/><FIELD attrname="lineItem" fieldtype="nested"><FIELDS><FIELD attrname="status" fieldtype="string" WIDTH="15"/><FIELD attrname="gtin" fieldtype="string" WIDTH="13"/><FIELD attrname="internalBuyerCode" fieldtype="string" WIDTH="12"/><FIELD attrname="internalSupplierCode" fieldtype="string" WIDTH="12"/><FIELD attrname="orderLineNumber" fieldtype="string" WIDTH="3"/><FIELD attrname="description" fieldtype="string" WIDTH="150"/><FIELD attrname="confirmedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasure" fieldtype="string" WIDTH="3"/><FIELD attrname="orderedQuantity" fieldtype="string" WIDTH="2"/><FIELD attrname="unitOfMeasureOrdered" fieldtype="string" WIDTH="3"/><FIELD attrname="netPrice" fieldtype="string" WIDTH="9"/><FIELD attrname="netPriceWithVAT" fieldtype="string" WIDTH="9"/><FIELD attrname="netAmount" fieldtype="string" WIDTH="9"/><FIELD attrname="amount" fieldtype="string" WIDTH="9"/></FIELDS><PARAMS/></FIELD></FIELDS><PARAMS/></METADATA><ROWDATA/></DATAPACKET>
]]></CdsSkeleton><XslTransform/><Skeleton><![CDATA[<?xml version="1.0"?>
<eDIMessage id="000001520" creationDateTime="2013-09-27T00:00:00">
	<!--идентификатор сообщения, время сообщения-->
	<!-- начало заголовка сообщения -->
	<interchangeHeader>
		<sender></sender>
		<!--GLN отправителя сообщения-->
		<recipient></recipient>
		<!--GLN получателя сообщения-->
		<documentType></documentType>
		<isTest></isTest>
		<!--тестовый флаг-->
	</interchangeHeader>
	<orderResponse number="" date="" status="">
		<!--номер документа-респонса, дата документа-респонса, статус документа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
		<originOrder number="" date=""/>
		<!--номер заказа, дата заказа-->
		<blanketOrderIdentificator number=""/>
		<!--номер серии заказов-->
		<seller>
			<gln></gln>
			<!--gln поставщика-->
			<organization>
				<name></name>
				<!--наименование поставщика для ЮЛ-->
				<inn></inn>
				<!--ИНН поставщика для ЮЛ-->
				<kpp></kpp>
				<!--КПП поставщика только для ЮЛ-->
			</organization>
		</seller>
		<buyer>
			<gln></gln>
			<!--gln покупателя-->
			<organization>
				<name></name>
				<!--наименование покупателя-->
				<inn></inn>
				<!--ИНН покупателя для ЮЛ-->
				<kpp></kpp>
				<!--КПП покупателя только для ЮЛ-->
			</organization>
		</buyer>
		<deliveryInfo>
			<estimatedDeliveryDateTime></estimatedDeliveryDateTime>
			<!--дата доставки-->
			<shipFrom>
				<gln></gln>
				<!--gln грузоотправителя-->
			</shipFrom>
			<shipTo>
				<gln></gln>
				<!--gln грузополучателя-->
			</shipTo>
		</deliveryInfo>
		<lineItems>
			<currencyISOCode></currencyISOCode>
			<!--код валюты (по умолчанию рубли)-->
			<lineItem status="">
				<!--статус подтверждения строки заказа: Changed - уточнен, Rejected - отклонен, Accepted - подтвержден-->
				<gtin></gtin>
				<!--GTIN товара-->
				<internalBuyerCode></internalBuyerCode>
				<!--внутренний код присвоенный покупателем-->
				<internalSupplierCode></internalSupplierCode>
				<!--артикул товара (код товара присвоенный продавцом)-->
				<orderLineNumber></orderLineNumber>
				<!--порядковый номер товара-->
				<description></description>
				<!--название товара-->
				<confirmedQuantity unitOfMeasure=""></confirmedQuantity>
				<!--заказанное количество-->
				<orderedQuantity unitOfMeasure=""></orderedQuantity>
				<!--подтвержденное количество-->
				<netPrice></netPrice>
				<!--цена товара без НДС-->
				<netPriceWithVAT></netPriceWithVAT>
				<!--цена товара с НДС-->
				<netAmount></netAmount>
				<!--сумма по позиции без НДС-->
				<amount></amount>
				<!--сумма по позиции с НДС-->
			</lineItem>
			<totalSumExcludingTaxes></totalSumExcludingTaxes>
			<!--сумма заявки без НДС-->
		</lineItems>
	</orderResponse>
</eDIMessage>
]]></Skeleton></XmlTransformation>
```