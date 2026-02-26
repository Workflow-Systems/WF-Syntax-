# Файл стилей

Файл стилей позволяет отделить детали дизайна от структуры и поведения пользовательского интерфейса. К деталям дизайна относятся стили объектов формы, цвета и стили шрифтов.

Стили, цвета и шрифты можно указать в xml-файле формы, в таком случае они доступны только на этой форме. Если их вынести в файл стилей, то они будут доступны для всех форм в проекте.

Файл ресурсов стиля обычно называется style.wstl и должен располагаться в папке \Forms\Styles.

Пример кода файла стилей:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<Appearance>
  <Colors>
    <Color Name="LightGreen" Red="194" Green="230" Blue="224" Alpha="255" />
    <Color Name="LightYellow" Red="255" Green="255" Blue="213" Alpha="255" />
  </Colors>

  <FontStyles>
    <FontStyle Name="HeadFontStyle" Font="Segoe UI" Size="15" />
    <FontStyle Name="LabelFontStyle" Font="Segoe UI" Size="9" Italic="True" />
  </FontStyles>

  <Styles>
    <MessageBoxStyle Name="DefaultMessageBoxStyle" Default="True">
      <DelimeterStartForeColor>LightGreen</DelimeterStartForeColor>
    </MessageBoxStyle>
  </Styles>
</Appearance>
```

Корневым тэгом является тэг [`<Appearance>`](workflow_forms/appearance.md), который полностью соответствует такому же тэгу в xml-файле формы. Вложенные тэги:

* `<Colors>` - список необязательных тэгов [`<Color>`](workflow_forms/appearance.md#color), описывающих цвета.
* `<FontStyles>` - список необязательных тэгов [`<FontStyle>`](workflow_forms/appearance.md#font_style), описывающих стили шрифтов.
* `<Styles>` - список необязательных тэгов [`<MessageBoxStyle>`](workflow_forms/appearance.md#message_box_style), описывающих стили диалоговых окон.

При запуске клиентской части программы считывает содержимое файла стилей и формирует словари для цветов, шрифтов и стилей. Когда открывается форма словари копируются и в них добавляются значения из файла формы. Если в xml-файле формы описан цвет, шрифт или стиль с таким же именем, то значение в словаре будет заменено.
