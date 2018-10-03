---
title: FxCopCmd-Fehler
ms.date: 10/19/2016
ms.prod: visual-studio-dev14
ms.technology: vs-ide-code-analysis
ms.topic: reference
helpviewer_keywords:
- FxCopCmd errors
ms.author: gewarren
author: gewarren
manager: douge
ms.workload:
- multiple
ms.openlocfilehash: 71e2a39b792dcc5a01eb28611664736f6620bb1f
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2018
ms.locfileid: "47523126"
---
# <a name="fxcopcmd-tool-errors"></a>FxCopCmd-Tool-Fehler

FxCopCmd werden alle schwerwiegenden Fehler nicht berücksichtigt. Wenn FxCopCmd genügend Informationen zum Ausführen einer partiellen Analysis hat, führt es die Analyse- und Berichten aufgetretenen. Der Fehlercode, der eine 32-Bit-Ganzzahl ist, enthält eine bitweise Kombination von numerischen Werten, die Fehlern entsprechen.

Die folgende Tabelle beschreibt die Fehlercodes von FxCopCmd zurückgegeben:

|Fehler|Numerischer Wert|
|-----------|-------------------|
|Keine Fehler|0x0|
|Analysefehler.|0x1|
|Ausnahmen von Netzwerkregeln|0x2|
|Fehler beim Laden des Projekts|0 x 4|
|Fehler beim Laden der Assembly|0x8|
|Fehler beim Laden von Regel-Bibliothek|0x10|
|Fehler beim Laden von Import-Bericht|0x20|
|Ausgabefehler|0 x 40|
|Befehlszeilenfehler switch|0x80|
|Initialisierungsfehler|0 x 100|
|Assembly-Verweise-Fehler|0 x 200|
|BuildBreakingMessage|0 x 400|
|Unbekannter Fehler|0x1000000|

**Analysefehler** für schwerwiegende Fehler zurückgegeben wird. Er gibt an, dass die Analyse nicht abgeschlossen werden konnte. Der Fehlercode enthält ggf. auch die zugrunde liegende Ursache des schwerwiegenden Fehlers. Die folgenden Bedingungen schwerwiegende Fehler zu generieren:

- Die Analyse konnte aufgrund unzureichender Eingabe nicht ausgeführt werden.

- Die Analyse ausgelöst hat, eine Ausnahme, die nicht von FxCopCmd behandelt wird.

- Die angegebene Projektdatei wurde nicht gefunden oder ist beschädigt.

- Die Output-Option wurde nicht angegeben oder die Datei konnte nicht geschrieben werden.

> [!NOTE]
> Die FxCopCmd Rückgabecode **Assemblyverweise Fehler** 0 x 200 allein ist eher eine Warnung als Fehler. Dieser Rückgabecode gibt an, dass, die es indirekte Verweise fehlen jedoch, dass FxCopCmd sie verarbeiten können. Die Warnung bedeutet, dass es besteht die Möglichkeit, dass einige Analyseergebnisse gefährdet sein könnte. Behandeln **Assemblyverweise Fehler** als einen Fehler, wenn es mit einem anderen Rückgabecode kombiniert wird.

## <a name="see-also"></a>Siehe auch

- [Anwendungsfehler bei der Codeanalyse](../code-quality/code-analysis-application-errors.md)