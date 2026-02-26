---
description: Команда; открывает дочернюю форму.
---

# FormShowCommand

## Шаблон FormShowCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="FormShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для FormShowCommand-->
  <Xml Type="Path"></Xml>
  <Show Type="" WithoutFocus="" />
  <Multiple Allow="" Reload="" />
  <Parameters>
    <Parameter Name="" />
  </Parameters>
  <UpdateResult Type="" />
  <Owner Form="" />
</Command>
```

## Описание FormShowCommand <a href="#description" id="description"></a>

```xml
<Command Name="FormShowCommandName" Type="FormShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для FormShowCommand-->
</Command>
```

Результатом выполнения команды FormShowCommand будут:

* Список неявных параметров открывающейся формы.
* Список явных параметров открывающейся формы.
* FormClosed - событийный параметр, срабатывает сразу же после закрытия формы.

## Тэги, специфичные для FormShowCommand <a href="#specific-tags" id="specific-tags"></a>

### Xml <a href="#xml" id="xml"></a>

Xml-код дочерней формы.

Обязательный тэг. Значение тэга `<Xml>`: зависит от значений атрибутов.

```xml
<Xml Type="Path">Path</Xml>
```

#### Атрибуты тэга `<Xml>` <a href="#attributes_tag_xml" id="attributes_tag_xml"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Название типа загрузки xml-код.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="form_show_command.md#xml_code_loading_types">типов загрузки</a> xml-кода.</p></td></tr></tbody></table>

#### Типы загрузки xml-кода <a href="#xml_code_loading_types" id="xml_code_loading_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Path</td><td>Загрузка кода из файла, расположенного по определенному пути.</td></tr></tbody></table>

Значение тэга `<Xml>` при атрибуте `Type`, равным Path: любое значение будет переведено в текстовое.

### Show <a href="#show" id="show"></a>

Способ открытия дочерней формы.

Необязательный тэг. Значение тэга `<Show>`: не ожидается.

Если тэг `<Show>` отсутствует, то для атрибута `Type` используется значение None.

```xml
<Show Type="Modal" WithoutFocus="False" />
```

#### Атрибуты тэга `<Show>` <a href="#attributes_tag_show" id="attributes_tag_show"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Название <a href="form_show_command.md#child_form_opening_types">типа открытия дочерней формы</a>.</p><p></p><p>Обязательный атрибут. Ожидается название одного из типов открытия дочерней формы.</p></td></tr><tr><td align="center">WithoutFocus</td><td><p>Признак, определяющий, будет ли дочерняя форма открыта без фокуса.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение. </p><p></p><p>Если атрибут <code>WithoutFocus</code> отсутствует, то используется значение False.</p></td></tr></tbody></table>

#### Типы открытия дочерней формы <a href="#child_form_opening_types" id="child_form_opening_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Modal</td><td>Открыть форму модально</td></tr><tr><td align="center">None</td><td>Открыть форму параллельно</td></tr><tr><td align="center">Hide</td><td>Открыть форму параллельно, спрятав родительскую</td></tr><tr><td align="center">Close</td><td>Открыть форму параллельно, закрыв родительскую (только если родительская форма - не стартовая)</td></tr><tr><td align="center">Thread</td><td>Открыть форму в фоновом потоке</td></tr></tbody></table>

### Multiple <a href="#multiple" id="multiple"></a>

Способ открытия еще одного экземпляра дочерней формы.

Необязательный тэг. Значение тэга `<Multiple>`: не ожидается.

Если тэг `<Multiple>` отсутствует, то для атрибута `Allow` используется значение False, а для атрибута `Reload` - значение True.

```xml
<Multiple Allow="False" Reload="True" />
```

#### Атрибуты тэга `<Multiple>` <a href="#attributes_tag_multiple" id="attributes_tag_multiple"></a>

<table data-header-hidden><thead><tr><th width="213.01324183369536" align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Allow</td><td><p>Признак, определяющий, можно ли открыть еще один экземпляр дочерней формы.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение.</p><p></p><p>Если атрибут <code>Allow</code> отсутствует, то используется значение False.</p></td></tr><tr><td align="center">Reload</td><td><p>Признак, определяющий, будут ли повторно отправлены параметры в экземпляр открытой дочерней формы.</p><p></p><p>Необязательный атрибут. Ожидается логическое значение. </p><p></p><p>Если атрибут <code>Reload</code> отсутствует, то используется значение False.</p><p></p><p>Данный атрибут актуален только, если атрибут <code>Allow</code> имеет значение False.</p></td></tr></tbody></table>

### Parameters <a href="#parameters" id="parameters"></a>

Параметры, которые будут переданы на дочернюю форму.

Необязательный тэг. Значение тэга `<Parameters>`: список тэгов `<Parameter>`.

```xml
<Parameters>
  <Parameter Name="ParameterName1">ParameterValue1</Parameter>
  <Parameter Name="ParameterName2">ParameterValue2</Parameter>
</Parameters>
```

#### Тэг `<Parameter>` <a href="#parameters_parameter" id="parameters_parameter"></a>

Параметр, который будет передан на дочернюю форму.

Необязательный тэг. Значение тэга `<Parameter>`: любое значение.

#### Атрибуты тэга `<Parameter>` <a href="#attributes_tag_parameters_parameter" id="attributes_tag_parameters_parameter"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название параметра.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>Name</code>: название одного из явных или неявных параметров дочерней формы.</p></td></tr></tbody></table>

### UpdateResult <a href="#update_result" id="update_result"></a>

Способ изменения результата команды.

Необязательный тэг. Значение тэга `<UpdateResult>`: не ожидается.

Если тэг `<UpdateResult>` отсутствует, то для атрибута `Type` используется значение OnFormClose.

```xml
<UpdateResult Type="OnFormClose" />
```

#### Атрибуты тэга `<UpdateResult>` <a href="#attributes_tag_update_result" id="attributes_tag_update_result"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Type</td><td><p>Название типа изменения результата команды.</p><p></p><p>Обязательный атрибут. Значение атрибута <code>Type</code>: ожидается название одного из <a href="form_show_command.md#command_result_edit_types">типов изменения результата команды</a>.</p></td></tr></tbody></table>

#### Типы изменения результата команды <a href="#command_result_edit_types" id="command_result_edit_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">OnFormClose</td><td>Изменение результатов команды происходит только после закрытия дочерней формы</td></tr><tr><td align="center">Always</td><td>Изменение результатов команды происходит мгновенно при любом изменении хотя бы одного явного (только явного, не неявного) параметра дочерней формы, даже без ее закрытия</td></tr></tbody></table>

### Owner <a href="#owner" id="owner"></a>

Указание на родительскую форму для формы, открываемой в команде.

Необязательный тэг. Значение тэга `<Owner>`: не ожидается`.`

Если тэг `<Owner>` отсутствует, то для атрибута `Form` используется значение This.

{% hint style="warning" %}
Родительская форма определяет порядок каскадного закрытия форм, но не передачу параметров.
{% endhint %}

```xml
<Owner Form="This" />
```

#### Атрибуты тэга `<Owner>` <a href="#attributes_tag_owner" id="attributes_tag_owner"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">Form</td><td><p>Название типа указания на родительскую форму.</p><p></p><p>Обязательный атрибут. Ожидается название одного из <a href="form_show_command.md#owner_form_types">типов указания на родительскую форму</a>.</p></td></tr></tbody></table>

#### Типы указания на родительскую форму <a href="#owner_form_types" id="owner_form_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="449.3333333333333"></th></tr></thead><tbody><tr><td align="center">This</td><td>Родительской для формы, открываемой в команде, будет текущая форма</td></tr><tr><td align="center">Parent</td><td>Родительской для формы, открываемой в команде, будет родительская форма текущей (другими словами, у текущей и открываемой формы будет одна и та же родительская форма)</td></tr></tbody></table>
