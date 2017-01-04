[![Build Status](https://travis-ci.org/PolymerEl/paper-locale-input.svg?branch=master)](https://travis-ci.org/PolymerEl/paper-locale-input)
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://beta.webcomponents.org/element/polymerEl/paper-locale-input)

# \<paper-locale-input\>

`<paper-locale-input>` is a customizable paper input to deal with locale data (e.g. currencies). 

It relies on [`toLocaleString`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/Number/toLocaleString) for returning a language seneitive representation of the inputed number. 
For older browser not supporting `toLocaleString` a fallback using a usual `paper-input` with a currency prefix is used.

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

<paper-locale-input value="123000000"	label="amount"  currency="EUR" locale="fr_FR"></paper-locale-input>

```

