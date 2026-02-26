---
description: Команда; проигрывает звук из указанного WAV-файла.
---

# SoundPlayCommand

## Шаблон SoundPlayCommand <a href="#template_sound_play_command" id="template_sound_play_command"></a>

```xml
<Command Name="" Type="SoundPlayCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <Condition Name="" />
  <Lock Value="" />
  <!--Тэги, специфичные для SoundPlayCommand-->
  <File></File>
</Command>
```

## Описание SoundPlayCommand <a href="#description_sound_play_command" id="description_sound_play_command"></a>

```xml
<Command Name="SoundPlayCommandName" Type="SoundPlayCommand" Assembly="Commands">
  <!--Тэги, общие для всех команд-->
  <!--Тэги, специфичные для SoundPlayCommand-->
</Command>
```

### Результат выполнения SoundPlayCommand <a href="#result_sound_play_command" id="result_sound_play_command"></a>

Команда не имеет результата.

## Тэги, специфичные для SoundPlayCommand <a href="#tags_sound_play_command" id="tags_sound_play_command"></a>

### File <a href="#file" id="file"></a>

Путь до проигрываемого файла.

Обязательный тэг. Любое значение будет переведено в текстовое.

Поддерживаются [константы замены](../values/replacement_constants.md).

```xml
<File>File.wav</File>
```
