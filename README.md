---
description: Описание структуры xml-файла формы, основных тэгов и свойств формы
---

# Form.xml

## Краткий шаблон Form <a href="#short_template" id="short_template"></a>

```xml
<?xml version="1.0"?>
<Form Name="" Title="" Top="" Left="" Height="" Width="" StartPosition="" FontStyle="" ForeColor="" StatusBar="" AsteriskForeColor="" AsteriskFontStyle="" TabAutoSelect="">
  <!--Тэги, специфичные для Form-->
  <Appearance></Appearance>
  <Parameters></Parameters>
  <DataConnections></DataConnections>
  <Conditions></Conditions>
  <Commands></Commands>
  <Executions></Executions>
  <Checkings></Checkings>
  <MainMenu></MainMenu>
  <ContextMenus></ContextMenus>
  <MyObjects></MyObjects>
</Form>
```

## Полный шаблон Form <a href="#full_template" id="full_template"></a>

```xml
<?xml version="1.0"?>
<Form Name="" Title="" Top="" Left="" Height="" Width="" HorizontalAlign="" VerticalAlign="" StartPosition="" FormState="" AutoScroll="" FontStyle="" ForeColor="" BackColor="" TransparencyColor="" BackgroundImage="" StatusBar="" DiagMessage="" FormBorderStyle="" ControlBox="" MinimizeBox="" MaximizeBox="" ShowInTaskbar="" TopMost="" Opacity="" KeyPreview="" ValidationType="" FlatColor="" FlatWidth="" AsteriskForeColor="" AsteriskFontStyle="" EnableWaitingAnimation="" EnableWaitingAnimationWhileActive="" RestoreLastFormState="" Icon="" TabAutoSelect="">
  <!--Тэги, специфичные для Form-->
  <StartLocale></StartLocale>
  <Appearance></Appearance>
  <Includes></Includes>
  <Parameters></Parameters>
  <DataConnections></DataConnections>
  <Conditions></Conditions>
  <Commands></Commands>
  <Executions></Executions>
  <Checkings></Checkings>
  <MainMenu></MainMenu>
  <ContextMenus></ContextMenus>
  <MyObjects></MyObjects>
</Form>
```

## Описание Form <a href="#description" id="description"></a>

Тэг `<Form>` - корневой элемент файла формы.

```xml
<Form Name=""
      Title=""
      Top=""
      Left=""
      Height=""
      Width=""
      TotalHeight=""
      TotalWidth=""
      HorizontalAlign=""
      VerticalAlign=""
      StartPosition=""
      AutoScroll=""
      FontStyle=""
      ForeColor=""
      BackColor=""
      TransparencyColor=""
      BackgroundImage=""
      StatusBar=""
      DiagMessage=""
      FormBorderStyle=""
      ControlBox=""
      MinimizeBox=""
      MaximizeBox=""
      ShowInTaskbar=""
      TopMost=""
      Opacity=""
      AsteriskForeColor=""
      AsteriskFontStyle=""
      EnableWaitingAnimation=""
      EnableWaitingAnimationWhileActive=""
      RestoreLastFormState=""
      Icon=""
      TabAutoSelect="">
  <!--Тэги, специфичные для Form-->
</Form>
```

## Атрибуты Form <a href="#attributes" id="attributes"></a>

### Name

Системное имя формы.

Обязательный атрибут. Любое значение будет переведено в текстовое.

### Title

Заголовок формы.

Необязательный атрибут. Любое значение будет переведено в текстовое.

### Top

Координата расположения формы по высоте (сверху вниз).

Необязательный атрибут. Ожидается целочисленное значение.

Если атрибут `Top` отсутствует и если косвенно атрибуты [`StartPosition`](./#start_position), [`HorizontalAlign`](./#horizontal_align) и [`VerticalAlign`](./#vertical_align) (в порядке значимости) тоже не определяет его значение, то используется стандартное значение .NET.

### Left

Координата расположения формы по ширине (слева направо).

Необязательный атрибут. Ожидается целочисленное значение.

Если атрибут `Left` отсутствует и если косвенно атрибуты [`StartPosition`](./#start_position), [`HorizontalAlign`](./#horizontal_align) и [`VerticalAlign`](./#vertical_align) (в порядке значимости) тоже не определяет его значение, то используется стандартное значение .NET.

### Height

Высота рабочей области формы (то есть кайма формы сюда не входит).

Необязательный атрибут. Ожидается целочисленное значение.

При задании одновременно двух атрибутов `Height` и [`TotalHeight`](./#total_height) приоритет имеет `TotalHeight`. Если атрибут `Height` отсутствует, то используется стандартное значение .NET.

### Width

Ширина рабочей области формы (то есть кайма формы сюда не входит).

Необязательный атрибут. Ожидается целочисленное значение.

При задании одновременно двух атрибутов `Width` и [`TotalWidth`](./#total_width) приоритет имеет `TotalWidth`. Если атрибут `Width` отсутствует, то используется стандартное значение .NET.

### TotalHeight <a href="#total_height" id="total_height"></a>

Полная высота формы (с учетом каймы).

Необязательный атрибут. Ожидается целочисленное значение.

При задании одновременно двух атрибутов [`Height`](./#height) и `TotalHeight` приоритет имеет `TotalHeight`. Если атрибут `TotalHeight` отсутствует, то используется стандартное значение .NET.

### TotalWidth <a href="#total_width" id="total_width"></a>

Полная ширина формы (с учетом каймы).

Необязательный атрибут. Ожидается целочисленное значение.

При задании одновременно двух атрибутов [`Width`](./#width) и `TotalWidth` приоритет имеет `TotalWidth`. Если атрибут `TotalWidth` отсутствует, то используется стандартное значение .NET.

### HorizontalAlign <a href="#horizontal_align" id="horizontal_align"></a>

Тип положения формы по горизонтали.

Необязательный атрибут. Ожидается название одного из типов положения формы по горизонтали:

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Left</td><td>Левой границей формы к краю левой части экрана</td></tr><tr><td align="center">Center</td><td>По центру</td></tr><tr><td align="center">Right</td><td>Правой границей формы к краю правой части экрана</td></tr></tbody></table>

Если атрибут `HorizontalAlign` отсутствует, то значение определяется через атрибуты [`StartPosition`](./#start_position) и [`Left`](./#left) (в порядке значимости).

### VerticalAlign <a href="#vertical_align" id="vertical_align"></a>

Тип положения формы по вертикали.

Необязательный атрибут. Ожидается название одного из типов положения формы по вертикали:

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Top</td><td>Верхней границей формы к краю верхней части экрана</td></tr><tr><td align="center">Center</td><td>Посередине</td></tr><tr><td align="center">Bottom</td><td>Нижней границей формы к краю нижней части экрана</td></tr></tbody></table>

Если атрибут `VerticalAlign` отсутствует, то значение определяется через атрибуты [`StartPosition`](./#start_position) и [`Top`](./#top) (в порядке значимости).

### StartPosition <a href="#start_position" id="start_position"></a>

Тип положения формы на экране.

Необязательный атрибут. Ожидается название одного из типов положения формы на экране:

<table data-header-hidden data-full-width="false"><thead><tr><th width="335" align="center"></th><th width="602.3333333333333"></th></tr></thead><tbody><tr><td align="center">Manual</td><td>Положение формы определяется атрибутами <a href="./#horizontal_align"><code>HorizontalAlign</code></a>, <a href="./#vertical_align"><code>VerticalAlign</code></a>, <a href="./#top"><code>Top</code></a> и <a href="./#left"><code>Left</code></a> (в порядке значимости)</td></tr><tr><td align="center">CenterScreen</td><td>Форма с заданными размерами располагается в центре текущего отображения</td></tr><tr><td align="center">WindowsDefaultLocation</td><td>Форма с заданными размерами размещается в расположении, определенном по умолчанию в операционной системе</td></tr><tr><td align="center">WindowsDefaultBounds</td><td>Положение формы и ее границы определены в операционной системе по умолчанию</td></tr><tr><td align="center">CenterParent</td><td>Форма располагается в центре родительской формы</td></tr></tbody></table>

Если атрибут `StartPosition` отсутствует, то значение определяется через атрибуты [`HorizontalAlign`](./#horizontal_align), [`VerticalAlign`](./#vertical_align), [`Top`](./#top) и [`Left`](./#left) (в порядке значимости), либо как значение WindowsDefaultLocation.

### FormState <a href="#form_state" id="form_state"></a>

Тип состояния формы.

Необязательный атрибут. Ожидается название одного из типов состояния формы:

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Minimized</td><td>Форма свернута в панель задач (данное значение можно задать только через set-проперти в процессе работы формы)</td></tr><tr><td align="center">Maximized</td><td>Форма развернута на весь экран</td></tr><tr><td align="center">Normal</td><td>Обычное положение формы: ни свернута в панель задач, ни развернута на весь экран</td></tr></tbody></table>

Если атрибут `FormState` отсутствует, то используется значение Normal.

### AutoScroll <a href="#auto_scroll" id="auto_scroll"></a>

Признак, определяющий, показывать ли полосы прокрутки на форме, если объекты не входят в ее рабочую область.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

### FontStyle <a href="#font_style" id="font_style"></a>

Имя стиля шрифта формы по умолчанию.

Необязательный атрибут. Ожидается имя одного из стилей шрифтов, описанных в форме.

По умолчанию используется стандартное значение .NET.

### ForeColor <a href="#fore_color" id="fore_color"></a>

Имя цвета текста формы по умолчанию.

Необязательный атрибут. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

### BackColor <a href="#back_color" id="back_color"></a>

Имя цвета фона формы.

Необязательный атрибут. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

### TransparencyColor <a href="#transparency_color" id="transparency_color"></a>

Имя цвета, который форма будет определять как прозрачный.

Необязательный атрибут. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

### BackgroundImage <a href="#background_image" id="background_image"></a>

Путь до файла с графическим содержанием, которое будет расположено на форме.

Необязательный атрибут. Любое значение будет переведено в текстовое.

### StatusBar <a href="#status_bar" id="status_bar"></a>

Признак отображения бара событий формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

### DiagMessage <a href="#diag_message" id="diag_message"></a>

Признак показа диагностического сообщения с результатами загрузки сущностей формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

### FormBorderStyle <a href="#form_border_style" id="form_border_style"></a>

Тип границ формы.

Необязательный атрибут. Ожидается название одного из типов границы формы:

<table data-header-hidden><thead><tr><th width="316" align="center"></th><th width="436.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет границы</td></tr><tr><td align="center">FixedSingle</td><td>Фиксированная граница из одной линии</td></tr><tr><td align="center">Fixed3D</td><td>Фиксированная трехмерная граница</td></tr><tr><td align="center">FixedDialog</td><td>Толстая фиксированная граница стиля диалогового окна</td></tr><tr><td align="center">Sizable</td><td>Граница с изменяемыми размерами</td></tr><tr><td align="center">FixedToolWindow</td><td>Неизменяемая граница окна инструментов (окно инструментов не отображается ни на панели задач, ни в окне, появляющемся при нажатии пользователем сочетания клавиш ALT+TAB)</td></tr><tr><td align="center">SizableToolWindow</td><td>Изменяемая граница окна инструментов (окно инструментов не отображается ни на панели задач, ни в окне, появляющемся при нажатии пользователем сочетания клавиш ALT+TAB)</td></tr></tbody></table>

По умолчанию используется значение FixedSingle.

### ControlBox <a href="#control_box" id="control_box"></a>

Признак, определяющий, отображаются или нет кнопки оконного меню в строке заголовка формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### MinimizeBox <a href="#minimize_box" id="minimize_box"></a>

Признак, определяющий, отображается ли кнопка свертывания в строке заголовка формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### MaximizeBox <a href="#maximize_box" id="maximize_box"></a>

Признак, определяющий, отображается ли кнопка развертывания в строке заголовка формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### ShowInTaskbar <a href="#show_in_taskbar" id="show_in_taskbar"></a>

Признак, определяющий, отображается ли форма в панели задач.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### TopMost <a href="#top_most" id="top_most"></a>

Признак, определяющий, необходимо ли отображать форму как форму переднего плана.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

### Opacity

Уровень непрозрачности формы.

Необязательный атрибут. Ожидается числовое значение (от 0 до 1).

По умолчанию используется значение 1.

### KeyPreview <a href="#key_preview" id="key_preview"></a>

Признак, определяющий, будет ли форма получать события нажатия клавиш с объектов, на ней расположенных.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### ValidationType <a href="#validation_type" id="validation_type"></a>

Вид `Checking` формы.

Необязательный атрибут. Ожидается название одного из типов `Checking`:

<table data-header-hidden><thead><tr><th align="center"></th><th width="471.3333333333333"></th></tr></thead><tbody><tr><td align="center">Asterisk</td><td>"Звёздочка" справа от объекта</td></tr><tr><td align="center">Flat</td><td>Полоска слева от объекта</td></tr></tbody></table>

По умолчанию используется значение Asterisk.

### FlatWidth <a href="#flat_width" id="flat_width"></a>

Ширина цвета полосы `Checking` формы.

Необязательный атрибут. Ожидается числовое значение.

По умолчанию используется значение 3.

### FlatColor <a href="#flat_color" id="flat_color"></a>

Имя цвета полосы `Checking` формы.

Необязательный атрибут. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется красный цвет.

### AsteriskForeColor <a href="#asterisk_fore_color" id="asterisk_fore_color"></a>

Имя цвета "звездочки" формы.

Необязательный атрибут. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET для надписи.

### AsteriskFontStyle <a href="#asterisk_font_style" id="asterisk_font_style"></a>

Имя стиля шрифта "звездочки" формы.

Необязательный атрибут. Ожидается имя одного из стилей шрифтов, описанных в форме.

По умолчанию используется стандартное значение .NET для надписи.

### EnableWaitingAnimation <a href="#enable_waiting_animation" id="enable_waiting_animation"></a>

Признак, определяющий, будет ли отображаться форма с анимацией.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### EnableWaitingAnimationWhileActive <a href="#enable_waiting_animation_while_active" id="enable_waiting_animation_while_active"></a>

Признак, определяющий, что форма с анимацией будет отображаться только тогда, когда окно активно.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

### RestoreLastFormState <a href="#restore_last_form_state" id="restore_last_form_state"></a>

Признак, определяющий, будет ли восстановлено предыдущее состояние формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение True.

### Icon

Путь до файла иконки.

Необязательный атрибут. Любое значение будет переведено в текстовое.

### TabAutoSelect <a href="#tab_auto_select" id="tab_auto_select"></a>

Признак, определяющий, будет ли выполняться автоматическая установка фокуса в первом элементе управления при запуске формы.

Необязательный атрибут. Ожидается логическое значение.

По умолчанию используется значение False.

## Тэги, специфичные для Form <a href="#specific-tags" id="specific-tags"></a>

### StartLocale <a href="#start_locale" id="start_locale"></a>

Единоразово устанавливает локаль и язык перевода для всего приложения при загрузке формы.

Необязательный тэг. Ожидается код одной из локалей, поддерживаемых Windows.

Если тэг `<StartLocale>` отсутствует, то для приложения устанавливается язык операционной системы пользователя.

Полный список всех кодов локалей можно посмотреть по [ссылке](https://msdn.microsoft.com/en-us/library/cc233982.aspx).

{% hint style="warning" %}
Установка локали происходит только один раз в момент загрузки формы, любое изменение универсального значения внутри (например, [`DataConnection`](workflow_forms/dataconnections/)) язык приложения не изменяет.
{% endhint %}

```xml
<StartLocale></StartLocale>
```

### Appearance <a href="#appearance" id="appearance"></a>

Содержит графические настройки отображения формы.

Необязательный тэг. Значение тэга `<Appearance>`: см. в разделе [Appearance](workflow_forms/appearance.md).

```xml
<Appearance></Appearance>
```

### Includes <a href="#includes" id="includes"></a>

Содержит документы, содержимое которых будет включено в текущий документ.

Необязательный тэг. Значение тэга `<Includes>`: см. в разделе [Includes](workflow_forms/includes.md).

```xml
<Includes></Includes>
```

### Parameters <a href="#parameters" id="parameters"></a>

Содержит описание параметров формы.

Необязательный тэг. Значение тэга `<Parameters>`: см. в разделе [Parameters](workflow_forms/parameters.md).

```xml
<Parameters></Parameters>
```

### DataConnections <a href="#data_connections" id="data_connections"></a>

Содержит описание соединений с данными.

Необязательный тэг. Значение тэга `<DataConnections>`: см. в разделе [DataConnections](workflow_forms/dataconnections/).

```xml
<DataConnections></DataConnections>
```

### Conditions <a href="#conditions" id="conditions"></a>

Содержит описание условий.

Необязательный тэг. Значение тэга `<Conditions>`: см. в разделе [Conditions](workflow_forms/conditions/).

```xml
<Conditions></Conditions>
```

### Commands <a href="#commands" id="commands"></a>

Содержит описание команд.

Необязательный тэг. Значение тэга `<Commands>`: см. в разделе [Commands](workflow_forms/commands/).

```xml
<Commands></Commands>
```

### Executions <a href="#executions" id="executions"></a>

Содержит описание действий.

Необязательный тэг. Значение тэга `<Executions>`: см. в разделе [Executions](workflow_forms/executions.md).

```xml
<Executions></Executions>
```

### Checkings <a href="#checkings" id="checkings"></a>

Содержит описание проверок.

Необязательный тэг. Значение тэга `<Checkings>`: см. в разделе [Checkings](workflow_forms/checkings.md).

```xml
<Checkings></Checkings>
```

### MainMenu <a href="#main_menu" id="main_menu"></a>

Содержит описание главного меню формы.

Необязательный тэг. Значение тэга `<MainMenu>`: см. в разделе [Menus](workflow_forms/menus/).

```xml
<MainMenu></MainMenu>
```

### ContextMenus <a href="#context_menus" id="context_menus"></a>

Содержит описание контекстных меню формы.

Необязательный тэг. Значение тэга `<ContextMenus>`: см. в разделе [Menus](workflow_forms/menus/).

```xml
<ContextMenus></ContextMenus>
```

### MyObjects <a href="#my_objects" id="my_objects"></a>

Содержит описание объектов формы.

Необязательный тэг. Значение тэга `<MyObjects>`: см. в разделе [Objects](workflow_forms/objects/).

```xml
<MyObjects></MyObjects>
```

## Get-проперти для получения свойств <a href="#get_properties" id="get_properties"></a>

### Title <a href="#get_title" id="get_title"></a>

Возвращает заголовок формы.

```xml
<Form>
  <Property Name="Title" />
</Form>
```

### Top <a href="#get_top" id="get_top"></a>

Возвращает координату расположения формы по высоте (сверху вниз).

```xml
<Form>
  <Property Name="Top" />
</Form>
```

### Left <a href="#get_left" id="get_left"></a>

Возвращает координату расположения формы по ширине (слева направо).

```xml
<Form>
  <Property Name="Left" />
</Form>
```

### Height <a href="#get_height" id="get_height"></a>

Возвращает высоту рабочей области формы (то есть кайма формы сюда не входит).

```xml
<Form>
  <Property Name="Height" />
</Form>
```

### Width <a href="#get_width" id="get_width"></a>

Возвращает ширину рабочей области формы (то есть кайма формы сюда не входит).

```xml
<Form>
  <Property Name="Width" />
</Form>
```

### TotalHeight <a href="#get_total_height" id="get_total_height"></a>

Возвращает полную высоту формы (с учетом каймы).

```xml
<Form>
  <Property Name="TotalHeight" />
</Form>
```

### TotalWidth <a href="#get_total_width" id="get_total_width"></a>

Возвращает полную ширину формы (с учетом каймы).

```xml
<Form>
  <Property Name="TotalWidth" />
</Form>
```

### FormState <a href="#get_form_state" id="get_form_state"></a>

Возвращает тип состояния формы.

```xml
<Form>
  <Property Name="FormState" />
</Form>
```

### AutoScroll <a href="#get_auto_scroll" id="get_auto_scroll"></a>

Возвращает признак, определяющий, показываются ли полосы прокрутки на форме, если объекты не входят в ее рабочую область.

```xml
<Form>
  <Property Name="AutoScroll" />
</Form>
```

### FontStyle <a href="#get_font_style" id="get_font_style"></a>

Возвращает имя стиля шрифта формы по умолчанию.

```xml
<Form>
  <Property Name="FontStyle" />
</Form>
```

### ForeColor <a href="#get_fore_color" id="get_fore_color"></a>

Возвращает имя цвета текста формы по умолчанию.

```xml
<Form>
  <Property Name="ForeColor" />
</Form>
```

### BackColor <a href="#get_back_color" id="get_back_color"></a>

Возвращает имя цвета фона формы.

```xml
<Form>
  <Property Name="BackColor" />
</Form>
```

### TransparencyColor <a href="#get_transparency_color" id="get_transparency_color"></a>

Возвращает имя цвета, который форма определяет как прозрачный.

```xml
<Form>
  <Property Name="TransparencyColor" />
</Form>
```

### BackgroundImage <a href="#get_background_image" id="get_background_image"></a>

Возвращает путь до файла с графическим содержанием, которое расположено на форме.

```xml
<Form>
  <Property Name="BackgroundImage" />
</Form>
```

### StatusBar <a href="#get_status_bar" id="get_status_bar"></a>

Возвращает признак отображения бара событий формы.

```xml
<Form>
  <Property Name="StatusBar" />
</Form>
```

### DiagMessage <a href="#get_diag_message" id="get_diag_message"></a>

Возвращает признак показа диагностического сообщения с результатами загрузки сущностей формы.

```xml
<Form>
  <Property Name="DiagMessage" />
</Form>
```

### FormBorderStyle <a href="#get_form_border_style" id="get_form_border_style"></a>

Возвращает тип границ формы.

```xml
<Form>
  <Property Name="FormBorderStyle" />
</Form>
```

### ControlBox <a href="#get_control_box" id="get_control_box"></a>

Возвращает признак, определяющий, отображаются или нет кнопки оконного меню в строке заголовка формы.

```xml
<Form>
  <Property Name="ControlBox" />
</Form>
```

### MinimizeBox <a href="#get_minimize_box" id="get_minimize_box"></a>

Возвращает признак, определяющий, отображается ли кнопка свертывания в строке заголовка формы.

```xml
<Form>
  <Property Name="MinimizeBox" />
</Form>
```

### MaximizeBox <a href="#get_maximize_box" id="get_maximize_box"></a>

Возвращает признак, определяющий, отображается ли кнопка развертывания в строке заголовка формы.

```xml
<Form>
  <Property Name="MaximizeBox" />
</Form>
```

### ShowInTaskbar <a href="#get_show_in_taskbar" id="get_show_in_taskbar"></a>

Возвращает признак, определяющий, отображается ли форма в панели задач.

```xml
<Form>
  <Property Name="ShowInTaskbar" />
</Form>
```

### TopMost <a href="#get_top_most" id="get_top_most"></a>

Возвращает признак, определяющий, отображается ли форма как форма переднего плана.

```xml
<Form>
  <Property Name="TopMost" />
</Form>
```

### Opacity <a href="#get_opacity" id="get_opacity"></a>

Возвращает уровень непрозрачности формы.

```xml
<Form>
  <Property Name="Opacity" />
</Form>
```

### KeyPreview <a href="#get_key_preview" id="get_key_preview"></a>

Возвращает признак, определяющий, получает ли форма события нажатия клавиш с объектов, на ней расположенных.

```xml
<Form>
  <Property Name="KeyPreview" />
</Form>
```

### LastKeys <a href="#get_last_keys" id="get_last_keys"></a>

Возвращает строку, содержащую символы, соответствующие последним нажатым клавишам (при условии, что атрибут`KeyPreview` формы имеет значение True).

Например, возвращаемые значения могут выглядеть следующим образом:

1. A
2. A, B
3. AB
4. Ctrl + A
5. Ctrl + A + B
6. Ctrl + A + B, Shift + C
7. Ctrl+Alt + A, Alt+Shift + B
8. Ctrl+Alt+Shift + A, Alt+Shift + B + C
9. И другие варианты

```xml
<Form>
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="LastKeys">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается целочисленное значение-->
      <!--Количество последних нажатых клавиш (не более 1024), которые могут запоминаться в данном проперти-->
      <Parameter Name="Value">5</Parameter>
      <!--Cтрока-разделитель, вставляемая в запись между нажатыми клавишами. Например, при разделителе ", " проперти будет возвращать "A, B"-->
      <!--Необязательный параметр. При отсутствии используется значение ""-->
      <!--Значение тэга Parameter с атрибутом Name, равным KeySeparator: любое значение будет переведено в текстовое-->
      <Parameter Name="KeySeparator">, </Parameter>
      <!--Признак, определяющий, каким образом будут выведены клавиши "1", "2" и другие цифры и "Enter" - как "D1", "D2" и т. д. и "Return" (оригинальный вид) или как "1", "2" и т. д. и "\r"-->
      <!--Необязательный параметр. При отсутствии используется значение "False"-->
      <!--Значение тэга Parameter с атрибутом Name, равным KeyOriginal: ожидается логическое значение-->
      <Parameter Name="KeyOriginal">False</Parameter>
      <!--Признак, определяющий, будет ли проперти возвращать сочетания с участием клавиши-модификатора Ctrl-->
      <!--Необязательный параметр. При отсутствии используется значение "False"-->
      <!--Значение тэга Parameter с атрибутом Name, равным CtrlHandling: ожидается логическое значение-->
      <Parameter Name="CtrlHandling">False</Parameter>
      <!--Признак, определяющий, будет ли проперти возвращать сочетания с участием клавиши-модификатора Alt-->
      <!--Необязательный параметр. При отсутствии используется значение "False"-->
      <!--Значение тэга Parameter с атрибутом Name, равным AltHandling: ожидается логическое значение-->
      <Parameter Name="AltHandling">False</Parameter>
      <!--Признак, определяющий, будет ли проперти возвращать сочетания с участием клавиши-модификатора Shift-->
      <!--Необязательный параметр. При отсутствии используется значение "False"-->
      <!--Значение тэга Parameter с атрибутом Name, равным ShiftHandling: ожидается логическое значение-->
      <Parameter Name="ShiftHandling">False</Parameter>
    </Parameters>
  </Property>  
</Form>
```

### AsteriskForeColor <a href="#get_asterisk_fore_color" id="get_asterisk_fore_color"></a>

Возвращает имя цвета "звездочки" формы.

```xml
<Form>
  <Property Name="AsteriskForeColor" />
</Form>
```

### AsteriskFontStyle <a href="#get_asterisk_font_style" id="get_asterisk_font_style"></a>

Возвращает имя стиля шрифта "звездочки" формы.

```xml
<Form>
  <Property Name="AsteriskFontStyle" />
</Form>
```

### DateTimeNow <a href="#get_date_time_now" id="get_date_time_now"></a>

Возвращает рабочую дату и время формы, определенную первый раз в момент открытия формы.

```xml
<Form>
  <Property Name="DateTimeNow" />
</Form>
```

### FormChanged <a href="#get_form_changed" id="get_form_changed"></a>

Возвращает признак изменения формы (определяется как совокупность get-проперти `ValueChanged` объектов на форме).

```xml
<Form>
  <Property Name="FormChanged" />
</Form>
```

### EnableWaitingAnimation <a href="#get_enable_waiting_animation" id="get_enable_waiting_animation"></a>

Возвращает признак, определяющий, отображается ли форма с анимацией.

```xml
<Form>
  <Property Name="EnableWaitingAnimation" />
</Form>
```

### EnableWaitingAnimationWhileActive <a href="#get_enable_waiting_animation_while_active" id="get_enable_waiting_animation_while_active"></a>

Возвращает признак, определяющий, что форма с анимацией отображается только тогда, когда окно активно.

```xml
<Form>
  <Property Name="EnableWaitingAnimationWhileActive" />
</Form>
```

### RestoreLastFormState <a href="#get_restore_last_form_state" id="get_restore_last_form_state"></a>

Возвращает признак, определяющий, восстанавливается ли предыдущее состояние формы.

```xml
<Form>
  <Property Name="RestoreLastFormState" />
</Form>
```

### ChangedObjects <a href="#get_changed_objects" id="get_changed_objects"></a>

Возвращает список изменённых объектов.

```xml
<Form>
  <Property Name="ChangedObjects" />
</Form>
```

### CheckingFired <a href="#get_checking_fired" id="get_checking_fired"></a>

Возвращает признак, определяющий, сработал ли хоть один [`<Checking>`](./#checkings).

Если в качестве параметра передано имя группы, то возвращает признак, определяющий, сработал ли хоть один [`<Checking>`](./#checkings) в группе.

```xml
<Form>
  <Property Name="CheckingFired" />
</Form>
```

```xml
<Form>
  <Property Name="CheckingFired">Group</Property>
</Form>
```

### Icon <a href="#get_icon" id="get_icon"></a>

Возвращает путь до файла иконки.

```xml
<Form>
  <Property Name="Icon" />
</Form>
```

### IsActive <a href="#get_is_active" id="get_is_active"></a>

Возвращает признак, определяющий, что форма активна.

```xml
<Form>
  <Property Name="IsActive" />
</Form>
```

### LoadMode <a href="#get_load_mode" id="get_load_mode"></a>

Возвращает идентификатор выбранного режима загрузки данных.

```xml
<Form>
  <Property Name="LoadMode" />
</Form>
```

Возвращает одно из значений:

<table data-header-hidden><thead><tr><th width="106" align="center"></th><th></th></tr></thead><tbody><tr><td align="center">0</td><td><p>Последовательный режим - загрузка соединений с данными будет происходить по очереди.</p><p>Обеспечивает минимальную скорость загрузки форм, при этом требует минимальное количество ресурсов со стороны сервера.</p></td></tr><tr><td align="center">1</td><td><p>Пакетный режим.</p><p>Обеспечивает стандартную скорость загрузки форм, при этом не требует значительного количества ресурсов со стороны сервера.</p></td></tr><tr><td align="center">2</td><td><p>Параллельный режим. Режим по умолчанию.</p><p>Обеспечивает увеличенную скорость загрузки форм, однако при этом требует максимальное количество ресурсов со стороны сервера. </p></td></tr></tbody></table>

## Set-проперти для динамического задания свойств <a href="#set_properties" id="set_properties"></a>

### Title <a href="#set_title" id="set_title"></a>

Задает заголовок формы.

Любое значение будет переведено в текстовое.

```xml
<Form>
  <Property Name="Title">Заголовок</Property>
</Form>
```

### Top <a href="#set_top" id="set_top"></a>

Задает координату расположения формы по высоте (сверху вниз).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="Top">10</Property>
</Form>
```

### Left <a href="#set_left" id="set_left"></a>

Задает координату расположения формы по ширине (слева направо).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="Left">20</Property>
</Form>
```

### Height <a href="#set_height" id="set_height"></a>

Задает высоту рабочей области формы (то есть кайма формы сюда не входит).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="Height">100</Property>
</Form>
```

### Width <a href="#set_width" id="set_width"></a>

Задает ширину рабочей области формы (то есть кайма формы сюда не входит).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="Width">200</Property>
</Form>
```

### TotalHeight <a href="#set_total_height" id="set_total_height"></a>

Задает полную высоту формы (с учетом каймы).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="TotalHeight">100</Property>
</Form>
```

### TotalWidth <a href="#set_total_width" id="set_total_width"></a>

Задает полную ширину формы (с учетом каймы).

Ожидается целочисленное значение.

```xml
<Form>
  <Property Name="TotalWidth">200</Property>
</Form>
```

### HorizontalAlign <a href="#set_horizontal_align" id="set_horizontal_align"></a>

Задает тип положения формы по горизонтали.

Ожидается название одного из типов положения формы по горизонтали.

```xml
<Form>
  <Property Name="HorizontalAlign">Right</Property>
</Form>
```

### VerticalAlign <a href="#set_vertical_align" id="set_vertical_align"></a>

Задает тип положения формы по вертикали.

Ожидается название одного из типов положения формы по вертикали.

```xml
<Form>
  <Property Name="VerticalAlign">Bottom</Property>
</Form>
```

### StartPosition <a href="#set_start_position" id="set_start_position"></a>

Задает тип положения формы на экране.

Ожидается название одного из типов положения формы на экране.

```xml
<Form>
  <Property Name="StartPosition">CenterScreen</Property>
</Form>
```

### CenterToScreen

Выравнивает форму по центру текущего экрана.

Значение не ожидается.

```xml
<Form>
  <Property Name="CenterToScreen" />
</Form>
```

### FormState <a href="#set_form_state" id="set_form_state"></a>

Задает тип состояния формы.

Ожидается название одного из типов состояния формы.

```xml
<Form>
  <Property Name="FormState">Normal</Property>
</Form>
```

### AutoScroll <a href="#set_auto_scroll" id="set_auto_scroll"></a>

Задает признак, определяющий, показывать ли полосы прокрутки на форме, если объекты не входят в ее рабочую область.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="AutoScroll">True</Property>
</Form>
```

### FontStyle <a href="#set_font_style" id="set_font_style"></a>

Задает имя стиля шрифта формы по умолчанию.

Ожидается имя одного из стилей шрифтов, описанных в форме.

```xml
<Form>
  <Property Name="FontStyle">FontStyle</Property>
</Form>
```

### ForeColor <a href="#set_fore_color" id="set_fore_color"></a>

Задает имя цвета текста формы по умолчанию.

Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Form>
  <Property Name="ForeColor">ForeColor</Property>
</Form>
```

### BackColor <a href="#set_back_color" id="set_back_color"></a>

Задает имя цвета фона формы.

Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Form>
  <Property Name="BackColor">BackColor</Property>
</Form>
```

### TransparencyColor <a href="#set_transparency_color" id="set_transparency_color"></a>

Задает имя цвета, который форма будет определять как прозрачный.

Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Form>
  <Property Name="TransparencyColor">TransparencyColor</Property>
</Form>
```

### BackgroundImage <a href="#set_background_image" id="set_background_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на форме.

Любое значение будет переведено в текстовое.

```xml
<Form>
  <Property Name="BackgroundImage">BackgroundImage</Property>
</Form>
```

### StatusBar <a href="#set_status_bar" id="set_status_bar"></a>

Задает признак отображения бара событий формы.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="StatusBar">True</Property>
</Form>
```

### FormBorderStyle <a href="#set_form_border_style" id="set_form_border_style"></a>

Задает тип границы формы.

Ожидается название одного из типов границы формы.

```xml
<Form>
  <Property Name="FormBorderStyle">FixedSingle</Property>
</Form>
```

### ControlBox <a href="#set_control_box" id="set_control_box"></a>

Задает признак, определяющий, отображаются или нет кнопки оконного меню в строке заголовка формы.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="ControlBox">False</Property>
</Form>
```

### MinimizeBox <a href="#set_minimize_box" id="set_minimize_box"></a>

Задает признак, определяющий, отображается ли кнопка свертывания в строке заголовка формы.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="MinimizeBox">False</Property>
</Form>
```

### MaximizeBox <a href="#set_maximize_box" id="set_maximize_box"></a>

Задает признак, определяющий, отображается ли кнопка развертывания в строке заголовка формы.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="MaximizeBox">False</Property>
</Form>
```

### ShowInTaskbar <a href="#set_show_in_taskbar" id="set_show_in_taskbar"></a>

Задает признак, определяющий, отображается ли форма в панели задач.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="ShowInTaskbar">False</Property>
</Form>
```

### TopMost <a href="#set_top_most" id="set_top_most"></a>

Задает признак, определяющий, необходимо ли отображать форму как форму переднего плана.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="TopMost">True</Property>
</Form>
```

### Opacity <a href="#set_opacity" id="set_opacity"></a>

Задает уровень непрозрачности формы.

Ожидается числовое значение (от 0 до 1).

```xml
<Form>
  <Property Name="Opacity">0</Property>
</Form>
```

### KeyPreview <a href="#set_key_preview" id="set_key_preview"></a>

Задает признак, определяющий, будет ли форма получать события нажатия клавиш с объектов, на ней расположенных.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="KeyPreview">True</Property>
</Form>
```

### AsteriskForeColor <a href="#set_asterisk_fore_color" id="set_asterisk_fore_color"></a>

Задает имя цвета "звездочки" формы.

Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Form>
  <Property Name="AsteriskForeColor">AsteriskForeColor</Property>
</Form>
```

### AsteriskFontStyle <a href="#set_asterisk_font_style" id="set_asterisk_font_style"></a>

Задает имя стиля шрифта "звездочки" формы.

Ожидается имя одного из стилей шрифтов, описанных в форме.

```xml
<Form>
  <Property Name="AsteriskFontStyle">AsteriskFontStyle</Property>
</Form>
```

### DateTimeNow <a href="#set_date_time_now" id="set_date_time_now"></a>

Задает рабочую дату и время формы, определенную первый раз в момент открытия формы.

Ожидается значение типа дата/время.

```xml
<Form>
  <Property Name="DateTimeNow">2015-11-04 23:42:50</Property>
</Form>
```

### RefreshDateTimeNow <a href="#set_refresh_date_time_now" id="set_refresh_date_time_now"></a>

Задает рабочую дату и время формы, равную текущей дате и времени.

Значение тэга `<Property>`: не ожидается.

```xml
<Form>
  <Property Name="RefreshDateTimeNow" />
</Form>
```

### FormChanged <a href="#set_form_changed" id="set_form_changed"></a>

Задает признак изменения формы (определяется как совокупность get-проперти `ValueChanged` объектов на форме).

Если `FormChanged` присваивается значение False, то проперти `ValueChanged` всех объектов формы тоже приобретут значение False.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="FormChanged">False</Property>
</Form>
```

### EnableWaitingAnimation <a href="#set_enable_waiting_animation" id="set_enable_waiting_animation"></a>

Задает признак, определяющий, будет ли отображаться форма с анимацией.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="EnableWaitingAnimation">False</Property>
</Form>
```

### EnableWaitingAnimationWhileActive <a href="#set_enable_waiting_animation_while_active" id="set_enable_waiting_animation_while_active"></a>

Задает признак, определяющий, что форма с анимацией будет отображаться только тогда, когда окно активно.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="EnableWaitingAnimationWhileActive">True</Property>
</Form>
```

### RestoreLastFormState <a href="#set_restore_last_form_state" id="set_restore_last_form_state"></a>

Задает признак, определяющий, будет ли восстановлено предыдущее состояние формы.

Ожидается логическое значение.

```xml
<Form>
  <Property Name="RestoreLastFormState">True</Property>
</Form>
```

### Icon <a href="#set_icon" id="set_icon"></a>

Задает иконку формы.

Любое значение будет переведено в текстовое.

```xml
<Form>
  <Property Name="Icon">Icon.ico</Property>
</Form>
```
