---
description: >-
  Проверка содержимого формы с подсветкой объектов в виде "звездочки" справа от
  объекта или в виде вертикальной полоски слева от объекта.
---

# Checkings

## Шаблон Checking <a href="#template" id="template"></a>

```xml
<Checking>
  <Object Name="" />
  <Group Name="" />
  <ConditionExpression>
    <Or>
      <Not>
        <And>
          <Condition Name="" />
          <Condition Name="" />
          <Condition Name="" />
        </And>
      </Not>
      <And>
        <Condition Name="" />
        <Condition Name="" />
      </And>
    </Or>
  </ConditionExpression>
  <AsteriskHint></AsteriskHint>
</Checking>
```

## Описание Checking <a href="#description" id="description"></a>

```xml
<Checking>
  <Object Name="" />
  <ConditionExpression></ConditionExpression>
  <AsteriskHint></AsteriskHint>
</Checking>
```

Когда значение тэга [`<ConditionExpression>`](checkings.md#condition_expression) будет True, рядом с объектом, указанным в тэге [`<Object>`](checkings.md#object), будет отображаться "звездочка" или вертикальная полоска, при наведении на которые будет отображаться текст подсказки, заданный в тэге [`<AsteriskHint>`](checkings.md#asterisk_hint).

{% hint style="info" %}
Через атрибут [`ValidationType`](https://wfsys.gitbook.io/workflow-forms-syntax#validation_type) тэга `<Form>` можно управлять видом `Checking` формы:  "звездочка" или вертикальная полоска.
{% endhint %}

## Тэги, специфичные для Checking <a href="#specific-tags" id="specific-tags"></a>

### Object <a href="#object" id="object"></a>

Объект, значение которого проверяется.

Обязательный тэг. Значение тэга `<Object>`: не ожидается.

### Group <a href="#group" id="group"></a>

Группа, к которой относится `Сhecking`.\
Используется при обращении к get-проперти [CheckingFired](https://wfsys.gitbook.io/workflow-forms-syntax/workflow_forms/form#get_checking_fired), чтобы проверить сработал ли хоть один `<Checking>` из группы.

Необязательный тэг. Значение тэга `<Group>`: не ожидается.

### ConditionExpression <a href="#condition_expression" id="condition_expression"></a>

Логическое выражение из значений условий.

Обязательный тэг. Ожидается логическое выражение с использованием тэгов `<And>`, `<Or>`, `<Not>` в качестве операций и тэгов `<Condition>` в качестве операндов.

### AsteriskHint <a href="#asterisk_hint" id="asterisk_hint"></a>

Текст подсказки, которая будет отображаться при наведении курсора мыши на "звездочку" или вертикальную полоску, отображаемые рядом с объектом.

Необязательный тэг. Любое значение будет переведено в текстовое.
