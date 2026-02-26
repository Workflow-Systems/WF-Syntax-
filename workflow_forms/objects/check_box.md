---
description: Графический объект; галочка.
---

# CheckBox

## Шаблон CheckBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="CheckBox" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
  <Height></Height>
  <Width></Width>
  <FontStyle></FontStyle>
  <ForeColor></ForeColor>
  <BackColor></BackColor>
  <Enabled></Enabled>
  <Visible></Visible>
  <Hint></Hint>
  <ContextMenu Name="" />
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для CheckBox-->
  <Text></Text>
  <Value></Value>
  <Appearance></Appearance>
  <Image></Image>
  <ImageAlign></ImageAlign>
  <Custom Value="" />
  <Solid Value="" />
  <OnBackgroundColor></OnBackgroundColor>
  <OnForegroundColor></OnForegroundColor>
  <OffBackgroundColor></OffBackgroundColor>
  <OffForegroundColor></OffForegroundColor>
</MyObject>
```

## Описание CheckBox <a href="#description" id="description"></a>

```xml
<MyObject Name="ButtonName" Type="CheckBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для CheckBox-->
</MyObject>
```

Значением CheckBox считается признак установки галочки.

### Получение значения <a href="#get-value" id="get-value"></a>

```xml
<Object Name="CheckBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: ожидается логическое значение.

```xml
<Object Name="CheckBoxName">False</Object>
```

## Тэги, специфичные для CheckBox <a href="#specific-tags" id="specific-tags"></a>

### Text

Текст подписи для галочки.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### Value

Признак установки галочки.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Value>False</Value>
```

### Appearance

Признак определяющей внешний вид CheckBox.

Необязательный тэг. Ожидается название одного из типов внешнего вида:

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="382.9046282007178"></th><th data-hidden></th></tr></thead><tbody><tr><td align="center">Normal</td><td>В виде квадратного флажка</td><td></td></tr><tr><td align="center">Button</td><td>В виде кнопки</td><td></td></tr></tbody></table>

Если тэг `<Appearance>` отсутствует, то используется значение Normal.

```xml
<Appearance>Button</Appearance>
```

### Image

Признак будет ли на текст CheckBox спроецировано изображение.\
Игнорируется, если тэг [`<Custom>`](check_box.md#custom) имеет значение True.

Необязательный тэг. Путь к файлу изображения.

Если тэг `<Image>` отсутствует, то изображение будет отсутствовать.

```xml
<Image>Icons\plus.png</Image>
```

### ImageAlign <a href="#image_align" id="image_align"></a>

Признак определяющей выравнивание изображения.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th width="167.8403990024938" align="center"></th><th width="496.3333333333333"></th></tr></thead><tbody><tr><td align="center">BottomCenter</td><td>Содержимое выравнивается по вертикали в нижней части и по горизонтали в центре</td></tr><tr><td align="center">BottomLeft</td><td>Содержимое выравнивается по вертикали внизу и по горизонтали слева</td></tr><tr><td align="center">BottomRight</td><td>Содержимое выравнивается по вертикали внизу и по горизонтали справа</td></tr><tr><td align="center">MiddleCenter</td><td>Содержимое выравнивается по вертикали посередине и по горизонтали в центре</td></tr><tr><td align="center">MiddleLeft</td><td>Содержимое выравнивается по вертикали посередине и по горизонтали слева</td></tr><tr><td align="center">MiddleRight</td><td>Содержимое выравнивается по вертикали посередине и по горизонтали справа</td></tr><tr><td align="center">TopCenter</td><td>Содержимое выравнивается по вертикали вверху и по горизонтали в центре</td></tr><tr><td align="center">TopLeft</td><td>Содержимое выравнивается по вертикали вверху и по горизонтали слева</td></tr><tr><td align="center">TopRight</td><td>Содержимое выравнивается по вертикали вверху и по горизонтали справа</td></tr></tbody></table>

Если тэг `<ImageAlign>` отсутствует, то используется значение MiddleCenter.

```xml
<ImageAlign>MiddleLeft</ImageAlign>
```

### Custom <a href="#custom" id="custom"></a>

Признак, отвечающий за внешний вид элемента.\
Если признак имеет значение False, то объект отображается в виде квадратной галочки. Если значение True, то в виде кнопки-переключателя ToggleButton.

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение False.

```xml
<Custom Value="True" />
```

### Solid

Признак, отключающий полную заливку фона переключателя.\
Если признак имеет значение False, то вокруг переключателя отображается рамка.

Необязательный тэг. Значение тэга не ожидается.

Необязательный атрибут `Value` ожидает логическое значение. По умолчанию используется значение True.

```xml
<Solid Value="False" />
```

### OnBackgroundColor <a href="#on_background_color" id="on_background_color"></a>

Цвет фона переключателя во включенном состоянии.\
Игнорируется, если тэг [`<Custom>`](check_box.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](https://wfsys.gitbook.io/workflow-forms-syntax/workflow_forms/appearance) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).

По умолчанию используется белый цвет.

```xml
<OnBackgroundColor>AnyColor</OnBackgroundColor>
```

### OffBackgroundColor <a href="#off_background_color" id="off_background_color"></a>

Цвет фона переключателя в выключенном состоянии.\
Игнорируется, если тэг [`<Custom>`](check_box.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](https://wfsys.gitbook.io/workflow-forms-syntax/workflow_forms/appearance) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).

По умолчанию используется белый цвет.

```xml
<OffBackgroundColor>AnyColor</OffBackgroundColor>
```

### OnForegroundColor <a href="#on_foreground_color" id="on_foreground_color"></a>

Цвет флажка переключателя во включенном состоянии.\
Игнорируется, если тэг [`<Custom>`](check_box.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](https://wfsys.gitbook.io/workflow-forms-syntax/workflow_forms/appearance) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).

По умолчанию используется белый цвет.

```xml
<OnForegroundColor>AnyColor</OnForegroundColor>
```

### OffForegroundColor <a href="#off_foreground_color" id="off_foreground_color"></a>

Цвет флажка переключателя в выключенном состоянии.\
Игнорируется, если тэг [`<Custom>`](check_box.md#custom) имеет значение False.

Необязательный тэг. Ожидается имя одного из цветов, описанных в тэге [`<Appearance>`](https://wfsys.gitbook.io/workflow-forms-syntax/workflow_forms/appearance) формы или в файле стилей. Так же принимается описание цвета в формате HTML (#rrggbb).

По умолчанию используется белый цвет.

```xml
<OffForegroundColor>AnyColor</OffForegroundColor>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Text <a href="#get_text" id="get_text"></a>

Возвращает текст подписи для галочки.

```xml
<Object Name="CheckBoxName">
  <Property Name="Text" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Text <a href="#set_text" id="set_text"></a>

Задает текст подписи для галочки.

Любое значение будет переведено в текстовое.

```xml
<Object Name="CheckBoxName">
  <Property Name="Text">Text</Property>
</Object>
```
