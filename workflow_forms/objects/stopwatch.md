---
description: Секундомер. Не имеет графического отображения.
---

# Stopwatch

## Шаблон Stopwatch <a href="#template" id="template"></a>

Не имеет вложенных тэгов.

```xml
<MyObject Name="Stopwatch" Type="Stopwatch" Assembly="SimpleControls" />
```

## Описание Stopwatch <a href="#description" id="description"></a>

```xml
<MyObject Name="Stopwatch" Type="Stopwatch" Assembly="SimpleControls" />
```

Значением Stopwatch считается интервал работы секундомера с момента старта (set-проперти [Start](stopwatch.md#set_start)) до остановки (set-проперти [Stop](stopwatch.md#set_stop)).

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения интервала работы секундомера используется get-проперти [Value](stopwatch.md#get_value):

```xml
<Object Name="Stopwatch">
  <Property Name="Value" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="Stopwatch" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Не имеет set-проперти для задания значения.

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### Value <a href="#get_value" id="get_value"></a>

Возвращает интервал (в миллисекундах) работы секундомера.

```xml
<Object Name="Stopwatch">
  <Property Name="Value" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### Start <a href="#set_start" id="set_start"></a>

Запускает секундомер.

Значение тэга `<Property>` не ожидается.

```xml
<Object Name="Stopwatch">
  <Property Name="Start" />
</Object>
```

### Stop <a href="#set_stop" id="set_stop"></a>

Останавливает секундомер.

Значение тэга `<Property>` не ожидается.

```xml
<Object Name="Stopwatch">
  <Property Name="Stop" />
</Object>
```
