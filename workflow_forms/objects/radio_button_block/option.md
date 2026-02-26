---
description: Задает настройки переключателя
---

# Option

## Шаблон Option <a href="#template" id="template"></a>

```xml
<Option Name="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Left></Left>
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
  <!--Тэги, специфичные для радиокнопки-->
  <Text></Text>
  <Checked></Checked>
  <Value></Value>
</Option>
```

## Атрибуты Option <a href="#attributes" id="attributes"></a>

### Name

Название радиокнопки.

Обязательный атрибут.

## Тэги, специфичные для Option <a href="#specific-tags" id="specific-tags"></a>

### Text <a href="#options_option_text" id="options_option_text"></a>

Текст переключателя. Отображается на кнопке или рядом с круглым флажком.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Текст</Text>
```

### Checked <a href="#options_option_checked" id="options_option_checked"></a>

Признак выбора переключателя.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Checked>False</Checked>
```

### Value <a href="#options_option_value" id="options_option_value"></a>

Значение переключателя.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Value>Value</Value>
```
