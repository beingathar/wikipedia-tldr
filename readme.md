# wikipedia-tldr 

> Grab the first paragraph of any Wikipedia page

Use it programmatically with JavaScript to fetch JSON, or use the command line interface (CLI) to look stuff up from your terminal.

## Programmatic Usage

Install it:

```sh
npm install wikipedia-tldr
```

Use it in JavaScript:

```js
const tldr = require('wikipedia-tldr')

tldr('somatology').then(result => {
  console.log(result)
})
```

The result looks like this:

```js
{
  query: 'somatology',
  html: '<p> ...same as text but with markup preserved... </p>',
  text: 'English\nEtymology\nFrom soma (body) +‎ -ology.\nNoun\nsomatology (usually uncountable, plural somatologies)\nThe study of the physical nature of human beings.\nDerived terms\nanthroposomatology\n'
}
```

If no result is found, `null` is returned.

The default language is English `en`, but you can specify a different language
with an optional secondar argument to the function:

```js
tldr('muñeca', 'es')
```

For available language codes, see the [List of Wikipedias](https://en.wikipedia.org/wiki/List_of_Wikipedias).

## CLI Usage

```
npm i -g wikipedia-tldr && wikipedia-tldr pomology
```

or use [npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b)

```sh
$ npx wikipedia-tldr zymology
npx: installed 62 in 4.301s
English

Alternative forms
zumology (dated)
Etymology
From zymo- +‎ -logy.
Noun
zymology (uncountable)
(zymurgy) A treatise on the fermentation of liquors, or the doctrine of fermentation.
The science of or knowledge concerning fermentation.
Translations


References
zymology in Webster’s Revised Unabridged Dictionary, G. & C. Merriam, 1913
The Century Dictionary, The Century Co., New York, 1914
```

## Tests

```sh
npm install
npm test
```

## Dependencies

- [cheerio](https://github.com/cheeriojs/cheerio): Tiny, fast, and elegant implementation of core jQuery designed specifically for the server
- [got](): Simplified HTTP requests

## Dev Dependencies

- [jest](https://github.com/facebook/jest): Delightful JavaScript Testing.


## License

MIT
