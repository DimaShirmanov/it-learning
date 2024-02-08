Устанавливаем ``babel-plugin-tsconfig-paths-module-resolver``
#### babel.config.js

Добавляем плагин ``tsconfig-paths-module-resolver`` 

```js
module.exports = {
  presets: ["module:metro-react-native-babel-preset"],
  plugins: ["tsconfig-paths-module-resolver", "react-native-reanimated/plugin"],
};
```

#### tsconfig.json

Добавляем в `paths` alias как должны импортироваться файлы 

```json
{
  "extends": "@tsconfig/react-native/tsconfig.json",
  "compilerOptions": {
    "noUnusedLocals": true,
    "noUnusedParameters": true,
    "baseUrl": "src",
    "paths": {
      "_shared/*": ["shared/*"],
      "_entities/*": ["entities/*"],
      "_features/*": ["features/*"],
      "_widgets/*": ["widgets/*"],
      "_screens/*": ["screens/*"],
      "_screens": ["screens"]
    }
  }
}
```