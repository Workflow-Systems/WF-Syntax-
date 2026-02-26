# Селекторы

### Field <a href="#selector_field" id="selector_field"></a>

Селектор поля соединения с данными.

Добавляет в результат колонку исходного соединения с данными.

Значение тэга не ожидается.

```xml
<Field Name="FieldName" Field="SourceFieldName"/>
```

Необязательный атрибут `Field` - название поля исходного соединения с данными.&#x20;

Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.

### Value <a href="#selector_value" id="selector_value"></a>

Селектор значения.

Добавляет в результат колонку с именем из атрибута `Name` и типом данных из атрибута `DataType`. Для каждой строки в ячейку новой колонки ставиться значение, указанное в качестве значения тэга.

Ожидается любое значение.

```xml
<Field Name="FieldName" Type="Value" DataType="StringDataType">Value</Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Value.

Необязательный атрибут `DataType` - тип данных, в который будет преобразовано значение. Атрибут ожидает один из доступных [типов данных](https://wfsys.gitbook.io/workflow-mobile-forms-syntax/workflow_mobile_forms/data_types). По умолчанию используется значение StringDataType.

### Substitution <a href="#selector_substitution" id="selector_substitution"></a>

Селектор подстановки значений.

Добавляет в результат колонку с именем из атрибута `Name`, а значение для нее берет из матрицы подстановки по ключу из поля, указанному в атрибуте `Field`.

В качестве значения тэга ожидается матрица из 2-х столбцов. В первом столбце должен быть ключ, по которому будет идти подстановка, а во втором - значение, которое будет использоваться при подстановке.

```xml
<Field Name="FieldName" Type="Substitution" Field="FieldName"></Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Substitution.

Необязательный атрибут `Field` - название поля исходного соединения с данными. Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.

### Replace <a href="#selector_replace" id="selector_replace"></a>

Селектор замены значений в строке.

Добавляет в результат колонку с именем из атрибута `Name` и значением исходного соединения с данными с заменой в нём подстрок с использованием таблицы замены.

В качестве значения тэга ожидается матрица из 2-х столбцов. В первом столбце должен быть ключ, по которому будет идти замена, а во втором - значение, которое будет использоваться при замене.

```xml
<Field Name="FieldName" Type="Replace" Field="FieldName"></Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Replace.

Необязательный атрибут `Field` - название поля исходного соединения с данными. Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.

Замена происходит следующим образом: исходное значение преобразуется в текстовое, затем в строке последовательно заменяется значение из первого столбца таблицы замены на значение второго столбца таблицы замены.

<details>

<summary>Пример</summary>

```xml
<DataConnection Name="ClientConvertDataConnection" Type="ConvertDataConnection" Assembly="WorkflowServer">
  <SourceDataConnection Name="ClientPrimaryGetDataConnection" />
  <Fields>
    <Field Name="ClientId" />
    <Field Name="TitleForReplace" />
    <Field Name="Result" Type="Replace" Field="TitleForReplace">
      <DataConnection SourceDataConnection="CityPrimaryGetDataConnection">
        <Fields>
          <Field Name="CityId" />
          <Field Name="Title" />
        </Fields>
      </DataConnection>
    </Field>
  </Fields>
</DataConnection>
```

Где CityPrimaryGetDataConnection хранит данные:

```
+---+--------------+
| 1 | Екатеринбург |
| 2 | Челябинск    |
| 3 | Москва       |
+---+--------------+
```

Тогда в ClientConvertDataConnection будут храниться данные:

```
+---+------------------------------+----------------------------------------+
| 3 | Муравьёв Юпитер Антонович(3) | Муравьёв Юпитер Антонович(Москва)      |
| 4 | Самойлов Макар Игнатьевич(2) | Самойлов Макар Игнатьевич(Челябинск)   |
| 5 | Костина Афина Елизаровна(1)  | Костина Афина Елизаровна(Екатеринбург) |
+---+------------------------------+----------------------------------------+
```

</details>

### Format <a href="#selector_format" id="selector_format"></a>

Селектор форматирования строки.

Добавляет в результат колонку с именем из атрибута `Name` и результатом построения строки по шаблону со значениями полей исходного соединения с данными.

В качестве значения тэга ожидается строка-шаблон, с указанием в фигурных скобках `{}` имен полей исходного соединения с данными, которые будут источниками значений.

```xml
<Field Name="FieldName" Type="Format">{FieldName}</Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Format.

<details>

<summary>Пример</summary>

```xml
<DataConnection Name="CityConvertDataConnection" Type="ConvertDataConnection" Assembly="WorkflowServer">
  <SourceDataConnection Name="CityPrimaryGetDataConnection" />
  <Fields>
    <Field Name="CityId" />
    <Field Name="Title" />
    <Field Name="TitleFormat" Type="Format">{Title} (id: {CityId})</Field>
  </Fields>
</DataConnection>
```

Данные:

```
+---+--------------+----------------------+
| 1 | Екатеринбург | Екатеринбург (id: 1) |
| 2 | Челябинск    | Челябинск (id: 2)    |
| 3 | Москва       | Москва (id: 3)       |
+---+--------------+----------------------+
```

</details>

### TemplateFormat <a href="#selector_template_format" id="selector_template_format"></a>

Селектор форматирования строки по шаблону.

Добавляет в результат столбец с результатом форматирования полей исходного соединения с данными на основе заданного шаблона.

Ожидается строка с шаблоном.

```xml
<Field Name="FieldName" Type="TemplateFormat" Evaluate="True">Template</Field>
```

В качестве шаблонизатора используется Scriban. Подробнее по [ссылке](https://github.com/lunet-io/scriban).

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение TemplateFormat.

Необязательный атрибут `Evaluate` - признак, определяющий что нужно вычислить выражение. Ожидается логическое значение.

<details>

<summary>Пример</summary>

```xml
<DataConnection Name="CityConvertDataConnection" Type="ConvertDataConnection" Assembly="WorkflowServer">
  <SourceDataConnection Name="CityPrimaryGetDataConnection" />
  <Fields>
    <Field Name="CityId" />
    <Field Name="Title" />
    <Field Name="Archive" />
    <Field Name="TitleFormat" Type="TemplateFormat">{{Title}}{{if Archive}} (арх.){{end}}</Field>
  </Fields>
</DataConnection>
```

Данные:

```
+---+--------------+-------+---------------+
| 1 | Екатеринбург | False | Екатеринбург  |
| 2 | Челябинск    | False | Челябинск     |
| 3 | Москва       | True  | Москва (арх.) |
+---+--------------+-------+---------------+
```

</details>

### Action <a href="#selector_action" id="selector_action"></a>

Селектор работы с вложенными массивами.

Добавляет в результат соединения столбец с результатом преобразования массива из исходного соединения с данными.

{% hint style="warning" %}
Поле исходного соединения должно быть массивом.
{% endhint %}

Ожидается описание операций по работе с массивами, перечисленных в статье [Array](../../values/array.md).

```xml
<Field Name="FieldName" Type="Action" Field="FieldName">Array Operations</Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Action.

Необязательный атрибут `Field` - название поля исходного соединения с данными. Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.

<details>

<summary>Пример</summary>

```xml
<DataConnection Name="ClientConvertDataConnection" Type="ConvertDataConnection" Assembly="WorkflowServer">
  <SourceDataConnection Name="ClientPrimaryGetDataConnection" />
  <Fields>
    <Field Name="ClientId" />
    <Field Name="Title" />
    <Field Name="MaterialsAction" Type="Action" Field="Materials">
      <StringJoin Separator=", " />
    </Field>
    <Field Name="TotalPriceAction" Type="Action" Field="TotalPrice">
      <Sum Type="DecimalDataType" />
    </Field>
  </Fields>
</DataConnection>
```

Данные:

```
+---+---------------------------+----------------------------------+------+
| 2 | Яковлев Прохор Феликсович | Ручка шариковая, SvetoCopy пачка | 7375 |
| 3 | Муравьёв Юпитер Антонович |                                  |      |
| 4 | Самойлов Макар Игнатьевич | Линейка, Карандаш простой        | 270  |
| 5 | Костина Афина Елизаровна  | Ручка шариковая, SvetoCopy пачка | 5000 |
+---+---------------------------+----------------------------------+------+
```

</details>

### Object <a href="#selector_object" id="selector_object"></a>

Селектор полей объекта.

В результирующую таблицу будут добавлены поля вложенных селекторов.

{% hint style="warning" %}
Поле исходного соединения должно быть словарём.
{% endhint %}

Значение тэга `<Field>`: список тэгов [`<Field>`](selectors.md#fields_field).

```xml
<Field Field="FieldName" Type="Object">
  <Field Name="SubFieldName" />
</Field>
```

Обязательный атрибут `Field` - название поля исходного соединения с данными, из которого будут выбираться данные.

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Object.

### SubField <a href="#selector_sub_field" id="selector_sub_field"></a>

Селектор вложенного поля.

В результат добавится значение поля вложенного объекта. Является короткой версий селектора полей объекта.

{% hint style="warning" %}
Поле исходного соединения должно быть словарём.
{% endhint %}

Значение тэга `<Field>`: не ожидается.

```xml
<Field Name="FieldName" Type="SubField" Field="FieldName" SubField="SubFieldName"/>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение SubField.

Необязательный атрибут `Field` - название поля исходного соединения с данными. Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.

Обязательный атрибут `SubField` - название поля вложенного объекта. Ожидается название одного из полей объекта в поле, имя которого указано в атрибуте `Field` или `Name`, если атрибут `Field` отсутствует.

### Array <a href="#selector_array" id="selector_array"></a>

Селектор соединения массива объектов.

Может содержать любые селекторы. В результирующую таблицу будут добавлены поля вложенных селекторов.

{% hint style="warning" %}
Поле исходного соединения должно быть словарём.
{% endhint %}

Значение тэга `<Field>`: список тэгов [`<Field>`](selectors.md#fields_field).

```xml
<Field Name="FieldName" Field="FieldName" Type="Array">
  <Field Name="FieldName" />
</Field>
```

Обязательный атрибут `Type` - тип селектора. Имеет фиксированное значение Array.

Необязательный атрибут `Field` - название поля исходного соединения с данными. Если атрибут `Field` указан, то значение из атрибута `Name` используется как псевдоним для поля преобразованного соединения с данными. Если атрибут `Field` отсутствует, то будет использоваться значение из атрибута `Name` для получения данных из исходного соединения с данными.
