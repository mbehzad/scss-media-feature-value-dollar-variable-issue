# Minimal Reproducing Repo for scss/scss-media-feature-value-dollar-variable false positive for `module.$var`

SCSS code:

```scss
@media (max-width: variables.$val) { a { color: red; } }
```

stylelintrc config:

```json
{
  "plugins": [
    "stylelint-scss"
  ],
  "rules": {
    "scss/media-feature-value-dollar-variable": "always"
  },
  "customSyntax": "postcss-scss"
}
```

Error:

```text
1:20  ✖  Expected a dollar-variable (e.g. $var) to be used as a media feature value  scss/media-feature-value-dollar-variable
```

Run `npm test` to see the stylelint error.
