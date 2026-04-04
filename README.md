# AC CountryList
This is a little helper to retrieve a countrylist and query this countrylist.

The countrylist is forked from https://gist.github.com/stefanbauer/bf0720c6846a3cc9b59e

[![Node.js CI](https://github.com/AdmiralCloud/ac-countrylist/actions/workflows/node.js.yml/badge.svg)](https://github.com/AdmiralCloud/ac-countrylist/actions/workflows/node.js.yml) [![CodeQL](https://github.com/AdmiralCloud/ac-countrylist/actions/workflows/github-code-scanning/codeql/badge.svg)](https://github.com/AdmiralCloud/ac-countrylist/actions/workflows/github-code-scanning/codeql)

## Usage
You can use the countrylist directly by importing countrylist.js. But it is recommended to use this little helper and require this module.

```
const acCountryList = require('ac-countrylist')
```

### Fetch country list
Return a short list with iso2, country name and spoken languages.
```
const list = acCountryList.showList()
// -> [{ name: 'Afghanistan',
    iso2: 'af',
    alpha2Code: 'af',
    languages: [ 'ps', 'uz', 'tk' ] }, ...]
```

### Query list
Query the country list (currently only iso2 and iso3 is supported)
```
const country = acCountryList.query({ iso2: 'de' })
// OR
const country = acCountryList.query({ iso3: 'deu' })

// -> { name: 'Germany',
  capital: 'Berlin',
  altSpellings:
   [ 'DE',
     'Federal Republic of Germany',
     'Bundesrepublik Deutschland' ],
  relevance: '3',
  region: 'Europe',
  subregion: 'Western Europe',
  translations:
   { de: 'Deutschland',
     es: 'Alemania',
     fr: 'Allemagne',
     ja: 'ドイツ',
     it: 'Germania' },
  population: 81083600,
  latlng: [ 51, 9 ],
  demonym: 'German',
  area: 357114,
  gini: 28.3,
  timezones: [ 'UTC+01:00' ],
  borders:
   [ 'AUT', 'BEL', 'CZE', 'DNK', 'FRA', 'LUX', 'NLD', 'POL', 'CHE' ],
  nativeName: 'Deutschland',
  callingCodes: [ '49' ],
  topLevelDomain: [ '.de' ],
  alpha2Code: 'DE',
  alpha3Code: 'DEU',
  currencies: [ 'EUR' ],
  languages: [ 'de' ] }
```

### Fetch random country
Return a random country
```
const randomCountry = acCountryList.random()
//
{ name: 'Afghanistan',
  iso2: 'af',
  alpha2Code: 'af',
  languages: [ 'ps', 'uz', 'tk' ] 
}
```

## Links
- [Website](https://www.admiralcloud.com/)
- [Twitter (@admiralcloud)](https://twitter.com/admiralcloud)
- [Facebook](https://www.facebook.com/MediaAssetManagement/)

## License
[MIT License](https://opensource.org/licenses/MIT) Copyright © 2009-present, AdmiralCloud, Mark Poepping