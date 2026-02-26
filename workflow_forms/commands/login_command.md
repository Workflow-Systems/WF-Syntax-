---
description: >-
  Команда; авторизует пользователя на веб-сервисе под определенным именем
  (олицетворение).
---

# LoginCommand

## Шаблон LoginCommand <a href="#template_login_command" id="template_login_command"></a>

```xml
<Command Name="" Type="LoginCommand" Assembly="Commands">>
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для LoginCommand-->
  <UserName></UserName>
  <UserDomain></UserDomain>
  <Password></Password>
</Command>
```

## Описание LoginCommand <a href="#description_login_command" id="description_login_command"></a>

```xml
<Command Name="LoginCommandName" Type="LoginCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для LoginCommand-->
</Command>
```

### Результат выполнения LoginCommand <a href="#result_login_command" id="result_login_command"></a>

#### Value <a href="#result_value" id="result_value"></a>

Если авторизация пройдена успешно, то результатом выполнения команды будет **Ok**, в случае ошибки будет значение **Fail**.

## Тэги, специфичные для LoginCommand <a href="#tags_login_command" id="tags_login_command"></a>

### UserName <a href="#user_name" id="user_name"></a>

Системное имя пользователя.

Обязательный тэг. Любое значение преобразуется в текстовое.

```xml
<UserName>False</UserName>
```

### UserDomain <a href="#user_domain" id="user_domain"></a>

Домен пользователя.

Обязательный тэг. Любое значение преобразуется в текстовое.

```xml
<UserDomain>False</UserDomain>
```

### Password <a href="#password" id="password"></a>

Пароль пользователя.

Обязательный тэг. Любое значение преобразуется в текстовое.

```xml
<Password>False</Password>
```
