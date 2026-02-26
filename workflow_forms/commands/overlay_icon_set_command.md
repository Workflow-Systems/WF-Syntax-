---
description: >-
  Команда отображения количества уведомлений на иконке приложения на панели
  задач
---

# OverlayIconSetCommand

## Шаблон OverlayIconSetCommand <a href="#template" id="template"></a>

```xml
<Command Name="" Type="OverlayIconSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для ClipboardSetCommand-->
  <NoticeCount></NoticeCount>
</Command>
```

## Описание OverlayIconSetCommand <a href="#description" id="description"></a>

```xml
<Command Name="OverlayIconSetCommandName" Type="OverlayIconSetCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для ClipboardSetCommand-->
</Command>
```

### Результат выполнения OverlayIconSetCommand <a href="#result" id="result"></a>

Команда не имеет результата.

## Тэги, специфичные для OverlayIconSetCommand <a href="#specific-tags" id="specific-tags"></a>

### NoticeCount <a href="#notice_count" id="notice_count"></a>

Число, которое будет отображаться на иконке приложения в панели задач.\
Если число больше 9, то будет отображаться значение "9+".

Обязательный тэг. Ожидается положительное целочисленное значение.

```xml
<NoticeCount>6</NoticeCount>
```
