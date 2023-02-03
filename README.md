# Deno JSON5
**[JSON5](https://npmjs.com/package/json5)** for **[Deno](https://deno.land)**.

# Example

`main.ts`
```js
import JSON5 from "https://deno.land/x/json5/mod.ts";

const data = `{
    // comments
    unquoted: 'and you can quote me on that',
    singleQuotes: 'I can use "double quotes" here',
    lineBreaks: "Look, Mom! \
No \\n's!",
    hexadecimal: 0xdecaf,
    leadingDecimalPoint: .8675309, andTrailing: 8675309.,
    positiveSign: +1,
    trailingComma: 'in objects', andIn: ['arrays',
        ],
    "backwardsCompatible": "with JSON",
}`;
console.log(JSON5.parse(data));

/*
{
  unquoted: "and you can quote me on that",
  singleQuotes: 'I can use "double quotes" here',
  lineBreaks: "Look, Mom! No \\n's!",
  hexadecimal: 912559,
  leadingDecimalPoint: 0.8675309,
  andTrailing: 8675309,
  positiveSign: 1,
  trailingComma: "in objects",
  andIn: [ "arrays" ],
  backwardsCompatible: "with JSON"
}
*/
```

# Methods
- `JSON5.stringify`
- `JSON5.parse`
- `JSON5.require`
- `JSON5.requireAsync`
