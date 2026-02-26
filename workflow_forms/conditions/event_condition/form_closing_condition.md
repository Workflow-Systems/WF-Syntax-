---
description: Событийное условие; срабатывает при попытке закрытия формы.
---

# FormClosingCondition

## Шаблон FormClosingCondition <a href="#template_form_closing_condition" id="template_form_closing_condition"></a>

```xml
<Condition Name="" Type="FormClosingCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <AlwaysChange Value="" />
  <!--Тэги, специфичные для FormClosingCondition-->
  <CloseReason Value="" />
  <ExceptCloseReasons>
    <CloseReason Value="" />
  </ExceptCloseReasons>
</Condition>
```

## Описание FormClosingCondition <a href="#description_form_closing_condition" id="description_form_closing_condition"></a>

```xml
<Condition Name="FormClosingConditionName" Type="FormClosingCondition" Assembly="Conditions">
  <!--Тэги, общие для всех условий-->
  <!--Тэги, специфичные для FormClosingCondition-->
</Condition>
```

## Тэги, специфичные для FormClosingCondition <a href="#tags_form_closing_condition" id="tags_form_closing_condition"></a>

### CloseReason <a href="#close_reason" id="close_reason"></a>

Причина закрытия формы.

Необязательный тэг. Значение тэга `<CloseReason>`: не ожидается.

Если тэг `<CloseReason>` отсутствует, то для атрибута `Value` используется значение None.

При наличии тэга `<CloseReason>` тэг [`<ExceptCloseReasons>`](form_closing_condition.md#except_close_reasons) игнорируется.

```xml
<CloseReason Value="None" />
```

#### Атрибуты тэга `<CloseReason>` <a href="#attributes_tag_close_reason" id="attributes_tag_close_reason"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="463.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение причины закрытия формы.</p><p></p><p>Обязательный атрибут. Ожидается название одной из <a href="form_closing_condition.md#close_reason_types">причин закрытия формы</a>.</p></td></tr></tbody></table>

#### Причины закрытия формы <a href="#close_reason_types" id="close_reason_types"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="463.3333333333333"></th></tr></thead><tbody><tr><td align="center">ApplicationExitCall</td><td>Вызов метода Exit класса Application</td></tr><tr><td align="center">FormOwnerClosing</td><td>Закрытие родительской формы</td></tr><tr><td align="center">MdiFormClosing</td><td>Закрытие родительской MDI-формы</td></tr><tr><td align="center">TaskManagerClosing</td><td>Планировщик задач Windows закрывает приложение</td></tr><tr><td align="center">UserClosing</td><td>Пользователь закрывает форму посредством интерфейса</td></tr><tr><td align="center">WindowsShutDown</td><td>Операционная система Windows закрывает все приложения перед выключением (завершением сеанса пользователя)</td></tr><tr><td align="center">None</td><td>Причина не указана или не может быть определена</td></tr></tbody></table>

### ExceptCloseReasons <a href="#except_close_reasons" id="except_close_reasons"></a>

Список исключающих причин закрытия формы, то есть тех, не из-за которых форма закрывается.

Необязательный тэг. Значение тэга `<ExceptCloseReasons>`: список тэгов [`<CloseReason>`](form_closing_condition.md#close_reason).

При наличии тэга [`<CloseReason>`](form_closing_condition.md#close_reason) тэг `<ExceptCloseReasons>` игнорируется.

```xml
<ExceptCloseReasons>
  <CloseReason Value="UserClosing" />
  <CloseReason Value="WindowsShutDown" />
</ExceptCloseReasons>
```
