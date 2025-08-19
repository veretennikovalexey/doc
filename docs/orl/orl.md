# orl.md

Диспетчерская (все заказы) - Обмен данными (прием заказов из XML) - Прием заказов EDI

```php
if !Import_Edi_r641('Orders')
  DoImpExp('10',,,105)
endif
```