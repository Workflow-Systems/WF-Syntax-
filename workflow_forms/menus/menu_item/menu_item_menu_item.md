---
description: >-
  Элемент меню, по нажатию на который выполняется определенная команда и/или
  раскрывается еще одно подменю.
---

# MenuItem

## Шаблон MenuItem <a href="#template_menu_item" id="template_menu_item"></a>

```xml
<MenuItem Name="" Type="MenuItem">
  <!--Тэги, общие для всех элементов меню-->
  <Enabled></Enabled>
  <Visible></Visible>
  <!--Тэги, специфичные для типа MenuItem-->
  <Title></Title>
  <Image></Image>
  <Command Name="" />
  <Commands StopOnError="" Lock="">
    <Command Name="" />
    <If>
      <When></When>
      <Then StopOnError="" Lock="">
        <Command Name="" />
      </Then>
      <ElseIf>
        <When></When>
        <Then StopOnError="" Lock="">
          <Command Name="">
            <Input Name="" />
            <Input Name="" />
          </Command>
        </Then>
      </ElseIf>
      <Else StopOnError="" Lock="">
        <Command Name="" />
      </Else>
    </If>
  </Commands>
  <ForeColor></ForeColor>
  <Blink></Blink>
  <BlinkInterval></BlinkInterval>
  <BlinkPart></BlinkPart>
  <Items></Items>
  <Hint></Hint>
  <IsInstruction></IsInstruction>
</MenuItem>
```

## Описание MenuItem <a href="#description_menu_item" id="description_menu_item"></a>

```xml
<MenuItem Name="MenuItemName" Type="MenuItem">
  <!--Тэги, общие для всех элементов меню-->
  <!--Тэги, специфичные для MenuItem-->
</MenuItem>
```

## Тэги, специфичные для MenuItem <a href="#tags_menu_item" id="tags_menu_item"></a>

### Title <a href="#title" id="title"></a>

Текст элемента меню.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Title>Текст</Title>
```

### Image <a href="#image" id="image"></a>

Путь до файла с графическим содержанием, которое будет расположено на элементе меню.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Image>Image</Image>
```

### Command <a href="#command" id="command"></a>

Задает имя команды, которая будет выполнена при нажатии на элемент меню.\
Игнорируется, если указан тэг [`<Commands>`](menu_item_menu_item.md#commands).

Необязательный тэг. Значение тэга не ожидается.

Допускается передача в команду значения через тэг [`<Input>`](../../values/input.md).

```xml
<!--Вариант 1-->
<Command Name="CommandName1" />

<!--Вариант 2-->
<Command Name="CommandName2">
  <Input Name="InputName1">input 1</Input>
  <Input Name="InputName2">input 2</Input>
</Command>
```

### Commands <a href="#commands" id="commands"></a>

Последовательность команд, которые будут выполнены при нажатии на элемент меню.\
Имеет приоритет над тэгом [`<Command>`](menu_item_menu_item.md#command).

Необязательный тэг. В качестве значения тэга ожидается список тэгов `<Command>`, для вызова команды по имени, и/или конструкций `<If>`, задающих условия вызова команд.

```xml
<Commands StopOnError="" Lock="">
  <Command Name="" />
  <If>
    <When></When>
    <Then StopOnError="" Lock="">
      <Command Name="" />
    </Then>
    <ElseIf>
      <When></When>
      <Then StopOnError="" Lock="">
        <Command Name="">
          <Input Name="" />
          <Input Name="" />
        </Command>
      </Then>
    </ElseIf>
    <Else StopOnError="" Lock="">
      <Command Name="" />
    </Else>
  </If>
</Commands>
```

#### Атрибуты тэга `<Commands>` <a href="#attributes_tag_commands" id="attributes_tag_commands"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="475.3333333333333"></th></tr></thead><tbody><tr><td align="center">StopOnError</td><td><p>Признак, определяющий, будет ли остановлено выполнение команд, если при выполнении очередной произойдет ошибка.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>StopOnError</code> отсутствует, то используется значение False.</p></td></tr><tr><td align="center">Lock</td><td><p>Признак, определяющий, будет ли блокироваться форма при выполнении команд.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Lock</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

### ForeColor <a href="#fore_color" id="fore_color"></a>

Цвет текста пункта меню.&#x20;

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).&#x20;

По умолчанию используется цвет, указанный в теге [ForeColor](../main_menu/#fore_color) для MainMenu.

```xml
<ForeColor>ForeColor</ForeColor>
```

### Blink

Признак, включающий режим мигания.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Blink>True</Blink>
```

### BlinkInterval <a href="#blink_interval" id="blink_interval"></a>

Задает интервал мигания (в миллисекундах).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 500.

```xml
<BlinkInterval>500</BlinkInterval>
```

### BlinkPart <a href="#blink_part" id="blink_part"></a>

Признак, определяющий режим мигания: только текст, только изображение или текст и изображение одновременно.

Необязательный тэг. Ожидается название одного из режимов:

<table data-header-hidden><thead><tr><th width="202.08667435984262" align="center"></th><th width="521.8817842146913"></th></tr></thead><tbody><tr><td align="center">All</td><td>Мигают и текст и изображение</td></tr><tr><td align="center">Text</td><td>Мигает только текст</td></tr><tr><td align="center">Image</td><td>Мигает только изображение</td></tr></tbody></table>

По умолчанию используется значение All.

```xml
<BlinkPart>Image</BlinkPart>
```

### Items <a href="#items" id="items"></a>

Вложенные элементы меню: пункты MenuItem и/или разделители [Separator](menu_item_separator.md).

Необязательный тэг. Значение тэга список тэгов [`<MenuItem>`](./).

```xml
<Items>
  <MenuItem Name="" Type="MenuItem">
    <Title></Title>
    <Command Name="" />
  </MenuItem>
  <MenuItem Name="" Type="Separator" />
  <MenuItem Name="" Type="MenuItem">
    <Title></Title>
    <Commands>
      <Command Name="" />
    </Commands>
  </MenuItem>
</Items>
```

### Hint <a href="#hint" id="hint"></a>

Текст всплывающей подсказки элемента меню.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Hint>Подсказка</Hint>
```

### IsInstruction <a href="#is_instruction" id="is_instruction"></a>

Признак помечающий пункты меню, которые должны отображаться в крайнем правом положении в панели меню.\
Используется только для [MainMenu](../main_menu/) и пунктов меню верхнего уровня. Для вложенных пунктов меню игнорируется.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<IsInstruction>True</IsInstruction>
```

## Get-проперти для получения свойств <a href="#get_property_menu_item" id="get_property_menu_item"></a>

### Title <a href="#get_title" id="get_title"></a>

Возвращает текст элемента меню.

```xml
<Object Name="MenuItemName">
  <Property Name="Title" />
</Object>
```

### Image <a href="#get_image" id="get_image"></a>

Возвращает путь до файла с графическим содержанием, которое расположено на элементе меню.

```xml
<Object Name="MenuItemName">
  <Property Name="Image" />
</Object>
```

### Hint <a href="#get_hint" id="get_hint"></a>

Возвращает текст всплывающей подсказки элемента меню.

```xml
<Object Name="MenuItemName">
  <Property Name="Hint" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set_property_menu_item" id="set_property_menu_item"></a>

### Title <a href="#set_title" id="set_title"></a>

Задает текст элемента меню.

Любое значение будет переведено в текстовое.

```xml
<Object Name="MenuItemName">
  <Property Name="Title">Текст</Property>
</Object>
```

### Image <a href="#set_image" id="set_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на элементе меню.

Любое значение будет переведено в текстовое.

```xml
<Object Name="MenuItemName">
  <Property Name="Image" />
</Object>
```

### Hint <a href="#set_hint" id="set_hint"></a>

Задает текст всплывающей подсказки элемента меню.

Любое значение будет переведено в текстовое.

```xml
<Object Name="MenuItemName">
  <Property Name="Hint">Подсказка</Property>
</Object>
```
