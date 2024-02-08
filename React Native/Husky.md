
Устанавливаем [https://typicode.github.io/husky/](Husky.md)

```
npm i husky
```

Создаем папку 

```
mkdir husky
```

Создаем файл `pre-commit` для проверок перед коммитом

```sh
#!/bin/sh
. "$(dirname "$0")/_/husky.sh"

npm run pretest:ci
```

Данный код будет запускать `pretest:ci` каждый раз перед коммитом