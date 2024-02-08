**Link:** **[react-hook-form](https://github.com/react-hook-form/react-hook-form)**

**Установка** 

```
npm install react-hook-form
```

**Использование**

**LoginScreen.tsx**

```ts
import type { SubmitHandler } from "react-hook-form";
import { useForm } from "react-hook-form";

interface Inputs {
  username: string;
  password: string;
}

const {
    control,
    handleSubmit,
  } = useForm<Inputs>({
    mode: "all",
    reValidateMode: "onChange",
    defaultValues: {
      username: "",
      password: "",
    },
  });

  const onSubmit: SubmitHandler<Inputs> = async ({ username, password }) => {
    try {
		// Code
    } finally {
    }
	  };
```

Создаем форму через `useForm`, также передаем `Inputs` для типизации