# aprs-symbols
JS library providing rendering interface for APRS icons

## Usage

Include the resources in your app
```html
<!-- Necessary CSS, PNG sprites should be in the same directory as the CSS file -->
<link rel="stylesheet" href="aprs-symbols.css"/>

<!-- Optional JS -->
<script src="aprs-symbols.js"></script>
```

Plain HTML/CSS
```html
<!-- To draw symbol from table 0, address row 1, column 13 -->
<i class="aprs-table0 aprs-address-1-13"></i>
```

JS helper function to get image tag string by symbol
```javascript
// helper function returns string "<i class="aprs-table0 aprs-address-3-10"></i>"
let imageTagString = getAPRSSymbolImageTag('/[');
```

JS helper function to get image tag by known address (format [table, column, row])
```javascript
// helper function returns string "<i class="aprs-table0 aprs-address-3-10"></i>"
let imageTagString = getAPRSSymbolImageTagByAddress([0, 3, 10]);
```

## Using symbols sprites from OH7LZB
PNG images used to render aprs symbols borrowed from OH7LZB repository
see source http://github.com/hessu/aprs-symbols/
