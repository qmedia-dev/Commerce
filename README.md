# Commerce

<img src="https://img.shields.io/badge/CMS-%3E%3D1.4.6-green.svg"> <img src="https://img.shields.io/badge/PHP-%3E=5.6-green.svg?php=5.6">

## Add product to cart

```html
<form action="#" data-commerce-action="add">
	<input type="hidden" name="id" value="[*id*]" />
	<input type="hidden" name="count" value="1" />
	<input type="hidden" name="options[color]" value="White" />
	<input type="hidden" name="options[services][]" value="Uplift" />
	<input type="hidden" name="options[services][]" value="Assembling" />
	<input type="hidden" name="meta[key]" value="value" />
	<button type="submit">Add to cart</button>
</form>

<a href="#" data-commerce-action="add" data-id="[*id*]" data-count="2">Add to cart</a>

<a href="#" data-commerce-action="add" data-id="[*id*]" data-instance="wishlist">Add to wishlist</a>

<a href="#" data-commerce-action="remove" data-row="[*row*]">Remove from cart by row hash</a>

<a href="#" data-commerce-action="remove" data-id="[*id*]">Remove from cart by ID</a>
```

## Show cart

```php
[!Cart
    &instance=`products`
    &theme=``
    &tpl=`tpl`
    &optionsTpl=`optionsTpl`
    &ownerTPL=`ownerTPL`
    &subtotalsRowTpl=`subtotalsRowTpl`
    &subtotalsTpl=`subtotalsTpl`
!]
```

## Show currency selection

```php
[!CurrencySelect
    &tpl=`tpl`
    &activeTpl=`activeTpl`
    &outerTpl=`outerTpl`
!]
```

## Show order form

```php
[!Order
    &formTpl=`formTpl`
    &deliveryTpl=`deliveryTpl`
    &deliveryRowTpl=`deliveryRowTpl`
    &paymentsTpl=`paymentsTpl`
    &paymentsRowTpl=`paymentsRowTpl`
    &reportTpl=`reportTpl`
    &ccSenderTpl=`ccSenderTpl`
!]
```

## Payments settings

```txt
Process: POST /commerce/<payment_code>/payment-process
Success: POST /commerce/<payment_code>/payment-success
Failed:  POST /commerce/<payment_code>/payment-failed
```
