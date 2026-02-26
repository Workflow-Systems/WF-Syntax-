---
description: Поле для ввода и редактирования текста. Элемент пользовательского интерфейса.
---

# TextBox

## Шаблон TextBox <a href="#template" id="template"></a>

Перечень всех возможных тэгов объекта:

```xml
<MyObject Name="" Type="TextBox" Assembly="BaseControls" ChangeForm="">
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
  <!--Тэги, специфичные для TextBox-->
  <MaxLength></MaxLength>
  <ReadOnly></ReadOnly>
  <Multiline></Multiline>
  <Password></Password>
  <ShowPasswordButton></ShowPasswordButton>
  <AllowedSymbols></AllowedSymbols>
  <InputLanguage></InputLanguage>
  <InputCase></InputCase>
  <SelectOnEnter></SelectOnEnter>
  <Mask></Mask>
  <TipText></TipText>
  <TextAlign></TextAlign>
  <Text></Text>
  <ScrollBars></ScrollBars>  
</MyObject>
```

## Описание TextBox <a href="#description" id="description"></a>

```xml
<MyObject Name="TextBoxName" Type="TextBox" Assembly="BaseControls">
  <!--Тэги, общие для всех графических объектов-->
  <!--Тэги, специфичные для TextBox-->
</MyObject>
```

Значением TextBox считается текст, указанный в поле.

### Получение значения <a href="#get-value" id="get-value"></a>

Для получения указанного в поле текста используется get-проперти [Text](textbox.md#get_text):

```xml
<Object Name="TextBoxName">
  <Property Name="Text" />
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="TextBoxName" />
```

### Задание значения <a href="#set-value" id="set-value"></a>

Для задания значения текстовому полю используется set-проперти [Text](textbox.md#set_text):

```xml
<Object Name="TextBoxName">
  <Property Name="Text">Текст</Property>
</Object>
```

Рекомендуется использовать сокращенный вариант записи:

```xml
<Object Name="TextBoxName">Текст</Object>
```

## Тэги, специфичные для TextBox <a href="#specific-tags" id="specific-tags"></a>

### MaxLength <a href="#max_length" id="max_length"></a>

Задает максимальное число символов, которое разрешается вводить или вставлять в текстовое поле.

Необязательный тэг. Ожидается положительное целочисленное значение.

По умолчанию используется значение 0, показывающее, что ограничения нет.

```xml
<MaxLength>0</MaxLength>
```

### ReadOnly <a href="#read_only" id="read_only"></a>

Указывает, доступно ли текстовое поле только для чтения или для чтения и редактирования.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<ReadOnly>False</ReadOnly>
```

### Multiline

Задает значение, показывающее, является ли данный элемент управления многострочным текстовым полем.\
Игнорируется при наличии тэга [`<Mask>`](textbox.md#mask).

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Multiline>False</Multiline>
```

### Password

Признак, разрешающий ввод пароля.\
Пользователь увидит только символы звездочек ( \* ). Игнорируется при наличии тэга [`<Mask>`](textbox.md#mask).

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<Password>False</Password>
```

### ShowPasswordButton <a href="#show_password_button" id="show_password_button"></a>

Признак, определяющий, будет ли показана кнопка просмотра введенных символов.\
Игнорируется, если тэг `<Password>` отсутствует.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

<pre class="language-xml"><code class="lang-xml"><strong>&#x3C;ShowPasswordButton>True&#x3C;/ShowPasswordButton>
</strong></code></pre>

Если в тэге `<Password>` явно задано значение False, а в тэге `<ShowPasswordButton>` стоит значение True, то текстовое поле будет работать в режиме ввода пароля с отображением введенных символов.

### AllowedSymbols <a href="#allowed_symbols" id="allowed_symbols"></a>

Задает набор символов, которые разрешено вводить в поле.\
Пустая строка соответствует запрету вводить вообще какие-либо символы.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг отсутствует, то можно вводить любые символы.

```xml
<AllowedSymbols>0123456789</AllowedSymbols>
```

### InputLanguage <a href="#input_language" id="input_language"></a>

Задает ограничение на язык вводимых символов.\
Если язык вводимого символа не совпадает с языком, указанным в данном тэге, то этот символ будет трансформирован в символ другого языка, расположенный на этой же клавише клавиатуры.

Необязательный тэг. Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="234.41687935952444" align="center"></th><th width="415.40287769784175"></th></tr></thead><tbody><tr><td align="center">Rus</td><td>Русский язык</td></tr><tr><td align="center">Eng</td><td>Английский язык</td></tr><tr><td align="center">None</td><td>Без ограничений по языку</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<InputLanguage>None</InputLanguage>
```

Например, при значении Rus вводимая последовательность символов "qwerty" будет преобразована в "йцукен".

### InputCase <a href="#input_case" id="input_case"></a>

Задает ограничение на регистр вводимых символов.\
Если регистр вводимого символа не совпадает с регистром, указанном в данном тэге, то этот символ будет трансформирован в указанный регистр.

Необязательный тэг. Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="238.67352271687434" align="center"></th><th width="430.0593141797961"></th></tr></thead><tbody><tr><td align="center">Upper</td><td>Верхний регистр</td></tr><tr><td align="center">Lower</td><td>Нижний регистр</td></tr><tr><td align="center">None</td><td>Без ограничений по регистру</td></tr></tbody></table>

По умолчанию используется значение None.

```xml
<InputCase>None</InputCase>
```

### SelectOnEnter <a href="#select_on_enter" id="select_on_enter"></a>

Признак, определяющий, будет ли выделено содержимое поля после получения им фокуса.

Необязательный тэг. Ожидается логическое значение.

По умолчанию используется значение False.

```xml
<SelectOnEnter>False</SelectOnEnter>
```

### Mask

Маска ввода текстового поля.\
При наличии тэга `<Mask>` поля [`<Multiline>`](textbox.md#multiline), [`<Password>`](textbox.md#password) и [`<TextAlign>`](textbox.md#text_align) объекта игнорируются.\
Если тэг `<Mask>` отсутствует, то маска ввода не используется и не сможет в дальнейшем быть установлена.

Пустая строка соответствует отсутствию маски, при этом поля [`<Multiline>`](textbox.md#multiline), [`<Password>`](textbox.md#password) и [`<TextAlign>`](textbox.md#text_align) объекта по-прежнему игнорируются.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Mask>AA-00</Mask>
```

Все поддерживаемые элементы в выражении для задания маски ввода смотрите по [ссылке](https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.maskedtextbox.mask?redirectedfrom=MSDN\&view=windowsdesktop-6.0#remarks).

Для задания маски номера телефона используется служебное слово `PHONE`, которое переключает текстовое поле в режим ввода номера телефона. При этом маска выбирается автоматически на основе зоны и кода страны. Подробнее по ссылкам [здесь](https://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BB%D0%B5%D1%84%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5_%D0%BA%D0%BE%D0%B4%D1%8B_%D1%81%D1%82%D1%80%D0%B0%D0%BD) и [здесь](https://ru.wikipedia.org/wiki/%D0%A2%D0%B5%D0%BB%D0%B5%D1%84%D0%BE%D0%BD%D0%BD%D1%8B%D0%B5_%D0%BF%D0%BB%D0%B0%D0%BD%D1%8B_%D0%BD%D1%83%D0%BC%D0%B5%D1%80%D0%B0%D1%86%D0%B8%D0%B8_%D0%B2_%D1%80%D0%B0%D0%B7%D0%BD%D1%8B%D1%85_%D1%81%D1%82%D1%80%D0%B0%D0%BD%D0%B0%D1%85).

```xml
<Mask>PHONE</Mask>
```

### TipText <a href="#tip_text" id="tip_text"></a>

Задает текст-заполнитель, который будет отображаться в поле, если оно не имеет фокуса и его значение NULL.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<TipText>Текст подсказки</TipText>
```

### TextAlign <a href="#text_align" id="text_align"></a>

Используется, чтобы указать способ выравнивания текста по горизонтали.\
Игнорируется при наличии тэга [`<Mask>`](textbox.md#mask).

Необязательный тэг.  Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="198.926508301592" align="center"></th><th width="355.0302460949434"></th></tr></thead><tbody><tr><td align="center">Left</td><td>Слева</td></tr><tr><td align="center">Center</td><td>По центру</td></tr><tr><td align="center">Right</td><td>Справа</td></tr></tbody></table>

По умолчанию используется значение Left.

```xml
<TextAlign>Left</TextAlign>
```

### Text

Задает значение текстового поля.

Необязательный тэг. Любое значение будет переведено в текстовое.

По умолчанию используется пустая строка.

```xml
<Text>Текст</Text>
```

### ScrollBars <a href="#scroll_bars" id="scroll_bars"></a>

Тип полос прокрутки, показывающий, какие полосы прокрутки должны присутствовать в многострочном поле.\
Используется при установленном тэге [`<Multiline>`](textbox.md#multiline).

Необязательный тэг. Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="199.42423557019467" align="center"></th><th width="353.07623138059114"></th></tr></thead><tbody><tr><td align="center">Vertical</td><td>Вертикальная полоса прокрутки</td></tr><tr><td align="center">Horizontal</td><td>Горизонтальная полоса прокрутки</td></tr><tr><td align="center">Both</td><td>Вертикальная и горизонтальная полосы прокрутки</td></tr><tr><td align="center">None</td><td>Без полос прокрутки</td></tr></tbody></table>

По умолчанию используется значение Vertical.

```xml
<ScrollBars>Vertical</ScrollBars>
```

### BorderStyle <a href="#border_style" id="border_style"></a>

Задает тип границы элемента.

Необязательный тэг. Ожидается одно из допустимых значений:

<table data-header-hidden><thead><tr><th width="199.42423557019467" align="center"></th><th width="353.07623138059114"></th></tr></thead><tbody><tr><td align="center">FixedSingle</td><td>Одиночная плоская граница</td></tr><tr><td align="center">Fixed3D</td><td>Одиночная объемная граница</td></tr><tr><td align="center">None</td><td>Нет границы</td></tr></tbody></table>

По умолчанию используется значение FixedSingle.

```xml
<BorderStyle>Fixed3D</BorderStyle>
```

## Get-проперти для получения свойств <a href="#get-properties" id="get-properties"></a>

### MaxLength <a href="#get_max_length" id="get_max_length"></a>

Возвращает максимальное число символов, которое разрешается вводить или вставлять в текстовое поле.

```xml
<Object Name="TextBoxName">
  <Property Name="MaxLength" />
</Object>
```

### ReadOnly <a href="#get_read_only" id="get_read_only"></a>

Возвращает значение, определяющее, доступно ли текстовое поле только для чтения или для чтения и редактирования.

```xml
<Object Name="TextBoxName">
  <Property Name="ReadOnly" />
</Object>
```

### Multiline <a href="#get_multiline" id="get_multiline"></a>

Возвращает значение, показывающее, является ли данный элемент управления многострочным текстовым полем.

```xml
<Object Name="TextBoxName">
  <Property Name="Multiline" />
</Object>
```

### Password <a href="#get_password" id="get_password"></a>

Возвращает значение признака ввода пароля в поле.

```xml
<Object Name="TextBoxName">
  <Property Name="Password" />
</Object>
```

### AllowedSymbols <a href="#get_allowed_symbols" id="get_allowed_symbols"></a>

Возвращает набор символов, которые разрешено вводить в поле.

```xml
<Object Name="TextBoxName">
  <Property Name="AllowedSymbols" />
</Object>
```

### InputLanguage <a href="#get_input_language" id="get_input_language"></a>

Возвращает название языка, к которому будут преобразовываться вводимые символы.

```xml
<Object Name="TextBoxName">
  <Property Name="InputLanguage" />
</Object>
```

### InputCase <a href="#get_input_case" id="get_input_case"></a>

Возвращает название регистра, к которому будут преобразовываться вводимые символы.

```xml
<Object Name="TextBoxName">
  <Property Name="InputCase" />
</Object>
```

### SelectOnEnter <a href="#get_select_on_enter" id="get_select_on_enter"></a>

Возвращает значение признака, определяющего, будет ли выделено содержимое поля после получения им фокуса.

```xml
<Object Name="TextBoxName">
  <Property Name="SelectOnEnter" />
</Object>
```

### Mask <a href="#get_mask" id="get_mask"></a>

Возвращает маску ввода текстового поля.

```xml
<Object Name="TextBoxName">
  <Property Name="Mask" />
</Object>
```

### TipText <a href="#get_tip_text" id="get_tip_text"></a>

Возвращает текст-заполнитель, который будет отображаться в поле, если оно не имеет фокуса и его значение NULL.

```xml
<Object Name="TextBoxName">
  <Property Name="TipText" />
</Object>
```

### TextAlign <a href="#get_text_align" id="get_text_align"></a>

Возвращает способ выравнивания текста по горизонтали.

```xml
<Object Name="TextBoxName">
  <Property Name="TextAlign" />
</Object>
```

### Text <a href="#get_text" id="get_text"></a>

Возвращает значение текстового поля.

```xml
<Object Name="TextBoxName">
  <Property Name="Text" />
</Object>
```

### MaskCompleted <a href="#mask_completed" id="mask_completed"></a>

Возвращает значение, показывающее, все ли обязательные входные данные введены в маску ввода.

```markup
<Object Name="TextBoxName">
  <Property Name="MaskCompleted" />
</Object>
```

#### Пример

Если у текстового поля задана маска вида:

```xml
<Mask>0000#?</Mask>
```

* 0 - обязательный символ, принимает любую цифру от 0 до 9;
* \\# - необязательный символ, принимает любую цифру от 0 до 9 или пробел. Допускаются знаки плюс (+) и минус (-);
* ? - необязательный символ, принимает буквы таблицы ASCII.

Если в поле будут введены все обязательные цифры, то get-проперти MaskCompleted вернет значение true. Если будет отсутствовать хотя бы одна обязательная цифра, то будет возвращено значение false.

### MaskFull <a href="#mask_full" id="mask_full"></a>

Возвращает значение, показывающее, все ли обязательные и необязательные входные данные были введены в маску ввода.

```markup
<Object Name="TextBoxName">
  <Property Name="MaskFull" />
</Object>
```

#### Пример

Если у текстового поля задана маска вида:

```xml
<Mask>0000#?</Mask>
```

Если в поле будет введена строка вида "1234-A", то get-проперти MaskFull вернет значение true. Если будет отсутствовать хотя бы один любой символ, то будет возвращено значение false.

### WordByNumber <a href="#word_by_number" id="word_by_number"></a>

Возвращает целое слово с указанным порядковым номером, извлеченное из значения поля.\
Символами-разделителями между словами считаются " ", ",", ".", ";".

Ожидается целочисленное положительное значение.

```xml
<Object Name="TextBoxName">
  <Property Name="WordByNumber">1</Property>
</Object>
```

Например, для строки "слово1 слово2" свойство со значением 2 вернет "слово2".

### Length

Возвращает длину текста, введенного в поле.

```xml
<Object Name="TextBoxName">
  <Property Name="Length" />
</Object>
```

### ScrollBars <a href="#get_scroll_bars" id="get_scroll_bars"></a>

Возвращает тип полос прокрутки, показывающий, какие полосы прокрутки должны присутствовать в многострочном поле.

```xml
<Object Name="TextBoxName">
  <Property Name="ScrollBars" />
</Object>
```

### BorderStyle <a href="#get_border_style" id="get_border_style"></a>

Возвращает тип границы элемента.

```xml
<Object Name="TextBoxName">
  <Property Name="BorderStyle" />
</Object>
```

## Set-проперти для динамического задания свойств <a href="#set-properties" id="set-properties"></a>

### MaxLength <a href="#set_max_length" id="set_max_length"></a>

Задает максимальное число символов, которое разрешается вводить или вставлять в текстовое поле.

Ожидается положительное целочисленное значение.

```xml
<Object Name="TextBoxName">
  <Property Name="MaxLength">200</Property>
</Object>
```

### ReadOnly <a href="#set_read_only" id="set_read_only"></a>

Задает значение, определяющее, доступно ли поле только для чтения или для чтения и редактирования.

Ожидается логическое значение.

```xml
<Object Name="TextBoxName">
  <Property Name="ReadOnly">True</Property>
</Object>
```

### Multiline <a href="#set_multiline" id="set_multiline"></a>

Задает значение, показывающее, является ли данный элемент управления многострочным текстовым полем.\
Если тэг [`<Mask>`](textbox.md#mask) присутствует в описании объекта, то любое переданное значение игнорируется.

Ожидается логическое значение.

```xml
<Object Name="TextBoxName">
  <Property Name="Multiline">True</Property>
</Object>
```

### Password <a href="#set_password" id="set_password"></a>

Задает значение признака ввода пароля в поле.\
Если тэг [`<Mask>`](textbox.md#mask) присутствует в описании объекта, то любое переданное значение игнорируется.

Ожидается логическое значение.

```xml
<Object Name="TextBoxName">
  <Property Name="Password">True</Property>
</Object>
```

### AllowedSymbols <a href="#set_allowed_symbols" id="set_allowed_symbols"></a>

Задает набор символов, которые разрешено вводить в поле.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TextBoxName">
  <Property Name="AllowedSymbols">0123,.</Property>
</Object>
```

### InputLanguage <a href="#set_input_language" id="set_input_language"></a>

Задает правила трансформации языка вводимых символов.

Ожидается одно из допустимых значений, указанных в описании тэга [`<InputLanguage>`](textbox.md#input_language).

```xml
<Object Name="TextBoxName">
  <Property Name="InputLanguage">Rus</Property>
</Object>
```

### InputCase <a href="#set_input_case" id="set_input_case"></a>

Задает название языка, к которому будут преобразовываться вводимые символы.

Ожидается одно из допустимых значений, указанных в описании тэга [`<InputCase>`](textbox.md#input_case).

```xml
<Object Name="TextBoxName">
  <Property Name="InputCase">Lower</Property>
</Object>
```

### SelectOnEnter <a href="#set_select_on_enter" id="set_select_on_enter"></a>

Задает значение признака, определяющего, будет ли выделено содержимое поля после получения им фокуса.

Ожидается логическое значение.

```xml
<Object Name="TextBoxName">
  <Property Name="SelectOnEnter">True</Property>
</Object>
```

### Mask <a href="#set_mask" id="set_mask"></a>

Задает маску ввода текстового поля.\
Если тэг [`<Mask>`](textbox.md#mask) отсутствует в описании объекта, то маска не будет установлена.

Любое значение будет переведено в текстовое. Полные правила указания маски ввода указаны в описании тэга [`<Mask>`](textbox.md#mask).

```xml
<Object Name="TextBoxName">
  <Property Name="Mask">###.##</Property>
</Object>
```

### TipText <a href="#set_tip_text" id="set_tip_text"></a>

Задает текст-заполнитель, который будет отображаться в поле, если оно не имеет фокуса и его значение NULL.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TextBoxName">
  <Property Name="TipText">Текст</Property>
</Object>
```

### TextAlign <a href="#set_text_align" id="set_text_align"></a>

Задает способ выравнивания текста по горизонтали.\
Если тэг [`<Mask>`](textbox.md#mask) присутствует в описании объекта, то любое переданное значение игнорируется.

Ожидается одно из допустимых значений, указанных в описании тэга [`<TextAlign>`](textbox.md#text_align).

```xml
<Object Name="LabelName">
  <Property Name="TextAlign">Right</Property>
</Object>
```

### Text <a href="#set_text" id="set_text"></a>

Задает значение текстового поля.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TextBoxName">
  <Property Name="Text">Текст</Property>
</Object>
```

### AppendText <a href="#append_text" id="append_text"></a>

Дописывает поле заданным текстом и переводит курсор в конец поля.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TextBoxName">
  <Property Name="AppendText">Текст</Property>
</Object>
```

### InsertAtCursorPosition

Вставляет заданный текст на место курсора и после переводит курсор в конец добавленного текста.\
Если поле не содержит фокуса, то тогда вставляемый текст добавляется в конец строки, и поле получает фокус.

Любое значение будет переведено в текстовое.

```xml
<Object Name="TextBoxName">
  <Property Name="InsertAtCursorPosition">Текст</Property>
</Object>
```

### ScrollBars <a href="#set_scroll_bars" id="set_scroll_bars"></a>

Задает тип полос прокрутки, показывающий, какие полосы прокрутки должны присутствовать в многострочном поле.\
Используется при установленном тэге [`<Multiline>`](textbox.md#multiline).

Ожидается одно из допустимых значений, указанных в описании тэга [`<ScrollBars>`](textbox.md#scroll_bars).

```xml
<Object Name="TextBoxName">
  <Property Name="ScrollBars">Horizontal</Property>
</Object>
```

### ScrollToEnd

Прокручивает содержимое поля до вертикальных и горизонтальных конечных точек полос прокрутки.

Значение не ожидается.

```xml
<Object Name="TextBoxName">
  <Property Name="ScrollToEnd"/>
</Object>
```

### BorderStyle <a href="#set_border_style" id="set_border_style"></a>

Задает тип границы элемента.

Ожидается одно из допустимых значений, указанных в описании тэга [`<BorderStyle>`](textbox.md#border_style).

```xml
<Object Name="TextBoxName">
  <Property Name="BorderStyle">Fixed3D</Property>
</Object>
```
