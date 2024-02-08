Полезные настройки в `linter`  `react-native`

```json
{
  "parser": "@typescript-eslint/parser",
  "extends": [
    "airbnb",
    "airbnb-typescript",
    "@react-native",
    "@feature-sliced/eslint-config/rules/public-api",
    "@feature-sliced/eslint-config/rules/layers-slices"
  ],
  "parserOptions": {
    "project": "tsconfig.json",
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true,
      "legacyDecorators": true
    }
  },
  "plugins": ["@typescript-eslint", "import", "react-native", "simple-import-sort", "react-hooks", "s24"],
  "env": {
    "react-native/react-native": true,
    "jest/globals": true
  },
  "rules": {
    "import/no-internal-modules": [
      "error",
      {
        "allow": ["**/ui/*", "dayjs/locale/**"]
      }
    ],
    "brace-style": ["error", "1tbs", { "allowSingleLine": false }],
    "curly": ["error", "all"],
    "padded-blocks": "off",
    "no-plusplus": "off",
    "arrow-body-style": ["error", "as-needed"],
    "arrow-parens": ["error", "as-needed"],
    "object-shorthand": ["error", "always"],
    "quotes": "off", // managed by prettier
    "object-curly-spacing": ["error", "always"],
    "@typescript-eslint/lines-between-class-members": ["error", "always", { "exceptAfterSingleLine": true }],
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "error",
    "react/jsx-no-target-blank": "off",
    "react/jsx-curly-spacing": ["error", { "when": "never", "children": true }],
    "react/static-property-placement": ["error", "static public field"],
    "react/jsx-fragments": "error",
    "operator-linebreak": ["error", "after", { "overrides": { "?": "ignore", ":": "ignore" } }],
    "no-mixed-operators": ["error", {
      "groups": [
        ["&", "|", "^", "~", "<<", ">>", ">>>"],
        ["==", "!=", "===", "!==", ">", ">=", "<", "<="],
        ["&&", "||"],
        ["in", "instanceof"]
      ],
      "allowSamePrecedence": true
    }],
    "@typescript-eslint/no-unused-expressions": [
      "error",
      {
        "enforceForJSX": true,
        "allowShortCircuit": false,
        "allowTernary": false,
        "allowTaggedTemplates": false
      }
    ],
    "class-methods-use-this": "off",
    "max-len": ["error", 160],
    "max-lines": "error",
    "consistent-return": "off",
    "function-paren-newline": "off",
    "implicit-arrow-linebreak": "off",
    "prefer-destructuring": [
      "error",
      {
        "VariableDeclarator": {
          "array": false,
          "object": true
        },
        "AssignmentExpression": {
          "array": false,
          "object": false
        }
      },
      {
        "enforceForRenamedProperties": false
      }
    ],
    "object-curly-newline": [
      "error",
      {
        "ObjectPattern": {
          "multiline": true,
          "consistent": true
        },
        "ImportDeclaration": {
          "multiline": true,
          "consistent": true
        },
        "ExportDeclaration": {
          "multiline": true,
          "consistent": true
        },
        "ObjectExpression": {
          "multiline": true,
          "consistent": true
        }
      }
    ],
    "@typescript-eslint/comma-dangle": [
      "error",
      {
        "arrays": "always-multiline",
        "objects": "always-multiline",
        "imports": "always-multiline",
        "exports": "always-multiline",
        "enums": "always-multiline",
        "functions": "only-multiline"
      }
    ],
    "react/jsx-wrap-multilines": [
      "error",
      {
        "declaration": "parens",
        "assignment": "parens",
        "return": "parens",
        "arrow": "ignore",
        "condition": "ignore",
        "logical": "ignore",
        "prop": "ignore"
      }
    ],
    "max-classes-per-file": "off",
    "no-console": ["error", { "allow": ["info", "warn", "error"] }],
    "no-param-reassign": "off",
    "no-restricted-syntax": "off",
    "no-underscore-dangle": "off",
    "@typescript-eslint/no-shadow": "off",
    "func-names": ["error", "as-needed"],
    "import/no-extraneous-dependencies": [
      "error",
      {
        "devDependencies": ["src/__tests__/**/*", "e2e/**/*", "metro.config.js"]
      }
    ],
    "import/no-unresolved": [
      "error",
      { 
        "ignore": ["^_", "^app"]
      }
    ],
    "import/no-named-as-default": "off",
    "import/prefer-default-export": "off",
    "import/no-default-export": "error",
    "no-use-before-define": "off",
    "@typescript-eslint/no-use-before-define": ["error", { "functions": false, "variables": false }],
    "simple-import-sort/imports": [
      "error",
      {
        "groups": [
          ["^\\u0000\\.?\\./", "^@?\\w", "^react", "^[a-zA-Z]", "^_screens", "^_widgets", "^_features", "^_entities", "^_shared/", "^\\.\\.", "^\\."]
        ]
      }
    ],
    "@typescript-eslint/array-type": ["error", { "default": "generic" }],
    "@typescript-eslint/consistent-type-assertions": ["error", { "assertionStyle": "as", "objectLiteralTypeAssertions": "never" }],
    "@typescript-eslint/consistent-type-imports": "error",
    "@typescript-eslint/member-delimiter-style": [
      "error",
      {
        "multiline": {
          "delimiter": "semi",
          "requireLast": true
        },
        "singleline": {
          "delimiter": "comma",
          "requireLast": false
        }
      }
    ],
    "@typescript-eslint/no-inferrable-types": ["error", { "ignoreParameters": true }],
    "@typescript-eslint/no-invalid-this": "error",
    "s24/no-magic-numbers": [
      "error",
      {
        "ignoreReadonlyClassProperties": true,
        "ignoreEnums": true,
        "detectObjects": false,
        "ignore": [-1, 0, 1, 2],
        "enforceConst": false,
        "ignoreArrayIndexes": false,
        "ignoreDefaultValues": false
      }
    ],
    "@typescript-eslint/no-require-imports": "error",
    "@typescript-eslint/no-unnecessary-boolean-literal-compare": "error",
    "@typescript-eslint/no-useless-constructor": "error",
    "@typescript-eslint/type-annotation-spacing": "error",
    "react/jsx-filename-extension": "off",
    "react/forbid-prop-types": "off",
    "react/jsx-tag-spacing": [
      "error",
      {
        "closingSlash": "never",
        "beforeSelfClosing": "always",
        "afterOpening": "never",
        "beforeClosing": "never"
      }
    ],
    "react/no-did-update-set-state": "off",
    "react/prop-types": "off",
    "react/sort-comp": "off",
    "react/jsx-one-expression-per-line": "off",
    "react/destructuring-assignment": "off",
    "react/no-unused-prop-types": "off",
    "react/require-default-props": "off",
    "react/no-danger": "off",
    "react/prefer-stateless-function": "off",
    "react/no-array-index-key": "off",
    "react/no-find-dom-node": "off",
    "react/no-children-prop": "off",
    "react/jsx-props-no-spreading": "off",
    "react/state-in-constructor": ["error", "never"],
    "react/jsx-indent": ["error", 2, { "checkAttributes": true, "indentLogicalExpressions": true }],
    "react/jsx-no-bind": ["error", { "allowArrowFunctions": true }],
    "react/jsx-no-useless-fragment": ["error", { "allowExpressions": true }],
    "react/jsx-pascal-case": ["error", { "allowAllCaps": false }],
    "jsx-a11y/click-events-have-key-events": "off",
    "jsx-a11y/no-static-element-interactions": "off",
    "jsx-a11y/anchor-is-valid": "off",
    "jsx-a11y/iframe-has-title": "off",
    "jsx-a11y/anchor-has-content": "off",
    "jsx-a11y/media-has-caption": "off",
    "jsx-a11y/control-has-associated-label": "off",
    "jsx-a11y/no-noninteractive-element-interactions": "off",
    "jsx-a11y/label-has-associated-control": "off",
    "jsx-a11y/label-has-for": "off",
    "react-native/no-unused-styles": "error",
    "react-native/split-platform-components": "error",
    "react-native/no-inline-styles": "error",
    "react-native/no-color-literals": "error",
    "react-native/no-raw-text": ["error", {"skip": ["Text.Text", "TabLabel"]}],
    "react-native/no-single-element-style-arrays": "error",
    "@typescript-eslint/padding-line-between-statements": [
      "error",
      { "blankLine": "always", "prev": "*", "next": ["return", "export", "interface", "type", "enum"] },
      { "blankLine": "always", "prev": ["export", "interface", "type", "enum"], "next": "*" }
  ]
  },
  "overrides": [
    {
      "files": ["./src/__tests__/**", "./e2e/**", "./src/__mocks__/**"],
      "plugins": ["jest"],
      "extends": ["plugin:jest/recommended"],
      "rules": {
        "s24/no-magic-numbers": "off",
        "react/jsx-no-useless-fragment": "off",
        "jest/no-disabled-tests": "warn",
        "jest/no-focused-tests": "error",
        "jest/no-identical-title": "error",
        "jest/prefer-to-have-length": "warn",
        "jest/valid-expect": "error",
        "jest/expect-expect": ["error", { "assertFunctionNames": ["expect", "waitFor"] }]
      }
    }
  ]
}
```