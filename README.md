# assemblables.github.io
https://assemblables.github.io/

Описание проекта на русском языке.
Этот проект предоставляет бесплатный плагин для популярных сред разработки электроники 
(печатных плат): KiCad, Altium Designer и другие. А также хостинг сборочных чертежей.
Плагин генерирует QR-code, в виде компонента/футпринта на печатной плате.
В QR-code содержится ссылка на сборочный чертеж для печатной платы.
Плагин загуружает сборочный чертеж на assemblables.org и генерирует соответствующий QR-code для печатной платы.
Пользователь может выбрать какую информацию о своей печатной плате он хочет включить в QR-code. Это может быть:
- Сборочный чертеж для человека. Используется Interactive HTML BOM.
- Positioning file (Pos) для pick-and-place машин
- Список компонентов (BOM)
   - Есть функция выборочного скрытия имен компонентов из списка (BOM)
- Copper layers - позволяют упростить ремонт печатной платы.
- Silkscreen layers

Положение и размер самого QR-code на печатной также содержится по ссылке, что позволяет pick-and-place машинам использовать сам QR-code как стартовый маркер.

## Для кого предназначен проект

### Разработчики печатных плат
Assemblables code позволяет безошибочно понять какой именно версии печатная плата в ваших руках, что особенно важно при работе с несколькими ревизиями одной и той же платы.

Это может быть удобым стандартом общения между rnd-отделом и пайщиками.

### Ремонтники
Если вам в ремонт попало устройство с повреждениями на печатной плате, Assemblables code позволит узнать номиналы компонентов и даже понять как восстановить поврежденные дорожки (для этого рекомендуется включать Copper layers).

### Удобный интерфейс общения с pick-and-place машинами
С помощью Assemblables code pick-and-place машины могут стать однокнопочными! Нужно только положить печатную плату на рабочую поверхность, и машина сама увидит QR-code, скачает всю необходимую информацию и начнет процесс сборки.

### Ссылки
Для минимизации размера QR-code мы используем наш короткий домен: asmb.io
Ссылка в QR-code имеет вид `asmb.io/<unique_id>`
По умолчанию все ссылки проекта - unlisted. Это означает, что они не индексируются поисковыми системами и доступны только тем, кто имеет прямую ссылку.

## Text for landing page

### Assembly data that stays with the PCB

Assemblables is a free plugin for KiCad, Altium Designer, and other PCB design tools that creates QR-code with the assembly data for the PCB. Since that moment, the assembly data stays with the physical board itself.

Scanning the code opens the documentation for that specific board and revision.

The published package can include:
- an Interactive HTML BOM for manual assembly;
- pick-and-place position data for automated assembly;
- a bill of materials, with selected component names hidden when needed;
- copper layers for inspection and repair;
- silkscreen layers.

### For PCB engineers and assembly teams

The code provides a direct connection between a physical PCB and its assembly data. It helps engineers distinguish board revisions and gives R&D and assembly teams a shared reference without relying on filenames or separate document folders.

### For repair technicians

A technician can scan the board to check component values, placement, and available layer data. Including copper layers can also help trace and reconstruct damaged connections.

### For pick-and-place machines

Assemblables enables a pick-and-place machine to identify a board, retrieve its assembly data, and begin component placement without manual intervention.
The assembly data also includes the QR code's position and dimensions, allowing the machine to use it as an initial reference for board alignment.



### Links and access

QR codes use the short `asmb.io/<unique_id>` format to keep the printed code compact. Links are unlisted by default: search engines do not index them, and access requires the direct URL.
