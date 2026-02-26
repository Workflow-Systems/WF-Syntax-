---
description: Главное меню.
---

# MainMenu

## Шаблон MainMenu <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MainMenu>
  <!--Тэги, общие для всех меню-->
  <!--Тэги, специфичные для MainMenu-->
  <ForeColor></ForeColor>
  <FontStyle></FontStyle>
  <DisabledTextColor></DisabledTextColor>
  <MenuItemSelectedColor></MenuItemSelectedColor>
  <Gradient>
    <StartColor></StartColor>
    <FinishColor></FinishColor>
  </Gradient>
  <Height></Height>
  <MenuItem Name="" Type="MenuItem">
    <Title></Title>
    <Image></Image>
    <Enabled></Enabled>
    <Visible></Visible>
    <Items>
    
    </Items>
    <Hint></Hint>
  </MenuItem>
</MainMenu>
```

## Описание MainMenu <a href="#description" id="description"></a>

```xml
<MainMenu>
  <!--Тэги, общие для всех контекстных меню-->
  <!--Тэги, специфичные для MainMenu-->
</MainMenu>
```

## Тэги, специфичные для MainMenu <a href="#specific-tags" id="specific-tags"></a>

### MenuItem <a href="#menu_item" id="menu_item"></a>

[Элементы меню](../menu_item/).

Необязательный список тэгов.

```xml
<MenuItem Name="" Type="MenuItem">
  <Title></Title>
  <Image></Image>
  <Enabled></Enabled>
  <Visible></Visible>
  <Items>
    <MenuItem Name="" Type="MenuItem">
      <Title></Title>
      <Command Name="" />
    </MenuItem>
    <MenuItem Name="" Type="Separator" />
    <MenuItem Name="" Type="MenuItem">
      <Title></Title>
      <Commands>
        <Command Name="" />
      </Commands>
    </MenuItem>
  </Items>
  <Hint></Hint>
</MenuItem>
```



### ForeColor <a href="#fore_color" id="fore_color"></a>

Цвет текста пунктов меню.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<ForeColor>ForeColorName</ForeColor> 
```

### FontStyle <a href="#font_style" id="font_style"></a>

Стиль шрифта пунктов меню.

Необязательный тэг. Ожидается имя одного из стилей шрифтов, описанных в форме.

По умолчанию используется стандартное значение .NET.

```xml
<FontStyle>FontStyleName</FontStyle> 
```

### DisabledTextColor <a href="#disabled_text_color" id="disabled_text_color"></a>

Цвет текста неактивных пунктов меню.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<DisabledTextColor>DisabledTextColorName</DisabledTextColor>
```

### MenuItemSelectedColor <a href="#menu_item_selected_color" id="menu_item_selected_color"></a>

Цвет фона активного пункта меню при наведении на него курсора мышки.

Необязательный тэг. Ожидается имя одного из цветов, описанных в форме или описание цвета в формате HTML (#rrggbb).

По умолчанию используется стандартное значение .NET.

```xml
<MenuItemSelectedColor>MenuItemSelectedColorName</MenuItemSelectedColor>
```

### Gradient <a href="#gradient" id="gradient"></a>

Задает настройки градиентной заливки панели главного меню.

Необязательный тэг. Описание вложенных тэгов по [ссылке](gradient.md).

```xml
<Gradient>
  <StartColor>StartColorName</StartColor>
  <FinishColor>FinishColorName</FinishColor>
</Gradient>
```

### Height <a href="#height" id="height"></a>

Высота главного меню.

Необязательный тэг. Ожидается целочисленное значение.

По умолчанию используется стандартное значение .NET.

```xml
<Height>40</Height
```









