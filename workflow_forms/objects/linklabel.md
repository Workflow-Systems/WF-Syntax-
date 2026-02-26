---
description: Графический объект; надпись-ссылка.
---

# LinkLabel

## Шаблон LinkLabel <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="LinkLabel" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для LinkLabel-->
  <ActiveLinkColor></ActiveLinkColor>
  <DisabledLinkColor></DisabledLinkColor>
  <LinkColor></LinkColor>
  <LinkVisited></LinkVisited>
  <AutoEllipsis></AutoEllipsis>
  <LinkBehavior></LinkBehavior>
  <WaitWhileOpen></WaitWhileOpen>
  <Link></Link>
  <Application></Application>
  <TextAlign></TextAlign>
  <Text></Text>
  <FileGuid></FileGuid>
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

## Описание LinkLabel <a href="#description" id="description"></a>

```xml
<MyObject Name="LinkLabelName" Type="LinkLabel" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для LinkLabel-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением LinkLabel считается текст ссылки.

```xml
<Object Name="LinkLabelName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Любое значение будет переведено в текстовое.

```xml
<Object Name="LinkLabelName"></Object>
```

## Тэги, специфичные для LinkLabel <a href="#specific-tags" id="specific-tags"></a>

### ActiveLinkColor <a href="#active_link_color" id="active_link_color"></a>

Название цвета нажатой в данный момент времени ссылки.

Необязательный тэг. Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<ActiveLinkColor>ActiveLinkColor</ActiveLinkColor>
```

### DisabledLinkColor <a href="#disabled_link_color" id="disabled_link_color"></a>

Название цвета неактивной ссылки.

Необязательный тэг. Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<DisabledLinkColor>DisabledLinkColor</DisabledLinkColor>
```

### LinkColor <a href="#link_color" id="link_color"></a>

Название цвета ссылки.

Необязательный тэг. Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<LinkColor>LinkColor</LinkColor>
```

### LinkVisited <a href="#link_visited" id="link_visited"></a>

Признак, определяющий, было ли нажатие на ссылку.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<LinkVisited>False</LinkVisited>
```

### AutoEllipsis <a href="#auto_ellipsis" id="auto_ellipsis"></a>

Признак, определяющий, показывать ссылку в сокращенном виде или нет, если ее текст не помещается в надписи.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<AutoEllipsis>False</AutoEllipsis>
```

### LinkBehavior <a href="#link_behavior" id="link_behavior"></a>

Название типа поведения ссылки.

Необязательный тэг. Ожидается название одного из типов поведения ссылки:

<table data-header-hidden><thead><tr><th align="center"></th><th width="465.3333333333333"></th></tr></thead><tbody><tr><td align="center">SystemDefault</td><td>Поведение данной настройки зависит от параметров, заданных с помощью диалогового окна "Свойства обозревателя" панели управления или Internet Explorer.</td></tr><tr><td align="center">AlwaysUnderline</td><td>В ссылке всегда отображается подчеркнутый текст.</td></tr><tr><td align="center">HoverUnderline</td><td>В ссылке отображается подчеркнутый текст, только когда мышь находится на тексте ссылки.</td></tr><tr><td align="center">NeverUnderline</td><td>Текст ссылки никогда не отображается подчеркнутым.</td></tr></tbody></table>

По умолчанию используется значение SystemDefault.

```xml
<LinkBehavior>SystemDefault</LinkBehavior>
```

### WaitWhileOpen <a href="#wait_while_open" id="wait_while_open"></a>

Признак, определяющий, ожидать ли открытие ссылки в потоке текущей формы или открыть ее в другом потоке.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<WaitWhileOpen>False</WaitWhileOpen>
```

### Link <a href="#link" id="link"></a>

Текст ссылки (открывается, только если поле [`<FileGuid>`](linklabel.md#file_guid) не задано).

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Link>Ссылка</Link>
```

### Application <a href="#application" id="application"></a>

Путь до исполнительного файла приложения для открытия ссылки.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Application>Приложение</Application>
```

### TextAlign <a href="#text_align" id="text_align"></a>

Название типа положения текста надписи.

Необязательный тэг. Ожидается название одного из типов положения текста:

<table data-header-hidden><thead><tr><th width="214" align="center"></th><th width="437.3333333333333"></th></tr></thead><tbody><tr><td align="center">TopLeft</td><td>Слева сверху</td></tr><tr><td align="center">TopCenter</td><td>По центру сверху</td></tr><tr><td align="center">TopRight</td><td>Справа сверху</td></tr><tr><td align="center">MiddleLeft</td><td>Слева посередине</td></tr><tr><td align="center">MiddleCenter</td><td>По центру посередине</td></tr><tr><td align="center">MiddleRight</td><td>Справа посередине</td></tr><tr><td align="center">BottomLeft</td><td>Слева снизу</td></tr><tr><td align="center">BottomCenter</td><td>По центру снизу</td></tr><tr><td align="center">BottomRight</td><td>Справа снизу</td></tr></tbody></table>

По умолчанию используется значение MiddleLeft.

```xml
<TextAlign>MiddleLeft</TextAlign>
```

### Text <a href="#text" id="text"></a>

Текст надписи.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### FileGuid <a href="#file_guid" id="file_guid"></a>

Guid файла, который будет загружаться с сервера при открытии ссылки (открывается несмотря на наличие ссылки в поле [`<Link>`](linklabel.md#link)).

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<FileGuid>Guid</FileGuid>
```

### Commands <a href="#commands" id="commands"></a>

Список команд, которые будут выполнены при клике мышкой (команды выполняются только если поля [`<Link>`](linklabel.md#link) и [`<FileGuid>`](linklabel.md#file_guid) пустые).

Необязательный тэг. В качестве значения тэга ожидается список тэгов [`<Command>`](linklabel.md#commands_command) и/или конструкций [`<If>`](../values/if.md).

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

### ActiveLinkColor <a href="#get_active_link_color" id="get_active_link_color"></a>

Возвращает название цвета нажатой в данный момент времени ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="ActiveLinkColor" />
</Object>
```

### DisabledLinkColor <a href="#get_disabled_link_color" id="get_disabled_link_color"></a>

Возвращает название цвета неактивной ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="DisabledLinkColor" />
</Object>
```

### LinkColor <a href="#get_link_color" id="get_link_color"></a>

Возвращает название цвета ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkColor" />
</Object>
```

### LinkVisited <a href="#get_link_visited" id="get_link_visited"></a>

Возвращает признак, определяющий, было ли нажатие на ссылку.

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkVisited" />
</Object>
```

### AutoEllipsis <a href="#get_auto_ellipsis" id="get_auto_ellipsis"></a>

Возвращает признак, определяющий, показывать ссылку в сокращенном виде или нет, если ее текст не помещается в надписи.

```xml
<Object Name="LinkLabelName">
  <Property Name="AutoEllipsis" />
</Object>
```

### LinkBehavior <a href="#get_link_behavior" id="get_link_behavior"></a>

Возвращает название типа поведения ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkBehavior" />
</Object>
```

### WaitWhileOpen <a href="#get_wait_while_open" id="get_wait_while_open"></a>

Возвращает признак, определяющий, ожидать ли открытие ссылки в потоке текущей формы или открыть ее в другом потоке.

```xml
<Object Name="LinkLabelName">
  <Property Name="WaitWhileOpen" />
</Object>
```

### Link <a href="#get_link" id="get_link"></a>

Возвращает текст ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="Link" />
</Object>
```

### Application <a href="#get_application" id="get_application"></a>

Возвращает путь до исполнительного файла приложения для открытия ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="Application" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает текст надписи.

```xml
<Object Name="LinkLabelName">
  <Property Name="Text" />
</Object>
```

### TextAlign <a href="#get_text_align" id="get_text_align"></a>

Возвращает название типа положения текста.

```xml
<Object Name="LinkLabelName">
  <Property Name="TextAlign" />
</Object>
```

### FileGuid <a href="#get_file_guid" id="get_file_guid"></a>

Возвращает Guid файла, который будет загружаться с сервера при открытии ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="FileGuid" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### ActiveLinkColor <a href="#set_active_link_color" id="set_active_link_color"></a>

Задает название цвета нажатой в данный момент времени ссылки.

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="LinkLabelName">
  <Property Name="ActiveLinkColor">ActiveLinkColor</Property>
</Object>
```

### DisabledLinkColor <a href="#set_disabled_link_color" id="set_disabled_link_color"></a>

Задает название цвета неактивной ссылки.

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="LinkLabelName">
  <Property Name="DisabledLinkColor">DisabledLinkColor</Property>
</Object>
```

### LinkColor <a href="#set_link_color" id="set_link_color"></a>

Задает название цвета ссылки.

Ожидается название одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkColor">LinkColor</Property>
</Object>
```

### LinkVisited <a href="#set_link_visited" id="set_link_visited"></a>

Задает признак, определяющий, было ли нажатие на ссылку.

Ожидается логическое значение.

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkVisited">True</Property>
</Object>
```

### AutoEllipsis <a href="#set_auto_ellipsis" id="set_auto_ellipsis"></a>

Задает признак, определяющий, показывать ссылку в сокращенном виде или нет, если ее текст не помещается в надписи.

Ожидается логическое значение.

```xml
<Object Name="LinkLabelName">
  <Property Name="AutoEllipsis">True</Property>
</Object>
```

### LinkBehavior <a href="#set_link_behavior" id="set_link_behavior"></a>

Задает название типа поведения ссылки.

Ожидается одно из названий типов поведения ссылки.

```xml
<Object Name="LinkLabelName">
  <Property Name="LinkBehavior">AlwaysUnderline</Property>
</Object>
```

### WaitWhileOpen <a href="#set_wait_while_open" id="set_wait_while_open"></a>

Задает признак, определяющий, ожидать ли открытие ссылки в потоке текущей формы или открыть ее в другом потоке.

Ожидается логическое значение.

```xml
<Object Name="LinkLabelName">
  <Property Name="WaitWhileOpen">True</Property>
</Object>
```

### Link <a href="#set_link" id="set_link"></a>

Задает текст ссылки.

Любое значение будет переведено в текстовое.

```xml
<Object Name="LinkLabelName">
  <Property Name="Link">Ссылка</Property>
</Object>
```

### Application <a href="#set_application" id="set_application"></a>

Задает путь до исполнительного файла приложения для открытия ссылки.

Любое значение будет переведено в текстовое.

```xml
<Object Name="LinkLabelName">
  <Property Name="Application">Приложение</Property>
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает текст надписи.

Любое значение будет переведено в текстовое.

```xml
<Object Name="LinkLabelName">
  <Property Name="Text">Text</Property>
</Object>
```

### TextAlign <a href="#set_text_align" id="set_text_align"></a>

Задает название типа положения текста.

Ожидается одно из названий типов положения текста.

```xml
<Object Name="LinkLabelName">
  <Property Name="TextAlign">TopLeft</Property>
</Object>
```

### FileGuid <a href="#set_file_guid" id="set_file_guid"></a>

Задает Guid файла, который будет загружаться с сервера при открытии ссылки.

Любое значение будет переведено в текстовое.

```xml
<Object Name="LinkLabelName">
  <Property Name="FileGuid">Guid</Property>
</Object>
```
