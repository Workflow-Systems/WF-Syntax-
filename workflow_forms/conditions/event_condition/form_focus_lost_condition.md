---
description: Событийное условие; срабатывает при потере фокуса формы.
---

# FormFocusLostCondition

## Шаблон FormFocusLostCondition <a href="#template_form_focus_lost_condition" id="template_form_focus_lost_condition"></a>

```xml
<Condition Name="" Type="FormFocusLostCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
</Condition>
```

## Описание FormFocusLostCondition <a href="#description_form_focus_lost_condition" id="description_form_focus_lost_condition"></a>

```xml
<Condition Name="FormFocusLostConditionName" Type="FormFocusLostCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
</Condition>
```

{% hint style="info" %}
Работает только если форма открыта командой [`FormShowCommand`](../../commands/form_show_command.md), где в способе открытия дочерней формы (тэг `<Show>`) тип открытия (атрибут`Type`) задан как None.
{% endhint %}
