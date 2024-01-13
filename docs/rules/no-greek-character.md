# Disallow Greek Characters (no-greek-character)

In an internationalized application, Greek characters are not allowed. This rule helps to find out where Greek characters are.

## Rule Details

The following patterns are considered problems:

```js
var str = "Ελληνικά";
```

The following patterns are not considered problems:

```js
var str = "English";

// or

var str = this.getIntlMessage("i18n.key"); // using an i18n tool instead of regular Greek characters
```

## Rule Options

The rule takes one option, an object, which has several keys with boolean values `true` or `false`.

### includeIdentifier

```json
"i18n/no-greek-character": [
  "warn",
  {
    "includeIdentifier": true
  }
]
```

### includeComment

* In general, we don't check comments for l10n/i18n. If you would like to lint them, set `includeComment` as `true` to enforce checking.

```json
"i18n/no-greek-character": [
  "warn",
  {
    "includeComment": true
  }
]
```
