---
description: Событийное условие; срабатывает перед изменением значения.
---

# BeforeChangeCondition

## Шаблон BeforeChangeCondition <a href="#template_before_change_condition" id="template_before_change_condition"></a>

```xml
<Condition Name="" Type="BeforeChangeCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для BeforeChangeCondition-->
  <Items>
    <Item></Item>
  </Items>
</Condition>
```

## Описание BeforeChangeCondition <a href="#description_before_change_condition" id="description_before_change_condition"></a>

```xml
<Condition Name="BeforeChangeConditionName" Type="BeforeChangeCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для BeforeChangeCondition-->
</Condition>
```

## Тэги, специфичные для BeforeChangeCondition <a href="#tags_before_change_condition" id="tags_before_change_condition"></a>

### Items <a href="#items" id="items"></a>

Значения для определения момента перед изменением хотя бы одного из них.

Обязательный тэг. Значение тэга `<Items>`: список тэгов [`<Item>`](before_change_condition.md#items_item).

```xml
<Items>
  <Item>Value1</Item>
  <Item>Value2</Item>
</Items>
```

#### Тэг `<Item>` <a href="#items_item" id="items_item"></a>

Значение для определения момента перед его изменением.

Необязательный тэг. Значение тэг `<Item>`: любое значение.
