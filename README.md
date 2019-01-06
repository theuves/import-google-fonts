# import-google-fonts

> Import fonts from Google Fonts with *styled-components*.

## Installation

You can install it with *npm* or *yarn*.

Try:

- `npm install import-google-fonts`
- `yarn add import-google-fonts`

## Usage

See a simple example:

```javascript
import { createGlobalStyle } from 'styled-components'
import importGoogleFonts from 'import-google-fonts'

importGoogleFonts(importGoogleFonts, null, [
  'Roboto',
  'Indie Flower'
])

createGlobalStyle`
  body {
    font-family: Roboto, Arial, sans-serif;
  }
`
```

### Syntax

```javascript
importGoogleFonts(injector, protocol, fonts)
```

When:

* `inject` - A function that handles global styles.
* `protocol` - Can be `'http'` or `'https'`. The default value is `'https'`.
* `fonts` - An array with the fonts you want to import.

> **NOTE**: `inject` must be [`createGlobalStyle`](https://www.styled-components.com/docs/api#createglobalstyle), but in *styled-components* v3 and bellow you must use [`injectGlobal`](https://www.styled-components.com/docs/api#deprecated-injectglobal).

## License

MIT &copy; Matheus Alves