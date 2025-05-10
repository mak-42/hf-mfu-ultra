# The script provides functionality for writing Mifare Ultralight Ultra/UL-5 tags via Proxmark3

## Language
# [English](#overview)
# [Русский](#описание)

## Overview
The script provides two operations with [Ultra](https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/magic_cards_notes.md#ultra-ru)/[UL-5](https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/magic_cards_notes.md#ul-5) tags:
1. Restore (write) dump to tag.
2. Wipe tag.

## Restore dump to tag
The operation enables writing a previously saved dump to tag.

Usage:
```
script run hf_mfu_ultra -k <passwd> -r <dump filename>
```

Example:
```
script run hf_mfu_ultra -key ffffffff -r hf-mfu-3476FF1514D866-dump.bin
```

## Wipe tag
The operation enables clearing previously written Ultra tag (excluding the UUID). Use it to prepare tag for restoring another dump.

[!WARNING]
Do not use this operation with UL-5 tags.

Usage:
```
script run hf_mfu_ultra -k <passwd> -w
```

Example:
```
script run hf_mfu_ultra -k 1d237f76 -w
```

## Описание
Скрипт реалиует 2 операции с метками [Ultra](https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/magic_cards_notes.md#ultra-ru)/[UL-5](https://github.com/RfidResearchGroup/proxmark3/blob/master/doc/magic_cards_notes.md#ul-5):
1. Восстановление (запись) метки из дампа.
2. Стирание данных метки.

## Восстановление метки из дампа
Операция позволяет записать на метку дамп, сохранённый в файл ранее.

Использование:
```
script run hf_mfu_ultra -k <passwd> -r <dump filename>
```

Пример:
```
script run hf_mfu_ultra -k ffffffff -r hf-mfu-3476FF1514D866-dump.bin
```

## Очистка метки
Операция позволяет стереть с метки Ultra все ранее записанные данные (кроме UUID). Используйте операцию для подготовки метки к восстановления метки из другого дампа.

[!WARNING]
Не выполняете эту операцию с метками UL-5.

Использование:
```
script run hf_mfu_ultra -k <passwd> -w
```

Пример:
```
script run hf_mfu_ultra -k 1d237f76 -w
```
