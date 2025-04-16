# shtango
Shtango (a parody of Django) web framework for Kumir2 with Kumir-Compose


### Basic controller

```1с
|| включить "shtango/macros"

алг нач
штанго_контроллер
штанго_ответ_шаблоном("200", "templates/index.html", новыйОбъект)
кон

|| включить "shtango/core"
|| включить "shtango/templating"
```

### Template for registration

```1с
|| включить "shtango/macros"

алг нач
штанго_контроллер
если Метод = "GET" то
    штанго_ответ_шаблоном("200", "templates/register.html", новыйОбъект)
    выход
все
лит форма
форма := декодировать_urlencode(Тело)
| тут надо сходить в базу
штанго_ответ_шаблоном("200", "templates/success-reg.html", форма)
кон

|| включить "shtango/core"
|| включить "shtango/validation"
|| включить "shtango/templating"
|| включить "shtango/urlencode"
```

[Learn more at example_web project at kumir-compose/compose](https://github.com/kumir-compose/compose)
