---
description: Иконка в трее.
---

# TrayIcon

## Шаблон TrayIcon <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="TrayIcon" Assembly="BaseControls" ChangeForm="">
  <Icon></Icon>
  <Text></Text>
  <HideFormOnMinimize></HideFormOnMinimize>
  <Blink></Blink>
  <BlinkInterval></BlinkInterval>
  <Visible></Visible>
  <ContextMenu Name="" />
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
          <Command Name="" />
        </Then>
      </ElseIf>
      <Else StopOnError="" Lock="">
        <Command Name="" />
      </Else>
    </If>
  </Commands>
</MyObject>
```

## Описание TrayIcon <a href="#description" id="description"></a>

```xml
<MyObject Name="" Type="TrayIcon" Assembly="BaseControls" ChangeForm="True">
  <!--Тэги, специфичные для TrayIcon-->
</MyObject>
```

#### Атрибуты TrayIcon <a href="#attributes_trayicon" id="attributes_trayicon"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="467.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название переменной.</p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Type</td><td><p>Название типа переменной в сборке.</p><p>Обязательный атрибут.</p></td></tr><tr><td align="center">Assembly</td><td><p>Название сборки (библиотека).</p><p>Обязательный атрибут.</p></td></tr></tbody></table>

### Получение значения <a href="#get-value" id="get-value"></a>

Значением TrayIcon считается текст иконки.

```xml
<Object Name="TrayIconName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: любое значение.

```xml
<Object Name="TrayIconName"></Object>
```

## Тэги, специфичные для TrayIcon <a href="#specific-tags" id="specific-tags"></a>

### Change <a href="#change" id="change"></a>

Настройки изменения проперти [`ValueChanged`](trayicon.md#get_value_changed) объекта.

Необязательный тэг.

Если тэг `<Change>` отсутствует, то для атрибутов `User`, `Source` и `ValueSet` используются значения True, True, и True соответственно.

```xml
<Change User="True" Source="False" ValueSet="True" />
```

#### Атрибуты тэга \<Change> <a href="#attributes_tag_change" id="attributes_tag_change"></a>

<table data-header-hidden><thead><tr><th width="166.33333333333331" align="center"></th><th width="506.8415398749965"></th></tr></thead><tbody><tr><td align="center">User</td><td><p>Признак, будет ли <a href="trayicon.md#get_value_changed"><code>ValueChanged</code></a> иметь значение True, если пользователь в графическом интерфейсе изменит значение объекта.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr><tr><td align="center">Source</td><td><p>Признак, будет ли <a href="trayicon.md#get_value_changed"><code>ValueChanged</code></a> иметь значение True, если значение объекта перезагрузится из источника.</p><p></p><p>Если атрибут <code>Source</code> имеет значение False, и при этом значение из источника перезагрузилось, то <a href="trayicon.md#get_value_changed"><code>ValueChanged</code></a> будет иметь значение False.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr><tr><td align="center">ValueSet</td><td><p>Признак, будет ли <a href="trayicon.md#get_value_changed"><code>ValueChanged</code></a> иметь значение True, если значение объекта будет присвоено из команды <a href="../commands/value_set_command.md"><code>ValueSetCommand</code></a>.</p><p></p><p>Если атрибут <code>ValueSet</code> имеет значение False, и при этом значение было присвоено из команды <a href="../commands/value_set_command.md"><code>ValueSetCommand</code></a>, то <a href="trayicon.md#get_value_changed"><code>ValueChanged</code></a> будет иметь значение False.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### Icon <a href="#icon" id="icon"></a>

Путь до файла типа ICO с графическим содержанием, которое будет расположено на иконке в трее.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<Icon>` отсутствует, то в качестве изображения будет использована иконка по умолчанию.

```xml
<Icon>Icon.ico</Icon>
```

### Text <a href="#text" id="text"></a>

Текст иконки (текст, всплывающий при наведении курсора мышки).

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### HideFormOnMinimize <a href="#hide_form_on_minimize" id="hide_form_on_minimize"></a>

Признак, определяющий, будет ли исчезать окно при сворачивании.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<HideFormOnMinimize>True</HideFormOnMinimize>
```

### Blink <a href="#blink" id="blink"></a>

Признак моргания иконки в трее.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Blink>False</Blink>
```

### BlinkInterval <a href="#blink_interval" id="blink_interval"></a>

Интервал моргания иконки в трее (в миллисекундах).

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется значение 500.

```xml
<BlinkInterval>500</BlinkInterval>
```

### Visible <a href="#visible" id="visible"></a>

Признак видимости иконки в трее.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<Visible>False</Visible>
```

### ContextMenu <a href="#context_menu" id="context_menu"></a>

Контекстное меню иконки в трее.

Необязательный тэг. Значение тэга `<ContextMenu>`: не ожидается.

```xml
<ContextMenu Name="ContextMenuName" />
```

#### Атрибуты тэга `<ContextMenu>` <a href="#attributes_tag_context_menu" id="attributes_tag_context_menu"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="448.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название контекстного меню.</p><p></p><p>Обязательный атрибут. Ожидается название одного из контекстных меню, описанных в форме.</p></td></tr></tbody></table>

### Commands <a href="#commands" id="commands"></a>

Список команд, которые будут выполнены при нажатии на иконку в трее.

Необязательный тэг. В качестве значения тэга ожидается список тэгов [`<Command>`](trayicon.md#commands_command) и/или конструкций [`<If>`](../values/if.md).

```xml
<Commands StopOnError="True"  Lock="">
  <Command Name="CommandName1" />
  <If>
    <When></When>
    <Then StopOnError="True" Lock="">
      <Command Name="CommandName2">
        <Input Name="InputName1">input 1</Input>
        <Input Name="InputName2">input 2</Input>
      </Command>
    </Then>
    <ElseIf>
      <When></When>
      <Then StopOnError="True" Lock="">
        <Command Name="CommandName3" />
      </Then>
    </ElseIf>
    <Else StopOnError="True" Lock="">
      <Command Name="CommandName4" />
    </Else>
  </If>
</Commands>
```

#### Атрибуты тэга `<Commands>` <a href="#attributes_tag_commands" id="attributes_tag_commands"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="532.4285714285713"></th></tr></thead><tbody><tr><td align="center">StopOnError</td><td><p>Признак, определяющий, будет ли остановлено выполнение команд, если при выполнении очередной произойдет ошибка.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение True.</p></td></tr><tr><td align="center">Lock</td><td><p>Признак, определяющий, будет ли блокироваться форма при выполнении команд.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>По умолчанию используется значение False.</p></td></tr></tbody></table>

#### Тэг `<Command>` <a href="#commands_command" id="commands_command"></a>

Обращение к команде по имени для ее выполнения.

Необязательный тэг. В качестве значения тэга ожидается список тэгов [`<Input>`](../values/input.md).

```xml
<!--Вариант 1-->
<Command Name="CommandName1" />

<!--Вариант 2-->
<Command Name="CommandName2">
  <Input Name="InputName1">input 1</Input>
  <Input Name="InputName2">input 2</Input>
</Command>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает текст иконки (текст, всплывающий при наведении курсора мышки).

```xml
<Object Name="TrayIconName">
  <Property Name="Value" />
</Object>
```

### ValueChanged <a href="#get_value_changed" id="get_value_changed"></a>

Возвращает признак того, было ли изменено значение объекта TrayIcon в процессе работы.

Есть 3 способа изменить значение объекта:

1. Изменить значение прямым образом в графическом интерфейсе формы.
2. Указать источник значения (ссылка на любые данные на форме). В случае изменения значения в источнике, автоматически изменится значение и самого объекта.
3. Присвоить значение объекту посредством команды [ValueSetCommand](../commands/value_set_command.md).

```xml
<Object Name="TrayIconName">
  <Property Name="ValueChanged" />
</Object>
```

### Icon <a href="#get_icon" id="get_icon"></a>

Возвращает путь до файла типа ICO с графическим содержанием, которое расположено на иконке в трее.

```xml
<Object Name="TrayIconName">
  <Property Name="Icon" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает текст иконки (текст, всплывающий при наведении курсора мышки).

```xml
<Object Name="TrayIconName">
  <Property Name="Text" />
</Object>
```

### HideFormOnMinimize <a href="#get_hide_form_on_minimize" id="get_hide_form_on_minimize"></a>

Возвращает признак, определяющий, будет ли исчезать окно при сворачивании.

```xml
<Object Name="TrayIconName">
  <Property Name="HideFormOnMinimize" />
</Object>
```

### Blink <a href="#get_blink" id="get_blink"></a>

Возвращает признак моргания иконки в трее.

```xml
<Object Name="TrayIconName">
  <Property Name="Blink" />
</Object>
```

### BlinkInterval <a href="#get_blink_interval" id="get_blink_interval"></a>

Возвращает интервал моргания иконки в трее (в миллисекундах).

```xml
<Object Name="TrayIconName">
  <Property Name="BlinkInterval" />
</Object>
```

### Visible <a href="#get_visible" id="get_visible"></a>

Возвращает признак видимости объекта.

```xml
<Object Name="ObjectName">
  <Property Name="Visible" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Value <a href="#set_value" id="set_value"></a>

Задает текст иконки (текст, всплывающий при наведении курсора мышки).

Любое значение будет переведено в текстовое.

```xml
<Object Name="TrayIconName">
  <Property Name="Value">Text</Property>
</Object>
```

### ValueChanged <a href="#set_value_changed" id="set_value_changed"></a>

Задает признак изменения значения текста иконки.

Ожидается логическое значение.

```xml
<Object Name="TrayIconName">
  <Property Name="ValueChanged">False</Property>
</Object>
```

### Icon <a href="#set_icon" id="set_icon"></a>

Задает путь до файла типа ICO с графическим содержанием, которое будет расположено на иконке в трее.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TrayIconName">
  <Property Name="Icon" />
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает текст иконки (текст, всплывающий при наведении курсора мышки).

Любое значение будет переведено в текстовое.

```xml
<Object Name="TrayIconName">
  <Property Name="Text">Text</Property>
</Object>
```

### HideFormOnMinimize <a href="#set_hide_form_on_minimize" id="set_hide_form_on_minimize"></a>

Задает признак, определяющий, будет ли исчезать окно при сворачивании.

Ожидается логическое значение.

```xml
<Object Name="TrayIconName">
  <Property Name="HideFormOnMinimize">True</Property>
</Object>
```

### Blink <a href="#set_blink" id="set_blink"></a>

Задает признак моргания иконки в трее.

Ожидается логическое значение.

```xml
<Object Name="TrayIconName">
  <Property Name="Blink">True</Property>
</Object>
```

### BlinkInterval <a href="#set_blink_interval" id="set_blink_interval"></a>

Задает интервал моргания иконки в трее (в миллисекундах).

Ожидается целочисленное значение.

```xml
<Object Name="TrayIconName">
  <Property Name="BlinkInterval">1000</Property>
</Object>
```

### Visible <a href="#set_visible" id="set_visible"></a>

Задает признак видимости объекта.

Ожидается логическое значение.

```xml
<Object Name="ObjectName">
  <Property Name="Visible">True</Property>
</Object>
```

### Show <a href="#set_show" id="set_show"></a>

Делает иконку в трее видимой.

Значение тэга Property: не ожидается.

```xml
<Object Name="TrayIconName">
  <Property Name="Show" />
</Object>
```

### Hide <a href="#set_hide" id="set_hide"></a>

Делает иконку в трее невидимой.

Значение тэга Property: не ожидается.

```xml
<Object Name="TrayIconName">
  <Property Name="Hide" />
</Object>
```

### ShowTip <a href="#set_show_tip" id="set_show_tip"></a>

Показывает всплывающую подсказку с текстом Text заголовком Title и пиктограммой типа Type над иконкой в трее.

```xml
<Object Name="TrayIconName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ShowTip">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Text: любое значение будет переведено в текстовое-->
      <Parameter Name="Text">Text</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным Title: любое значение будет переведено в текстовое-->
      <Parameter Name="Title">Title</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение None-->
      <!--Значение тэга Parameter с атрибутом Name, равным Type: ожидается название одного из типов пиктограмм для всплывающей подсказки-->
      <Parameter Name="Type">Info</Parameter>
    </Parameters>
  </Property>
</Object>
```

#### Типы пиктограмм для всплывающей подсказки для иконки в трее: <a href="#pictogram_types" id="pictogram_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="468.3333333333333"></th></tr></thead><tbody><tr><td align="center">Information</td><td>Пиктограмма содержит символ, состоящий из буквы i в нижнем регистре, помещенной в синий кружок.</td></tr><tr><td align="center">Warning</td><td>Пиктограмма содержит символ, состоящий из восклицательного знака в желтом треугольнике.</td></tr><tr><td align="center">Error</td><td>Пиктограмма содержит символ, состоящий из белого значка Х, заключенного в красный кружок.</td></tr><tr><td align="center">None</td><td>Без пиктограммы.</td></tr></tbody></table>
