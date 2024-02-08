#### Установка 

`npm install eslint-plugin-simple-import-sort --save-dev`

#### .eslintrc.json

```json
{
	"rules": {
	"simple-import-sort/imports": [
      "error",
      {
        "groups": [
          [
          "^\\u0000\\.?\\./", 
          "^@?\\w", 
          "^react", 
          "^[a-zA-Z]", 
          "^_screens", 
          "^_widgets", 
          "^_features", 
          "^_entities", 
          "^_shared/",
          "^\\.\\.", 
          "^\\."
          ]
        ]
      }
    ],
}
}
```