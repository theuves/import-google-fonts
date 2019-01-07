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
import React, { Fragment } from 'react'
import ReactDOM from 'react-dom'
import styled, { createGlobalStyle } from 'styled-components'
import importGoogleFonts from 'import-google-fonts'

const GoogleFonts = importGoogleFonts(createGlobalStyle, null, [
  'Pacifico'
])

const MyText = styled.h1`
  font-family: 'Pacifico', cursive;
`

const App = () => (
  <Fragment>
    <GoogleFonts />
    <MyText>
      Hello, World!
    </MyText>
  </Fragment>   
)

ReactDOM.render(
  <App />,
  document.getElementById('root')
)
```

### Syntax

```javascript
importGoogleFonts(inject, protocol, fonts)
```

When:

* `inject` - The [`createGlobalStyle`](https://www.styled-components.com/docs/api#createglobalstyle) function in v4 and above or [`injectGlobal`](https://www.styled-components.com/docs/api#deprecated-injectglobal) in v3 and bellow.
* `protocol` - Can be `'http'` or `'https'`. The default value is `'https'`.
* `fonts` - An array with the fonts you want to import.

**NOTE:** In *styled-components* v3 and below you don't need to create a component.

## License

MIT &copy; Matheus Alves