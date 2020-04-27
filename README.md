# aprs-symbols
CSS library with optional JS providing rendering means for APRS icons, rendering square icons of sizes 24px, 48px, 64px and 128px

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
<!-- To draw symbol from table 1, address row 3, column 3, size 128px -->
<i class="aprs-table0-128 aprs-address-3-3"></i>
```

JS helper function to get image tag string by symbol
```javascript
// helper function returns string "<i class="aprs-table0 aprs-address-3-10"></i>"
let imageTagString = getAPRSSymbolImageTag('/[');
// helper function returns string "<i class="aprs-table0-64 aprs-address-64-3-10"></i>", ie. same symbol as above, but 64x64px size
let imageTagString = getAPRSSymbolImageTag('/[', 64);
```

JS helper function to get image tag by known address (format [table, column, row])
```javascript
// helper function returns string "<i class="aprs-table0 aprs-address-3-10"></i>"
let imageTagString = getAPRSSymbolImageTagByAddress([0, 3, 10]);
// helper function returns string "<i class="aprs-table0-48 aprs-address-48-3-10"></i>", ie. same symbol as above, but 48x46px size
let imageTagString = getAPRSSymbolImageTagByAddress([0, 3, 10], 48);
```

## Using symbols sprites from OH7LZB
PNG images used to render aprs symbols borrowed from OH7LZB repository
see source http://github.com/hessu/aprs-symbols/
