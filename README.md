[![Build Status](https://travis-ci.org/PolymerEl/paper-locale-input.svg?branch=master)](https://travis-ci.org/PolymerEl/paper-locale-input)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/polymerEl/paper-locale-input)

# \<paper-locale-input\>

`<paper-locale-input>` is a customizable paper input to deal with locale data (e.g. currencies). 

It relies on [`toLocaleString`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString) for returning a language sensitive representation of the inputed number. 
For older browser not supporting `toLocaleString` a fallback using a usual `paper-input` with a currency prefix is used.

Every country and language has its own usual representation of numbers and currency: 

``` js
var number = 123456.789;

// German uses comma as decimal separator and period for thousands
console.log(number.toLocaleString('de-DE'));
// → 123.456,789

// Arabic in most Arabic speaking countries uses Eastern Arabic digits
console.log(number.toLocaleString('ar-EG'));
// → ١٢٣٤٥٦٫٧٨٩

// India uses thousands/lakh/crore separators
console.log(number.toLocaleString('en-IN'));
// → 1,23,456.789

// the nu extension key requests a numbering system, e.g. Chinese decimal
console.log(number.toLocaleString('zh-Hans-CN-u-nu-hanidec'));
// → 一二三,四五六.七八九

// when requesting a language that may not be supported, such as
// Balinese, include a fallback language, in this case Indonesian
console.log(number.toLocaleString(['ban', 'id']));
// → 123.456,789

// request a currency format
console.log(number.toLocaleString('de-DE', { style: 'currency', currency: 'EUR' }));
// → 123.456,79 €

// the Japanese yen doesn't use a minor unit
console.log(number.toLocaleString('ja-JP', { style: 'currency', currency: 'JPY' }))
// → ￥123,457

// limit to three significant digits
console.log(number.toLocaleString('en-IN', { maximumSignificantDigits: 3 }));
// → 1,23,000

```
Example Usage:

<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="paper-locale-input.html">
    <link rel="import" href="../paper-input/paper-input.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
```html

<paper-locale-input value="123000000"	label="amount"  currency="EUR" locale="fr-FR"></paper-locale-input>

```

