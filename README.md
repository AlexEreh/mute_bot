# Бот АнтиФёдор

![CI](https://github.com/AlexEreh/mute_bot/actions/workflows/ci.yml/badge.svg)
[![codecov](https://codecov.io/gh/AlexEreh/mute_bot/branch/master/graph/badge.svg)](https://codecov.io/gh/AlexEreh/mute_bot)

## Что умеет этот бот
* Мутить по команде `/mute amount unit`, 
где amount и unit отвечают за количество времени 
и единицу его измерения соответственно. 
Для выполнения команды пользователь должен иметь права администратора в группе, 
а пользователь которого требуется замутить их иметь не должен. 
Сообщение о муте должно быть ответом на сообщение, 
которое свою очередь является пересланным сообщением.
`amount` - величина в единицах unit.
  Целое число.
`unit` - единица измерения времени.
  Доступные варианты единиц измерения:
  * Часы - `h`, `hours`, `ч`
  * Минуты - `m`, `minutes`, `м`
  * Секунды - `s`, `seconds`, `с`

* Размутить пользователя по команде `/unmute`. 
Требования у команды аналогичны команде `/mute`.
* Вывод справки о командах по `/help`.

## Перед использованием
**Убедитесь, что в файле `Secrets.toml` написан токен телеграм-бота.**

### Пример
```toml
TELOXIDE_TOKEN = 'токен'
```

## Стек технологий
* [Rust](https://www.rust-lang.org/) - language of utterly deranged.
* [Shuttle](https://www.shuttle.rs) - инструмент для быстрого написания бэкендов для Rust. 
* [Teloxide](https://github.com/teloxide/teloxide) - достаточно простой фреймворк для написания 
телеграм ботов с помощью языка Rust.
* [chrono](https://crates.io/crates/chrono) - крейт для работы с единицами измерения времени.
