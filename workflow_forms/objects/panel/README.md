---
description: Графический объект; группирующая панель.
---

# Panel

## Шаблон Panel <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="Panel" Assembly="BaseControls" ChangeForm="">
  <!--Тэги, общие для всех графических объектов-->
  <Top></Top>
  <Bottom></Bottom>
  <Left></Left>
  <Right></Right>
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
  <!--Тэги, специфичные для Panel-->
  <HorizontalScroll></HorizontalScroll>
  <VerticalScroll></VerticalScroll>
  <AutoScroll></AutoScroll>
  <BorderStyle></BorderStyle>
  <BackgroundImage></BackgroundImage>
  <BackgroundImageLayout></BackgroundImageLayout>
  <Gradient>
    <StartColor></StartColor>
    <FinishColor></FinishColor>
    <Scale></Scale>
    <Mode></Mode>
  </Gradient>
  <MyObject Name="" Type="" Assembly="" />
  <MyObject Name="" Type="" Assembly="" />
</MyObject>
```

## Описание Panel <a href="#description" id="description"></a>

```xml
<MyObject Name="PanelName" Type="Panel" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для Panel-->
</MyObject>
```

Panel не имеет значения.

## Тэги, специфичные для Panel <a href="#specific-tags" id="specific-tags"></a>

### HorizontalScroll <a href="#horizontal_scroll" id="horizontal_scroll"></a>

Признак наличия горизонтальной полосы прокрутки на панели.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<HorizontalScroll>False</HorizontalScroll>
```

### VerticalScroll <a href="#vertical_scroll" id="vertical_scroll"></a>

Признак наличия вертикальной полосы прокрутки на панели.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<VerticalScroll>False</VerticalScroll>
```

### AutoScroll <a href="#auto_scroll" id="auto_scroll"></a>

Признак автоматической установки полос прокрутки на панели.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<AutoScroll>False</AutoScroll>
```

### BorderStyle <a href="#border_style" id="border_style"></a>

Название типа границ панели.

Необязательный тэг. Ожидается название одного из типов границ панели:

<table data-header-hidden><thead><tr><th align="center"></th><th width="405.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет границ</td></tr><tr><td align="center">FixedSingle</td><td>Одиночная плоская</td></tr><tr><td align="center">Fixed3D</td><td>Одиночная объемная</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<BorderStyle>None</BorderStyle>
```

### BackgroundImage <a href="#background_image" id="background_image"></a>

Путь до файла с графическим содержанием, которое будет расположено на панели.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<BackgroundImage>BackgroundImage</BackgroundImage>
```

### BackgroundImageLayout <a href="#background_image_layout" id="background_image_layout"></a>

Название типа расположения графического содержания на панели.

Необязательный тэг. Ожидается название одного из типов расположения графического содержания на панели:

<table data-header-hidden><thead><tr><th width="170" align="center"></th><th width="550.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Изображение выравнивается в панели вверху по левой стороне</td></tr><tr><td align="center">Tile</td><td>Выполняется мозаичное заполнение изображением панели</td></tr><tr><td align="center">Center</td><td>Изображение центрируется на панели</td></tr><tr><td align="center">Stretch</td><td>Изображение растягивается на всю длину панели</td></tr><tr><td align="center">Zoom</td><td>Изображение увеличивается в пределах панели</td></tr></tbody></table>

По умолчанию используется значение Tile.

```xml
<BackgroundImageLayout>Tile</BackgroundImageLayout>
```

### Gradient

Задает настройки градиентной заливки панель. Заливка отрисовывается поверх [BackgroundImage](./#background_image) и [BackColor](../#back_color).&#x20;

Необязательный тэг. Описание вложенных тэгов по [ссылке](gradient.md).

```xml
<Gradient>
  <StartColor>#8BC34A</StartColor>
  <FinishColor>#FBC02D</FinishColor>
  <Scale>100</Scale>
  <Mode>ForwardDiagonal</Mode>
</Gradient>
```

### MyObject <a href="#my_object" id="my_object"></a>

Объект, расположенный на данной панели.

Необязательный тэг. Тэгов `<MyObject>` может быть несколько.

```xml
<MyObject Name="ObjectName1" Type="ObjectType1" Assembly="ObjectAssembly1" />
<MyObject Name="ObjectName2" Type="ObjectType2" Assembly="ObjectAssembly2" />
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### HorizontalScroll <a href="#get_horizontal_scroll" id="get_horizontal_scroll"></a>

Возвращает признак наличия горизонтальной полосы прокрутки на панели.

```xml
<Object Name="PanelName">
  <Property Name="HorizontalScroll" />
</Object>
```

### VerticalScroll <a href="#get_vertical_scroll" id="get_vertical_scroll"></a>

Возвращает признак наличия вертикальной полосы прокрутки на панели.

```xml
<Object Name="PanelName">
  <Property Name="VerticalScroll" />
</Object>
```

### AutoScroll <a href="#get_auto_scroll" id="get_auto_scroll"></a>

Возвращает признак автоматической установки полос прокрутки на панели.

```xml
<Object Name="PanelName">
  <Property Name="AutoScroll" />
</Object>
```

### BorderStyle <a href="#get_border_style" id="get_border_style"></a>

Возвращает название типа границ таблицы.

```xml
<Object Name="PanelName">
  <Property Name="BorderStyle" />
</Object>
```

### BackgroundImage <a href="#get_background_image" id="get_background_image"></a>

Возвращает путь до файла с графическим содержанием, которое расположено на панели.

```xml
<Object Name="PanelName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#get_background_image_layout" id="get_background_image_layout"></a>

Возвращает название типа расположения графического содержания на панели.

```xml
<Object Name="PanelName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### ContainerChanged <a href="#get_container_changed" id="get_container_changed"></a>

Возвращает признак изменения объекта-контейнера (определяется как совокупность get-проперти `ValueChanged` всех его дочерних объектов на любом уровне вложенности).

```xml
<Object Name="PanelName">
  <Property Name="ContainerChanged" />
</Object>
```

### ChangedObjects <a href="#get_changed_objects" id="get_changed_objects"></a>

Возвращает список изменённых объектов.

```xml
<Object>
  <Property Name="ChangedObjects" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### HorizontalScroll <a href="#set_horizontal_scroll" id="set_horizontal_scroll"></a>

Задает признак наличия горизонтальной полосы прокрутки на панели.

Ожидается логическое значение.

```xml
<Object Name="PanelName">
  <Property Name="HorizontalScroll" />
</Object>
```

### VerticalScroll <a href="#set_vertical_scroll" id="set_vertical_scroll"></a>

Задает признак наличия вертикальной полосы прокрутки на панели.

Ожидается логическое значение.

```xml
<Object Name="PanelName">
  <Property Name="VerticalScroll" />
</Object>
```

### AutoScroll <a href="#set_auto_scroll" id="set_auto_scroll"></a>

Задает признак автоматической установки полос прокрутки на панели.

Ожидается логическое значение.

```xml
<Object Name="PanelName">
  <Property Name="AutoScroll" />
</Object>
```

### BorderStyle <a href="#set_border_style" id="set_border_style"></a>

Задает название типа границ панели.

Ожидается одно из названий типов границ панели.

```xml
<Object Name="PanelName">
  <Property Name="BorderStyle" />
</Object>
```

### BackgroundImage <a href="#set_background_image" id="set_background_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на панели.

Любое значение будет переведено в текстовое.

```xml
<Object Name="PanelName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#set_background_image_layout" id="set_background_image_layout"></a>

Задает название типа расположения графического содержания на панели.

Ожидается одно из названий типов расположения графического содержания на панели.

```xml
<Object Name="PanelName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### ContainerChanged <a href="#set_container_changed" id="set_container_changed"></a>

Задаёт признак изменения объекта-контейнера (определяется как совокупность get-проперти `ValueChanged` всех его дочерних объектов на любом уровне вложенности).

Ожидается логическое значение.

```xml
<Object Name="PanelName">
  <Property Name="ContainerChanged" />
</Object>
```
