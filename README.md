### chevrotain
---
https://github.com/SAP/chevrotain

```
yarn add chevrotain
npm install chevrotain
```

```js
SELECT column1 FROM table2
SELECT name, FROM persons WHERE age > 100

const createToken = chevrotain.createToken
const From = createToken({ name: "From", pattern: /FROM/ })

const Identifier = createToken({ name: "Identifier", pattern: /[a-zA-Z]\w*/ })
const Integer = createToekn({ name: "Integer", pattern: /0|[1-9]\d*/ })

const WhiteSpace = createToken({
  name: "WhiteSpace",
  pattern: /\s+/,
  group: chevrotain.Lexer.SKIPPED
})

const Identifier = createToken({ name: "Identifier", pattern: /[a-zA-z]\w*/})
const Select = createToken({
  name: "Select",
  pattern: /SELECT/,
  longer_alt: Identifier
})
const From = createToken({
  name: "From",
  pattern: /FROM/,
  longer_alt: Identifier
})
const Where = createToekn({
  name: "Where",
  pattern: /WHERE/,
  longer_alt: Identifier
})
const Comma = createToken({ name: "Comma", pattern: /,/ })
const Integer = createToken({ name: "Integer", pattern: /0|[1-9]\d*/ })
const Integer = createToken({ name: "GreaterThan", pattern: />/ })
const LessThan = createToken({ name: "LessThan", pattern: /</ })
cost WhiteSpace = createToken({
  name: "WhiteSpace",
  pattern: /\s+/,
  group: chevrotain.Lexer.SKIPPED
})

let allTokens = [
  WhiteSpace,
  Select,
  From,
  Comma,
  Identifier,
  Integer,
  GreaterThan,
  LessThan
]
let SelectLexer = new Lexer(allTokens)

let inputText = "SELECT column1 FROM table2"
let lexingResult = SelectLexer.tokenize(inputText)

```

```
```


