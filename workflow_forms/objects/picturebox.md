---
description: Графический объект; поле с изображением.
---

# PictureBox

## Шаблон PictureBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="PictureBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для PictureBox-->
  <SizeMode></SizeMode>
  <InitialImage></InitialImage>
  <ErrorImage></ErrorImage>
  <WaitOnLoad></WaitOnLoad>
  <NullImage></NullImage>
  <Image></Image>
  <ImagesLoad Value="" />
  <ImagesList></ImagesList>
</MyObject>
```

## Описание PictureBox <a href="#description" id="description"></a>

```xml
<MyObject Name="PictureBoxName" Type="PictureBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для PictureBox-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением PictureBox считается источник текущего отображаемого изображения.

```xml
<Object Name="PictureBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Значение объекта: любое значение будет интерпретировано как источник.

```xml
<Object Name="PictureBoxName"></Object>
```

## Тэги, специфичные для PictureBox <a href="#specific-tags" id="specific-tags"></a>

### SizeMode <a href="#size_mode" id="size_mode"></a>

Название типа размера изображения.

Необязательный тэг. Ожидается название одного из типов размеров изображения:

<table data-header-hidden><thead><tr><th width="165.33333333333331" align="center"></th><th width="540.1606663084364"></th></tr></thead><tbody><tr><td align="center">AutoSize</td><td>Изображение располагается в левом верхнем углу</td></tr><tr><td align="center">CenterImage</td><td>Если поле больше изображения, то изображение отображается в центре; если изображение больше поля, то рисунок размещается в центре, а его внешние края обрезаются</td></tr><tr><td align="center">Normal</td><td>Изображение размещается в верхнем левом углу; изображение располагается в центре, если размер поля больше, чем размер изображения</td></tr><tr><td align="center">StretchImage</td><td>Изображение вытягивается или сужается, чтобы в точности соответствовать размеру</td></tr><tr><td align="center">Zoom</td><td>Размер изображения увеличивается или уменьшается, сохраняя пропорции размеров</td></tr></tbody></table>

По умолчанию используется значение Zoom.

```xml
<SizeMode>Zoom</SizeMode>
```

### InitialImage <a href="#initial_image" id="initial_image"></a>

Источник изображения, которое будет использоваться в качестве изображения поля, пока в асинхронном режиме загружается требуемое. Начальная загрузка изображения из источника для `<InitialImage>` всегда происходит синхронно, вне зависимости от значения свойства [`<WaitOnLoad>`](picturebox.md#wait_on_load).

Необязательный тэг. Ожидается источник изображения.

Если тэг `<InitialImage>` отсутствует, то в момент загрузки требуемого изображения никаких изменений в поле не будет происходить.

```xml
<InitialImage>Images\InitialImage.gif</InitialImage>
```

### ErrorImage <a href="#error_image" id="error_image"></a>

Источник изображения, которое будет использоваться в качестве изображения поля, если требуемое не было загружено. Начальная загрузка изображения из источника для `<ErrorImage>` всегда происходит синхронно, вне зависимости от значения свойства [`<WaitOnLoad>`](picturebox.md#wait_on_load).

Необязательный тэг. Ожидается источник изображения.

Если тэг `<ErrorImage>` отсутствует, то в случае ошибки загрузки требуемого изображения никаких изменений в поле не будет ничего происходить.

```xml
<ErrorImage>D:\ErrorImage.png</ErrorImage>
```

### WaitOnLoad <a href="#wait_on_load" id="wait_on_load"></a>

Признак, определяющий, будет ли загрузка изображений происходить в синхронном режиме.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<WaitOnLoad>False</WaitOnLoad>
```

### NullImage <a href="#null_image" id="null_image"></a>

Источник изображения, которое будет использоваться в качестве изображения поля, если значение поля установлено в NULL.

Необязательный тэг. Ожидается источник изображения.

Если тэг `<NullImage>` отсутствует, то в случае установки NULL-значения в поле не будет ничего происходить.

```xml
<NullImage>D:\NullImage.jpg</NullImage>
```

### Image <a href="#image" id="image"></a>

Источник изображения, которое будет использоваться в качестве начального отображаемого изображения при загрузке формы.

Необязательный тэг. Ожидается источник изображения.

Если тэг `<Image>` отсутствует, то в качестве начального изображения будет использовано первое изображения из списка, указанного в тэге [`<ImagesList>`](picturebox.md#images_list).

```xml
<Image>http://wfsys.ru/image.bmp</Image>
```

#### Источники изображений <a href="#image_sources" id="image_sources"></a>

1. Сокращенный путь до файла - например, "Images\Sample.png" (в качестве исходной папки будет взята папка с расположением формы, на которой описано данное поле).
2. Полный путь до файла в формате UNC - например, "D:\sample.jpg" или "\SERVER\Images\sample.bmp".
3. Ссылка на интернет-ресурс по протоколам http://, https:// или ftp:// - например, "[http://wfsys.ru/sample.png](http://wfsys.ru/sample.png)".
4. Ссылка на GUID файла, расположенного на сервере, - например, "guid://cbed3d33-7591-49ff-8119-8ad7e3c81599".

### ImagesLoad <a href="#images_load" id="images_load"></a>

Тип загрузки изображений из списка, указанного в тэге [`<ImagesList>`](picturebox.md#images_list).

Необязательный тэг. Значение тэга `<ImagesLoad>`: не ожидается.

Если тэг [`<ImagesList>`](picturebox.md#images_list) отсутствует, то для атрибута `Value` используется значение ByRequest.

```xml
<ImagesLoad Value="ByRequest" />
```

#### Атрибуты тэга `<ImagesLoad>` <a href="#attributes_tag_images_load" id="attributes_tag_images_load"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="519"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается название одного из типов загрузки изображений.</p></td></tr></tbody></table>

#### Типы загрузки изображений <a href="#images_load_types" id="images_load_types"></a>

<table data-header-hidden><thead><tr><th width="150" align="center"></th><th width="491"></th></tr></thead><tbody><tr><td align="center">ByRequest</td><td>Изображения будут загружаться только в том случае, если их требуется отобразить</td></tr><tr><td align="center">All</td><td>Все изображения будут загружены при загрузке формы</td></tr></tbody></table>

### ImagesList <a href="#images_list" id="images_list"></a>

Список источников изображений, которые будут использоваться в качестве изображений для установки в поле.

Необязательный тэг. Ожидается массив источников изображений.

Если тэг `<ImagesList>` отсутствует, то в качестве начального изображения будет использовано изображение из источника, указанного в тэге [`<NullImage>`](picturebox.md#null_image).

```xml
<ImagesList>
  <DataConnection SourceDataConnection="SourceDataConnectionName">
    <Fields>
      <Field Name="ImageSource" />
    </Fields>
  </DataConnection>
</ImagesList>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### SizeMode <a href="#get_size_mode" id="get_size_mode"></a>

Возвращает название типа размера изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="SizeMode" />
</Object>
```

### InitialImage <a href="#get_initial_image" id="get_initial_image"></a>

Возвращает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, пока в асинхронном режиме загружается требуемое.

```xml
<Object Name="PictureBoxName">
  <Property Name="InitialImage" />
</Object>
```

### ErrorImage <a href="#get_error_image" id="get_error_image"></a>

Возвращает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, если требуемое изображение не было загружено.

```xml
<Object Name="PictureBoxName">
  <Property Name="ErrorImage" />
</Object>
```

### WaitOnLoad <a href="#get_wait_on_load" id="get_wait_on_load"></a>

Возвращает признак, определяющий, будет ли загрузка изображений происходить в синхронном режиме.

```xml
<Object Name="PictureBoxName">
  <Property Name="WaitOnLoad" />
</Object>
```

### NullImage <a href="#get_null_image" id="get_null_image"></a>

Возвращает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, если значение поля установлено в NULL.&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="NullImage" />
</Object>
```

### Image <a href="#get_image" id="get_image"></a>

Возвращает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве начального отображаемого изображения при загрузке формы.&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="Image" />
</Object>
```

### ImagesLoad <a href="#get_images_load" id="get_images_load"></a>

Возвращает тип загрузки изображений из списка, указанного в тэге [`<ImagesList>`](picturebox.md#images_list).&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="ImagesLoad" />
</Object>
```

### ImagesList <a href="#get_images_list" id="get_images_list"></a>

Возвращает массив источников изображений, которые будут использоваться в качестве изображений для установки в поле.&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="ImagesList" />
</Object>
```

### Count <a href="#get_count" id="get_count"></a>

Возвращает общее количество изображений в списке [`<ImagesList>`](picturebox.md#images_list).&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="Count" />
</Object>
```

### CurrentImageIndex <a href="#get_current_image_index" id="get_current_image_index"></a>

Возвращает индекс отображаемого изображения (-1 - если установлено изображение из настройки [`<Image>`](picturebox.md#image), 0 - если установлено изображение из настройки [`<NullImage>`](picturebox.md#null_image), от 1 до N - если установлено изображение из списка [`<ImagesList>`](picturebox.md#images_list), где N - общее количество изображений в этом списке).&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="CurrentImageIndex" />
</Object>
```

### CurrentImageSource <a href="#get_current_image_source" id="get_current_image_source"></a>

Возвращает источник отображаемого изображения.&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="CurrentImageSource" />
</Object>
```

### CurrentRealImageSource <a href="#get_current_real_image_source" id="get_current_real_image_source"></a>

Возвращает источник изображения даже если это изображение не отображается, а отображается [`<ErrorImage>`](picturebox.md#error_image).&#x20;

```xml
<Object Name="PictureBoxName">
  <Property Name="CurrentRealImageSource" />
</Object>
```

### IsCurrentImageSourceError <a href="#get_is_current_image_source_error" id="get_is_current_image_source_error"></a>

Возвращает True или False в зависимости от того, была ли ошибка в загрузке текущего изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="IsCurrentImageSourceError" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### SizeMode <a href="#set_size_mode" id="set_size_mode"></a>

Задает название типа размера изображения.

Ожидается название одного из типов размеров изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="SizeMode">StretchImage</Property>
</Object>
```

### InitialImage <a href="#set_initial_image" id="set_initial_image"></a>

Задает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, пока в асинхронном режиме загружается требуемое.

Ожидается источник изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="InitialImage">ftp://wfsys.ru/Image.png</Property>
</Object>
```

### ErrorImage <a href="#set_error_image" id="set_error_image"></a>

Задает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, если требуемое не было загружено.

Ожидается источник изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="ErrorImage">D:\ErrorImage.bmp</Property>
</Object>
```

### WaitOnLoad <a href="#set_wait_on_load" id="set_wait_on_load"></a>

Задает признак, определяющий, будет ли загрузка изображений происходить в синхронном режим.

Ожидается логическое значение.

```xml
<Object Name="PictureBoxName">
  <Property Name="WaitOnLoad">True</Property>
</Object>
```

### NullImage <a href="#set_null_image" id="set_null_image"></a>

Задает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве изображения поля, если значение поля установлено в NULL.

Ожидается источник изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="NullImage">\\SHARE\Images\NullImage.png</Property>
</Object>
```

### Image <a href="#set_image" id="set_image"></a>

Задает [источник изображения](picturebox.md#image_sources), которое будет использоваться в качестве начального отображаемого изображения при загрузке формы.

Ожидается источник изображения.

```xml
<Object Name="PictureBoxName">
  <Property Name="Image">guid://26c7d4b6-2b4a-48f3-bde1-def012932219</Property>
</Object>
```

### ImagesList <a href="#set_images_list" id="set_images_list"></a>

Задает список [источников изображений](picturebox.md#image_sources), которые будут использоваться в качестве изображений для установки в поле. При наличии в новом списке ранее загруженных изображений (по совпадению источника) их перезагрузка не происходит.

Ожидается массив источников изображений.

```xml
<Object Name="PictureBoxName">
  <Property Name="ImagesList">
    <DataConnection SourceDataConnection="SourceDataConnectionName">
      <Fields>
        <Field Name="ImageSource" />
      </Fields>
    </DataConnection>
  </Property>
</Object>
```

### Open <a href="#set_open" id="set_open"></a>

Открывает файл изображения с индексом ImageIndex, предварительно при необходимости перезагрузив его в соответствии с признаком ForceRefresh.

```xml
<Object Name="PictureBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Open">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ImageIndex: ожидается целочисленное значение-->
      <!--Необязательный параметр. При отсутствии или значении NULL открывает текущее отображаемое изображение-->
      <Parameter Name="ImageIndex">1</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ForceRefresh: ожидается логическое значение-->
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <Parameter Name="ForceRefresh">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Next <a href="#set_next" id="set_next"></a>

Устанавливает в качестве текущего следующее по списку [`<ImagesList>`](picturebox.md#images_list) изображение, предварительно при необходимости перезагрузив его в соответствии с признаком ForceRefresh.

```xml
<Object Name="PictureBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Next">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ForceRefresh: ожидается логическое значение-->
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <Parameter Name="ForceRefresh">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Prev <a href="#set_prev" id="set_prev"></a>

Устанавливает в качестве текущего предыдущее по списку [`<ImagesList>`](picturebox.md#images_list) изображение, предварительно при необходимости перезагрузив его в соответствии с признаком ForceRefresh.

```xml
<Object Name="PictureBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Prev">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ForceRefresh: ожидается логическое значение-->
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <Parameter Name="ForceRefresh">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Show <a href="#set_show" id="set_show"></a>

Устанавливает в качестве текущего изображение с индексом ImageIndex, предварительно при необходимости перезагрузив его в соответствии с признаком ForceRefresh.

```xml
<Object Name="PictureBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Show">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ImageIndex: ожидается целочисленное значение-->
      <Parameter Name="ImageIndex">1</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным ForceRefresh: ожидается логическое значение-->
      <!--Необязательный параметр. При отсутствии используется значение False-->
      <Parameter Name="ForceRefresh">False</Parameter>
    </Parameters>
  </Property>
</Object>
```

### Refresh <a href="#set_refresh" id="set_refresh"></a>

Перезагружает изображение с индексом ImageIndex.

```xml
<Object Name="PictureBoxName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="Refresh">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ImageIndex: ожидается целочисленное значение-->
      <!--Необязательный параметр. При отсутствии или значении NULL перезагружает все изображения из списка ImagesList-->
      <Parameter Name="ImageIndex">1</Parameter>
    </Parameters>
  </Property>
</Object>
```
