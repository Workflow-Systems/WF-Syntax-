---
description: Объект; не имеет графического отображения.
---

# Variable

## Шаблон Variable <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="Variable" Assembly="SimpleControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Change User="" Source="" ValueSet="" />
  <!--Тэги, специфичные для Variable-->
  <SaveOnFormClose Value=""/>
  <Value></Value>
</MyObject>
```

## Описание Variable <a href="#description" id="description"></a>

```xml
<MyObject Name="" Type="Variable" Assembly="SimpleControls" ChangeForm="True">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Variable-->
</MyObject>
```

Значением Variable считается значение, указанное в тэге [`<Value>`](variable.md#value).

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения значения объекта используется get-проперти [Value](variable.md#get_value):

```xml
<Object Name="VariableName">
  <Property Name="Value" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="VariableName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания значения объекту используется set-проперти [Value](variable.md#set_value):

```xml
<Object Name="VariableName">
  <Property Name="Value">Новое значение</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="VariableName">Новое значение</Object>
```

## Тэги, специфичные для Variable <a href="#specific-tags" id="specific-tags"></a>

### Value <a href="#value" id="value"></a>

Значение объекта Variable.

Необязательный тэг. Ожидается любое значение.

По умолчанию используется значение NULL.

```xml
<Value>Value</Value>
```

### SaveOnFormClose <a href="#save_on_form_close" id="save_on_form_close"></a>

Настройка сохранения значения переменной в базе данных в таблице public.user\_form\_info.

Необязательный тэг. В качестве значения атрибута `Value` ожидается логическое значение.

По умолчанию используется значение False.

```xml
<SaveOnFormClose Value="True"/>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает значение объекта Variable, если он его имеет.

```xml
<Object Name="VariableName">
  <Property Name="Value" />
</Object>
```

### ValueChanged <a href="#get_value_changed" id="get_value_changed"></a>

Возвращает признак того, было ли изменено значение объекта Variable в процессе работы.

```xml
<Object Name="VariableName">
  <Property Name="ValueChanged" />
</Object>
```

Есть 3 способа изменить значение объекта:

1. Изменить значение прямым образом в графическом интерфейсе формы, с помощью set-проперти [`ValueChanged`](variable.md#valuechanged-1).
2. Указать источник значения (ссылка на любые данные на форме). В случае изменения значения в источнике, автоматически изменится значение и самого объекта.
3. Присвоить значение объекту посредством команды [`ValueSetCommand`](../commands/value_set_command.md).

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Value <a href="#set_value" id="set_value"></a>

Задает значение объекта Variable.

Ожидается любое значение.

```xml
<Object Name="VariableName">
  <Property Name="Value">Value</Property>
</Object>
```

### ValueChanged <a href="#set_value_changed" id="set_value_changed"></a>

Задает признак изменения значения объекта Variable.

Ожидается логическое значение.

```xml
<Object Name="VariableName">
  <Property Name="ValueChanged">False</Property>
</Object>
```

### Refresh

Обновляет значение объекта Variable.

```xml
<Object Name="ConstVariable">
  <Property Name="Refresh" />
</Object>
```

## Примеры <a href="#examples_variable" id="examples_variable"></a>

Работают только со числами. Со строками не работают вообще.

### Пример 1. Работающий. <a href="#example_1" id="example_1"></a>

```xml
<MyObject Name="Variable" Type="Variable" Assembly="SimpleControls">
  <Value>
	<Calculate>
	  <Expression>if({0}={1}, 1, 2)</Expression>
	  <Items>
		<Item>1</Item>
		<Item>0</Item>
	  </Items>
	</Calculate>
  </Value>
</MyObject>
```

### Пример 2. Не работающий. <a href="#example_2" id="example_2"></a>

```xml
<MyObject Name="Variable" Type="Variable" Assembly="SimpleControls">
  <Value>
	<Calculate>
	  <Expression>if({0}='test', 1, 2)</Expression>
	  <Items>
		<Item>test</Item>
		<Item>0</Item>
	  </Items>
	</Calculate>
  </Value>
</MyObject>
```
