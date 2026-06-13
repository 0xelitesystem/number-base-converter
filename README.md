# Number Base Converter

Convert an integer between binary, octal, decimal, hexadecimal, and any base from 2 to 36, in your browser. No server, no tracking, no third-party scripts.

**Live demo:** https://0xelitesystem.github.io/number-base-converter/

## Use

Open `index.html` in any modern browser, or visit the GitHub Pages link in the repo description.

Type a value into any field. The other fields update live to show the same number in their base. The arbitrary-base field has its own base selector (2 to 36) so you can convert to or from things like base 12 or base 36.

- Conversion uses BigInt, so even very large numbers stay exact (no floating-point rounding)
- Input is validated per base; an invalid digit shows a clear error naming the offending character
- Negative numbers are supported with a leading `-`
- Each field has a Copy button

## Why this exists

Programmer calculators and online base converters often lose precision on large values because they convert through a JavaScript `Number`, or they bury the tool under ads and trackers. This one uses BigInt for exact results of any size, single file, no analytics, no signup, MIT licensed.

## Privacy

Everything runs in your browser. The numbers you type never leave your machine. Verify by viewing the page source or by opening DevTools and watching the network tab, no requests are made.

## Run locally

```bash
git clone https://github.com/0xelitesystem/number-base-converter
cd number-base-converter
# Open index.html in your browser, or:
python -m http.server 8000
```

## Contribute

Issues and PRs welcome:

- Parsing edge cases (signs, whitespace, very long inputs)
- Optional grouping or separators in the output
- UI improvements (keep it minimal, no frameworks)
- Translations

Don't add: analytics, tracking, external scripts, npm dependencies. The whole point of this tool is no surveillance.

## Build

There is no build. It's a single HTML file.

## License

MIT.

## Related

- [base64-url-encoder-decoder](https://github.com/0xelitesystem/base64-url-encoder-decoder), encode and decode Base64 and Base64URL
- [json-formatter-and-validator](https://github.com/0xelitesystem/json-formatter-and-validator), format and validate JSON in your browser
- [case-converter](https://github.com/0xelitesystem/case-converter), convert text between casing styles
