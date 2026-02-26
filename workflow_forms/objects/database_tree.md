---
description: Графический объект; дерево значений.
---

# DatabaseTree

## Шаблон DatabaseTree <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="DatabaseTree" Assembly="ComplexControls" ChangeForm="">
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
  <!--Тэги, специфичные для DatabaseTree-->
  <BorderStyle></BorderStyle>
  <HideSelection></HideSelection>
  <Sorted></Sorted>
  <Items>
    <DataConnection SourceDataConnection="VariantRelationPrimaryGetDataConnection">
      <SourceQuery Name="ItemVariant">
        <Fields>
          <Field Name="" />
          <Field Name="" />
        </Fields>
      </SourceQuery>
      <SourceQuery Name="VariantVariant">
        <Fields>
          <Field Name="" />
          <Field Name="" />
          <Field Name="" />
        </Fields>
      </SourceQuery>
    </DataConnection>
  </Items>
  <TopItems></TopItems>
</MyObject>
```

## Описание DatabaseTree <a href="#description" id="description"></a>

```xml
<MyObject Name="DatabaseTreeName" Type="DatabaseTree" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для DatabaseTree-->
</MyObject>
```

### Получение значения <a href="#get-value" id="get-value"></a>

Значением DatabaseTree считается значение выделенного узла.

```xml
<Object Name="DatabaseTreeName" />
```

Задать значение DatabaseTree нельзя.

## Тэги, специфичные для DatabaseTree <a href="#specific-tags" id="specific-tags"></a>

### BorderStyle <a href="#border_style" id="border_style"></a>

Название типа границ дерева.

Необязательный тэг. Ожидается название одного из типов границ дерева:

<table data-header-hidden><thead><tr><th align="center"></th><th width="461.3333333333333"></th></tr></thead><tbody><tr><td align="center">None</td><td>Нет границ</td></tr><tr><td align="center">FixedSingle</td><td>Одиночная плоская</td></tr><tr><td align="center">Fixed3D</td><td>Одиночная объемная</td></tr></tbody></table>

По умолчанию используется значение FixedSingle.

```xml
<BorderStyle>FixedSingle</BorderStyle>
```

### HideSelection <a href="#hide_selection" id="hide_selection"></a>

Признак видимости выделенного элемента в дереве.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение True.

```xml
<HideSelection>True</HideSelection>
```

### Sorted <a href="#sorted" id="sorted"></a>

Признак сортировки элементов дерева по отображаемым значениям.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Sorted>False</Sorted>
```

### Items <a href="#items" id="items"></a>

Элементы дерева и их взаимосвязи списка.

Обязательный тэг. Ожидается соединение с данными с двумя таблицами: одна с двумя полями, другая - с двумя или тремя.

Первая таблица соответствует линейному списку элементов дерева: первое поле будет соответствовать идентификатору элемента, второе - его отображаемому значению.

Вторая таблица соответствует взаимосвязям элементов дерева: первое поле будет соответствовать дочернему идентификатору элемента, второе - родительскому, а третье (необязательное поле) - признаку видимости данной взаимосвязи.

Один элемент может входить в несколько родительских элементов.

```xml
<Items>
  <DataConnection SourceDataConnection="VariantRelationPrimaryGetDataConnection">
    <SourceQuery Name="ItemVariant">
      <Fields>
        <Field Name="VariantId" />
        <Field Name="ViewItemTitle" />
      </Fields>
    </SourceQuery>
    <SourceQuery Name="VariantVariant">
      <Fields>
        <Field Name="ChildVariantId" />
        <Field Name="ParentVariantId" />
        <Field Name="VariantBase" />
      </Fields>
    </SourceQuery>
  </DataConnection>
</Items>
```

### TopItems <a href="#top_items" id="top_items"></a>

Идентификаторы узлов верхнего уровня дерева.

Необязательный тэг. Ожидается массив любых значений или любое скалярное значение.

Если тэг `<TopItems>` отсутствует, то значения верхнего уровня находятся автоматически.

```xml
<TopItems>1</TopItems>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### BorderStyle <a href="#get_border_style" id="get_border_style"></a>

Возвращает название типа границ дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="BorderStyle" />
</Object>
```

### HideSelection <a href="#get_hide_selection" id="get_hide_selection"></a>

Возвращает признак видимости выделенного элемента в дереве.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="HideSelection" />
</Object>
```

### Sorted <a href="#get_sorted" id="get_sorted"></a>

Возвращает признак сортировки элементов дерева по отображаемым значениям.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="Sorted" />
</Object>
```

### SelectedItemId <a href="#get_selected_item_id" id="get_selected_item_id"></a>

Возвращает идентификатор выделенного узла дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="SelectedItemId" />
</Object>
```

### SelectedItemTitle <a href="#get_selected_item_title" id="get_selected_item_title"></a>

Возвращает отображаемое значение выделенного узла дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="SelectedItemTitle" />
</Object>
```

### ParentSelectedItemId <a href="#get_parent_selected_item_id" id="get_parent_selected_item_id"></a>

Возвращает идентификатор родительского узла дерева по отношению к выделенному узлу.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ParentSelectedItemId" />
</Object>
```

### ItemsParentalRelation <a href="#get_items_parental_relation" id="get_items_parental_relation"></a>

Возвращает признак, определяющий, входит ли узел дерева с идентификатором PossibleChildItemId в узел с идентификатором PossibleParentItemId.

```xml
<Object Name="DatabaseTreeName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ItemsParentalRelation">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным PossibleChildItemId: ожидается любое значение, равное идентификатору узла дерева-->
      <Parameter Name="PossibleChildItemId">ChildNodeId</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным PossibleParentItemId: ожидается любое значение, равное идентификатору узла дерева-->
      <Parameter Name="PossibleParentItemId">ParentNodeId</Parameter>
    </Parameters>
  </Property>
</Object>
```

### SelectedNodeHasChildren <a href="#get_selected_node_has_children" id="get_selected_node_has_children"></a>

Возвращает признак, определяющий, имеет ли выделенный узел дочерние узлы.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="SelectedNodeHasChildren" />
</Object>
```

### ItemTitleByItemId <a href="#get_item_title_by_item_id" id="get_item_title_by_item_id"></a>

Возвращает отображаемое значение узла дерева по его идентификатору.

```xml
<Object Name="DatabaseTreeName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ItemTitleByItemId">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается любое значение, равное идентификатору узла дерева-->
      <Parameter Name="Value">NodeId</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ItemAdded <a href="#get_item_added" id="get_item_added"></a>

Возвращает признак, определяющий, был ли узел дерева с указанным идентификатором сохранен в базе данных.

```xml
<Object Name="DatabaseTreeName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ItemAdded">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным Value: ожидается любое значение, равное идентификатору узла дерева-->
      <Parameter Name="Value">NodeId</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ExpandedNodesIds <a href="#get_expanded_nodes_ids" id="get_expanded_nodes_ids"></a>

Возвращает массив идентификаторов открытых (видимых) элементов.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ExpandedNodesIds" />
</Object>
```

### SelectedItemLevel <a href="#get_selected_item_level" id="get_selected_item_level"></a>

Возвращает номер уровня, на котором находится выделенный в дереве элемент.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="SelectedItemLevel" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### BorderStyle <a href="#set_border_style" id="set_border_style"></a>

Задает название типа границ дерева.

Ожидается название одного из типов границ дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="BorderStyle">Fixed3D</Property>
</Object>
```

### HideSelection <a href="#set_hide_selection" id="set_hide_selection"></a>

Задает признак видимости выделенного элемента в дереве.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="HideSelection">True</Property>
</Object>
```

### Sorted <a href="#set_sorted" id="set_sorted"></a>

Задает признак сортировки элементов дерева по отображаемым значениям.

Ожидается логическое значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="Sorted">True</Property>
</Object>
```

### SelectedItemId <a href="#set_selected_item_id" id="set_selected_item_id"></a>

Задает идентификатор выделенного узла дерева.

Ожидается любое значение, равное идентификатору узла дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="SelectedItemId">NodeId</Property>
</Object>
```

### InsertItem <a href="#set_insert_item" id="set_insert_item"></a>

Добавляет в узел ParentItemId дерева новый узел с идентификатором ItemId, отображаемым значением ItemTitle, добавленный узел выделяется в соответствии с признаком SelectAfterAdd.

```xml
<Object Name="DatabaseTreeName">
  <!--Значение тэга Property: ожидается любое значение-->
  <Property Name="InsertItem">
    <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ItemId: ожидается любое значение с идентификатором добавляемого узла-->
      <!--Если узел с данным идентификатором уже есть в дереве, новый узел добавлен не будет-->
      <Parameter Name="ItemId">-1</Parameter>
      <!--Необязательный параметр. При отсутствии используется пустая строка-->
      <!--Значение тэга Parameter с атрибутом Name, равным ItemTitle: ожидается любое значение с отображаемым названием добавляемого узла-->
      <Parameter Name="ItemTitle">NodeTitle</Parameter>
      <!--Необязательный параметр. При отсутствии узел будет добавлен на верхний уровень дерева-->
      <!--Значение тэга Parameter с атрибутом Name, равным ParentItemId: ожидается любое значение, равное идентификатору узла дерева, к которому будет добавляться новый узел-->
      <!--Если узел с переданным родительским идентификатором отсутствует в дереве, то новый узел добавлен не будет-->
      <Parameter Name="ParentItemId">0</Parameter>
      <!--Необязательный параметр. При отсутствии используется значение True-->
      <!--Значение тэга Parameter с атрибутом Name, равным SelectAfterInsert: ожидается логическое значение-->
      <Parameter Name="SelectAfterInsert">True</Parameter>
    </Parameters>
  </Property>
</Object>
```

### InsertItemIntoSelectedNode <a href="#set_insert_item_into_selected_node" id="set_insert_item_into_selected_node"></a>

Добавляет новый узел с отображаемым значением и идентификатором -1 в выделенный узел дерева.

Ожидается любое значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="InsertItemIntoSelectedNode">NodeTitle</Property>
</Object>
```

### UpdateSelectedItemTitle <a href="#set_update_selected_item_title" id="set_update_selected_item_title"></a>

Изменяет отображаемое значение выделенного узла дерева.

Ожидается любое значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="UpdateSelectedItemTitle">NewNodeTitle</Property>
</Object>
```

### DeleteSelectedItem <a href="#set_delete_selected_item" id="set_delete_selected_item"></a>

Удаляет выделенный узел дерева.

Значение тэга Property: не ожидается.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="DeleteSelectedItem" />
</Object>
```

### TransferSelectedItem <a href="#set_transfer_selected_item" id="set_transfer_selected_item"></a>

Переносит выделенный узел дерева в указанный.

Ожидается любое значение, равное идентификатору узла дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="TransferSelectedItem">NodeId</Property>
</Object>
```

### TransferItem <a href="#set_transfer_item" id="set_transfer_item"></a>

Переносит один узел дерева в другой.

```xml
<Object Name="DatabaseTreeName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="TransferItem">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным SourceNodeId: ожидается любое значение, равное идентификатору узла дерева, соответствующее переносимому узлу-->
      <Parameter Name="SourceNodeId">SourceNodeId</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным DestinationNodeId: ожидается любое значение, равное идентификатору узла дерева, в который будет осуществлен перенос-->
      <Parameter Name="DestinationNodeId">DestinationNodeId</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ReplaceItemVisibility <a href="#set_replace_item_visibility" id="set_replace_item_visibility"></a>

Изменяет видимость элемента с идентификатором OldNodeIdVisible на видимость элемента с идентификатором NewNodeIdVisible в рамках одного родительского узла с идентификатором ParentItemId.

```xml
<Object Name="DatabaseTableName">
  <!--Значение тэга Property: тэг Parameters со вложенными тэгами Parameter-->
  <Property Name="ReplaceItemVisibility">
    <Parameters>
      <!--Значение тэга Parameter с атрибутом Name, равным ParentItemId: ожидается любое значение, равное идентификатору узла дерева, соответствующее родительскому узлу-->
      <Parameter Name="ParentItemId">ParentNodeId</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным OldNodeIdVisible: ожидается любое значение, равное идентификатору узла дерева в рамках одного родительского узла-->
      <Parameter Name="OldNodeIdVisible">OldNodeId</Parameter>
      <!--Значение тэга Parameter с атрибутом Name, равным NewNodeIdVisible: ожидается любое значение, равное идентификатору узла дерева в рамках одного родительского узла-->
      <Parameter Name="NewNodeIdVisible">NewNodeId</Parameter>
    </Parameters>
  </Property>
</Object>
```

### ExpandNodeId <a href="#set_expand_node_id" id="set_expand_node_id"></a>

Раскрывает указанный узел дерева.

Ожидается любое значение, равное идентификатору узла дерева.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ExpandNodeId">NodeId</Property>
</Object>
```

### ExpandNodeTitle <a href="#set_expand_node_title" id="set_expand_node_title"></a>

Раскрывает узел дерева, содержащий определенный текст.

Ожидается любое значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ExpandNodeTitle">NodeTitle</Property>
</Object>
```

### ExpandAll <a href="#set_expand_all" id="set_expand_all"></a>

Раскрывает все узлы дерева.

Значение тэга Property: не ожидается.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ExpandAll" />
</Object>
```

### ExpandLevel <a href="#set_expand_level" id="set_expand_level"></a>

Раскрывает все узлы дерева до определенного уровня.

Ожидается целочисленное значение.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ExpandLevel">1</Property>
</Object>
```

### CollapseAll <a href="#set_collapse_all" id="set_collapse_all"></a>

Сворачивает все узлы дерева.

Значение тэга Property: не ожидается.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="CollapseAll" />
</Object>
```

### ClearSelection <a href="#set_clear_selection" id="set_clear_selection"></a>

Сбрасывает текущее выделение узла дерева.

Значение тэга Property: не ожидается.

```xml
<Object Name="DatabaseTreeName">
  <Property Name="ClearSelection" />
</Object>
```
