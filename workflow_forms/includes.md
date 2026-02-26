---
description: Документы, содержимое которых будет включено в текущий документ.
---

# Includes

## Описание Include <a href="#description_include" id="description_include"></a>

```xml
<Include Path = "IncludeDocument.xml" />
```

### Атрибуты Include <a href="#attributes_include" id="attributes_include"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="464.3333333333333"></th></tr></thead><tbody><tr><td align="center">Path</td><td><p>Путь до xml-файла документа.</p><p></p><p>Обязательный атрибут.</p></td></tr></tbody></table>

## Описание процесса включения документов <a href="#description_include_document" id="description_include_document"></a>

Включаемый файл представляет собой xml-файл формы.

При включении производится поиск тэгов `<Include>` в блоке `<Includes>`.

Если тэги присутствуют в текущем документе, то xml-документ, указанный в атрибуте `Path`, загружается.

В загруженном документе так же производится поиск тэгов `<Include>`, тем самым поддерживается любой уровень вложенности документов.

При этом, если файл был загружен ранее, то повторно он загружен не будет.

После загрузки документа для включения все тэги внутри корневного тэга `<Forms>` копируются в вышестоятещий документ. Если в вышестоящем документе присутствует тэг, например `<DataConnections>`, то из документа-включения копируются тэги внутри `<DataConnections>` в тэг `<DataConnections>` вышестоящего документа.

### Пример простого включения документа <a href="#include_document_example_1" id="include_document_example_1"></a>

Файл Form1.xml

```xml
<Forms>
  <Includes>
    <Include Path="Form2.xml" />
  </Includes>
  <MyObjects>
    <MyObject Name="Panel" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```

Файл Form2.xml

```xml
<Forms>
  <Appearance>
    <Colors>
      <Color Name="Red" Red="255" Green="0" Blue="0" Alpha="255" />
    </Colors>
  </Appearance>
  <MyObjects>
    <MyObject Name="Panel2" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```

Итоговый документ после включения Form2.xml в Form1.xml

```xml
<Forms>
  <Includes>
    <Include Path="Form2.xml" />
  </Includes>
  <Appearance>
    <Colors>
      <Color Name="Red" Red="255" Green="0" Blue="0" Alpha="255" />
    </Colors>
  </Appearance>
  <MyObjects>
    <MyObject Name="Panel" Type="Panel" Assembly="BaseControls"></MyObject>
    <MyObject Name="Panel2" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```

### Пример включения документов с вложенными документами <a href="#include_document_example_2" id="include_document_example_2"></a>

Файл Form1.xml

```xml
<Forms>
  <Includes>
    <Include Path="Form2.xml" />
  </Includes>
  <MyObjects>
    <MyObject Name="Panel" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```

Файл Form2.xml

```xml
<Forms>
  <Includes>
    <Include Path="Form3.xml" />
  </Includes>
  <MyObjects>
    <MyObject Name="Panel2" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```

Файл Form3.xml

```xml
<Forms>
  <Appearance>
    <Colors>
      <Color Name="Red" Red="255" Green="0" Blue="0" Alpha="255" />
    </Colors>
  </Appearance>
</Forms>
```

Итоговый документ после включения Form3.xml в Form2.xml, который был включен в Form1.xml

```xml
<Forms>
  <Includes>
    <Include Path="Form2.xml" />
  </Includes>
  <Appearance>
    <Colors>
      <Color Name="Red" Red="255" Green="0" Blue="0" Alpha="255" />
    </Colors>
  </Appearance>
  <MyObjects>
    <MyObject Name="Panel" Type="Panel" Assembly="BaseControls"></MyObject>
    <MyObject Name="Panel2" Type="Panel" Assembly="BaseControls"></MyObject>
  </MyObjects>
</Forms>
```
