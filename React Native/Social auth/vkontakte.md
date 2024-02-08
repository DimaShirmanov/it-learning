
**Устанавливаем библиотеку**

```
npm i react-native-vkontakte-login
```

**Следующим шагом нужно сделать инициализацию**

```tsx
useEffect(() => {
	VKLogin.initialize(Config.VK_ID);
}, [])
```

**Теперь можем делать авторизацию**

```tsx
  const signWithVk = async () => {
    try {
      if (await VKLogin.isLoggedIn()) {
        await VKLogin.logout();
      }

      const response = await VKLogin.login(["email"]);
      if (response.access_token && response.user_id) {
        const { accessToken, refreshToken } = await authorizationService.exchangeVk({
          token: response.access_token,
          userId: response.user_id,
          email: response.email || undefined,
        });
      }
    } finally {
    }
  };
```

Тут мы делаем авторизацию, запрашиваем через массив дополнительные данные и если все успешно, то получаем `access_token` и другие данные от пользователя.
Следующим шагом мы должны на наш бек отправить `access_token` и в ответ получить `accessToken, refreshToken`.

**Mock библиотеки JEST**

```js
jest.mock("react-native-vkontakte-login", () => ({
  _esModule: true,
  default: "VkLogin",
  namedExport: jest.fn(),
}));
```
