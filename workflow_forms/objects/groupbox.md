---
description: Графический объект; группирующая панель с каймой и заголовком.
---

# GroupBox

## Шаблон GroupBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="GroupBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для GroupBox-->
  <BackgroundImage></BackgroundImage>
  <BackgroundImageLayout></BackgroundImageLayout>
  <Text></Text>
  <MyObject Name="" Type="" Assembly="" />
  <MyObject Name="" Type="" Assembly="" />
</MyObject>
```

## Описание GroupBox <a href="#description" id="description"></a>

```xml
<MyObject Name="GroupBoxName" Type="GroupBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для GroupBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением GroupBox считается текст его заголовка.

```xml
<Object Name="GroupBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Любое значение будет переведено в текстовое.

```xml
<Object Name="GroupBoxName"></Object>
```

## Тэги, специфичные для GroupBox <a href="#specific-tags" id="specific-tags"></a>

### BackgroundImage <a href="#background_image" id="background_image"></a>

Путь до файла с графическим содержанием, которое будет расположено на панели.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<BackgroundImage>BackgroundImage</BackgroundImage>
```

### BackgroundImageLayout <a href="#background_image_layout" id="background_image_layout"></a>

Название типа расположения графического содержания на панели.

Необязательный тэг. Ожидается название одного из типов расположения графического содержания на панели:

<table data-header-hidden><thead><tr><th width="164.09690937663703" align="center"></th><th width="535.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Изображение выравнивается в панели вверху по левой сторон</td></tr><tr><td align="center">Tile</td><td>Выполняется мозаичное заполнение изображением панели</td></tr><tr><td align="center">Center</td><td>Изображение центрируется на панели</td></tr><tr><td align="center">Stretch</td><td>Изображение растягивается на всю длину панели</td></tr><tr><td align="center">Zoom</td><td>Изображение увеличивается в пределах панели</td></tr></tbody></table>

По умолчанию используется значение Tile.

```xml
<BackgroundImageLayout>Tile</BackgroundImageLayout>
```

### Text <a href="#text" id="text"></a>

Заголовок панели.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Text>Заголовок</Text>
```

### MyObject <a href="#my_object" id="my_object"></a>

Объект, расположенный на данной панели.

Необязательный тэг. Тэгов `<MyObject>` может быть несколько.

```xml
<MyObject Name="ObjectName1" Type="ObjectType1" Assembly="ObjectAssembly1" />
<MyObject Name="ObjectName2" Type="ObjectType2" Assembly="ObjectAssembly2" />
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### BackgroundImage <a href="#get_background_image" id="get_background_image"></a>

Возвращает путь до файла с графическим содержанием, которое расположено на панели.

```xml
<Object Name="GroupBoxName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#get_background_image_layout" id="get_background_image_layout"></a>

Возвращает название типа расположения графического содержания на панели.

```xml
<Object Name="GroupBoxName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### ContainerChanged <a href="#get_container_changed" id="get_container_changed"></a>

Возвращает признак изменения объекта-контейнера (определяется как совокупность get-проперти `ValueChanged` всех его дочерних объектов на любом уровне вложенности).

```xml
<Object Name="GroupBoxName">
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

### Text <a href="#get_text" id="get_text"></a>

Возвращает заголовок панели.

```xml
<Object Name="GroupBoxName">
  <Property Name="Text" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### BackgroundImage <a href="#set_background_image" id="set_background_image"></a>

Задает путь до файла с графическим содержанием, которое будет расположено на панели.

Любое значение будет переведено в текстовое.

```xml
<Object Name="GroupBoxName">
  <Property Name="BackgroundImage" />
</Object>
```

### BackgroundImageLayout <a href="#set_background_image_layout" id="set_background_image_layout"></a>

Задает название типа расположения графического содержания на панели.

Ожидается одно из названий типов расположения графического содержания на панели.

```xml
<Object Name="GroupBoxName">
  <Property Name="BackgroundImageLayout" />
</Object>
```

### ContainerChanged <a href="#set_container_changed" id="set_container_changed"></a>

Задаёт признак изменения объекта-контейнера (определяется как совокупность get-проперти `ValueChanged` всех его дочерних объектов на любом уровне вложенности).

Ожидается логическое значение.

```xml
<Object Name="GroupBoxName">
  <Property Name="ContainerChanged" />
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает заголовок панели.

Любое значение будет переведено в текстовое.

```xml
<Object Name="GroupBoxName">
  <Property Name="Text">Заголовок</Property>
</Object>
```
