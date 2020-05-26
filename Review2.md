Здравствуйте!

С Api все получилось хорошо, но вы несколько изменили класс UserInfo и он перестал отвечать требованиям.

## Надо исправить

- Все комментарии в коде UserInfo

## Можно лучше

- Повторяющийся код

      .then((res) => {
        if (res.ok) {
          return res.json()
        }
        return Promise.reject(res)
      })
      .catch((err) => {
        return Promise.reject(new Error(`Ошибка: ${err.message}`))
      });

Можно вынести в отдельный метод и использовать для проверки ответа его

## Промежуточный итог

Api хороший, все сделали верно, почините UserInfo и с удовольствием приму работу!