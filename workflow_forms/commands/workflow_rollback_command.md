---
description: >-
  Команда; откатывает состояние процесса (совокупность состояний шагов) к
  определенному состоянию.
---

# WorkflowRollbackCommand

## Шаблон WorkflowRollbackCommand <a href="#template_workflow_rollback_command" id="template_workflow_rollback_command"></a>

```xml
<Command Name="" Type="WorkflowRollbackCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для WorkflowRollbackCommand-->
  <Async Value="" />
  <Workflow Name="" />
  <WorkflowId></WorkflowId>
  <WorkflowStateId></WorkflowStateId>
</Command>
```

## Описание WorkflowRollbackCommand <a href="#description_workflow_rollback_command" id="description_workflow_rollback_command"></a>

```xml
<Command Name="WorkflowRollbackCommandName" Type="WorkflowRollbackCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для WorkflowRollbackCommand-->
</Command>
```

### Результат выполнения WorkflowRollbackCommand <a href="#result_workflow_rollback_command" id="result_workflow_rollback_command"></a>

Команда не имеет результата.

## Тэги, специфичные для WorkflowRollbackCommand <a href="#tags_workflow_rollback_command" id="tags_workflow_rollback_command"></a>

### Async <a href="#async" id="async"></a>

Признак, определяющий, будет ли выполнение команды происходить в асинхронном режиме (в фоновом потоке).

Необязательный тэг. Значение тэга не ожидается.\
Обязательный атрибут `Value` ожидает логическое значение

По умолчанию используется значение False.

```xml
<Async Value="False" />
```

### Workflow <a href="#workflow" id="workflow"></a>

Процесс, в рамках которого происходит действие с экземпляром.

Обязательный тэг. Значение тэга `<Workflow>`: не ожидается.

```xml
<Workflow Name="WorkflowName" />
```

#### Атрибуты тэга `<Workflow>` <a href="#attributes_tag_workflow" id="attributes_tag_workflow"></a>

<table data-header-hidden><thead><tr><th align="center"></th><th width="454.3333333333333"></th></tr></thead><tbody><tr><td align="center">Name</td><td><p>Название процесса.</p><p></p><p>Обязательный атрибут. Ожидается название одного из процессов, расположенных на сервере и заголовочно описанных в базе.</p></td></tr></tbody></table>

### WorkflowId <a href="#workflow_id" id="workflow_id"></a>

Идентификатор экземпляра процесса.

Обязательный тэг. Ожидается целочисленное значение.

```xml
<WorkflowId>1</WorkflowId>
```

### WorkflowStateId <a href="#workflow_state_id" id="workflow_state_id"></a>

Идентификатор состояния экземпляра процесса, к которому нужно откатиться.

Обязательный тэг. Ожидается целочисленное значение.

```xml
<WorkflowStateId>1</WorkflowStateId>
```
