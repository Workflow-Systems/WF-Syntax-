---
description: Команда; отправляет e-mail.
---

# EmailSendCommand

## Шаблон EmailSendCommand <a href="#template_email_send_command" id="template_email_send_command"></a>

```xml
<Command Name="" Type="EmailSendCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для EmailSendCommand-->
  <Async Value="" />
  <AuthorSmtpServerAddress></AuthorSmtpServerAddress>
  <AuthorSmtpServerPort></AuthorSmtpServerPort>
  <AuthorEmailAddress></AuthorEmailAddress>
  <AuthorEmailPassword></AuthorEmailPassword>
  <AuthorName></AuthorName>
  <Timeout></Timeout>
  <BlindCarbonCopy></BlindCarbonCopy>
  <EnableSSL></EnableSSL>
  <Subject></Subject>
  <Text></Text>
  <InlineFiles></InlineFiles>
  <Files></Files>
  <Addressees></Addressees>
</Command>
```

## Описание EmailSendCommand <a href="#description_email_send_command" id="description_email_send_command"></a>

```xml
<Command Name="EmailSendCommandName" Type="EmailSendCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для EmailSendCommand-->
</Command>
```

### Результат выполнения EmailSendCommand <a href="#result_email_send_command" id="result_email_send_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Результат успешной отправки в виде 0.

## Тэги, специфичные для EmailSendCommand <a href="#tags_email_send_command" id="tags_email_send_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга `<Async>`: не ожидается.

Если тэг `<Async>` отсутствует, то для атрибута `Value` используется значение False.

```xml
<Async Value="False" />
```

#### Атрибуты тэга `<Async>` <a href="#attributes_tag_async" id="attributes_tag_async"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="476.3333333333333"></th></tr></thead><tbody><tr><td align="center">Value</td><td><p>Значение.</p><p></p><p>Обязательный атрибут. Ожидается логическое значение.</p></td></tr></tbody></table>

### AuthorSmtpServerAddress <a href="#author_smtp_server_address" id="author_smtp_server_address"></a>

Адрес SMTP-сервера почтового ящика отправителя.

Обязательный тэг. Любое значение будет переведено в текстовое.

```xml
<AuthorSmtpServerAddress>smtp.yandex.ru</AuthorSmtpServerAddress>
```

### AuthorSmtpServerPort <a href="#author_smtp_server_port" id="author_smtp_server_port"></a>

Порт SMTP-сервера почтового ящика отправителя.

Обязательный тэг. Ожидается целочисленное значение.

```xml
<AuthorSmtpServerPort>25</AuthorSmtpServerPort>
```

### AuthorEmailAddress <a href="#author_email_address" id="author_email_address"></a>

Ящик отправителя.

Обязательный тэг. Любое значение будет переведено в текстовое.

```xml
<AuthorEmailAddress>sender@mail.com</AuthorEmailAddress>
```

### AuthorEmailPassword <a href="#author_email_password" id="author_email_password"></a>

Пароль от ящика отправителя.

Обязательный тэг. Любое значение будет переведено в текстовое.

```xml
<AuthorEmailPassword>password</AuthorEmailPassword>
```

### Timeout <a href="#timeout" id="timeout"></a>

Предельный интервал ожидания отправки письма (в миллисекундах).

Необязательный тэг. Ожидается положительное целочисленное значение.

Если тэг `<Timeout>` отсутствует, то ограничение отсутствует.

```xml
<Timeout>100000</Timeout>
```

### BlindCarbonCopy <a href="#blind_carbon_copy" id="blind_carbon_copy"></a>

Список адресатов, для которых письма будут отправлены слепой копией.

Необязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<BlindCarbonCopy>addressee@mail.com</BlindCarbonCopy>
```

### EnableSSL <a href="#enable_ssl" id="enable_ssl"></a>

Признак, определяющий, будет ли применено SSL-шифрование при отправке писем.

Необязательный тэг. Ожидается логическое значение.

Если тэг `<EnableSSL>` отсутствует, то используется значение True.

```xml
<EnableSSL>True</EnableSSL>
```

### AuthorName <a href="#author_name" id="author_name"></a>

Заголовок имени отправителя.

Необязательный тэг. Любое значение будет переведено в текстовое.

Если тэг `<AuthorName>` отсутствует, то используется значение из тэга [`<AuthorEmailAddress>`](email_send_command.md#author_email_address).

```xml
<AuthorName>Name</AuthorName>
```

### Subject <a href="#subject" id="subject"></a>

Тема письма.

Необязательный тэг. Любое значение будет переведено в текстовое.

```xml
<Subject>Subject</Subject>
```

### Text <a href="#text" id="text"></a>

Содержание письма.

Необязательный тэг. Любое значение будет переведено в текстовое.

Текст поддерживает переменные типа "{1}", "{2}" и т.д., заменяемые в теле письма изображениями, содержащимися в файлах, указанных в тэге [`<InlineFiles>`](email_send_command.md#inline_files), в том порядке, в котором они указаны.

```xml
<Text>Text</Text>
```

### InlineFiles <a href="#inline_files" id="inline_files"></a>

Файлы, отображаемые в тексте письма.

Необязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<InlineFiles>file.png</InlineFiles>
```

### Files <a href="#files" id="files"></a>

Файлы, прикрепляющиеся к письму.

Необязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<Files>file.ext</Files>
```

### Addressees <a href="#addressees" id="addressees"></a>

Список адресатов, кому будет отправлено письмо.

Обязательный тэг. Любое значение будет переведено в массив текстовых значений.

```xml
<Addressees>addressee@mail.com</Addressees>
```
