---
description: Команда; устанавливает локаль и язык перевода для всего приложения.
---

# LocaleSetCommand

## Шаблон LocaleSetCommand <a href="#template_locale_set_command" id="template_locale_set_command"></a>

```xml
<Command Name="" Type="LocaleSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для LocaleSetCommand-->
  <Locale></Locale>
</Command>
```

## Описание LocaleSetCommand <a href="#description_locale_set_command" id="description_locale_set_command"></a>

```xml
<Command Name="LocaleSetCommandName" Type="LocaleSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для LocaleSetCommand-->
</Command>
```

### Результат выполнения LocaleSetCommand <a href="#result_locale_set_command" id="result_locale_set_command"></a>

Команда не имеет результата.

## Тэги, специфичные для LocaleSetCommand <a href="#tags_locale_set_command" id="tags_locale_set_command"></a>

### Locale <a href="#locale" id="locale"></a>

Локаль.

Обязательный тэг. Ожидается код одной из локалей, поддерживаемых Windows.

Полный список всех кодов локалей можно посмотреть по [ссылке](https://msdn.microsoft.com/en-us/library/cc233982.aspx).

```xml
<Locale>ru-RU</Locale>
```
