---
description: Команда; открывает диалоговое окно выбора цвета.
---

# ColorDialogShowCommand

## Шаблон ColorDialogShowCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="ColorDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
</Command>
```

## Описание ColorDialogShowCommand <a href="#description" id="description"></a>

```xml
<Command Name="ColorDialogShowCommandName" Type="ColorDialogShowCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
</Command>
```

### Результат выполнения ColorDialogShowCommand <a href="#result" id="result"></a>

#### OK <a href="#result_ok" id="result_ok"></a>

Признак того, что в диалоговом окне пользователем был выбран цвет.

#### Red <a href="#result_red" id="result_red"></a>

Красная составляющая выбранного цвета.

#### Green <a href="#result_green" id="result_green"></a>

Зелёная составляющая выбранного цвета.

#### Blue <a href="#result_blue" id="result_blue"></a>

Синяя составляющая выбранного цвета.

#### Value <a href="#result_value" id="result_value"></a>

Выбранный цвет в HTML формате (#rrggbb).
