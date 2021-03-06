---
title: 'DA0024: Übermäßige GC-CPU-Zeit | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- vs.performance.DA0024
- vs.performance.24
- vs.performance.rules.DA0024
ms.assetid: 228872da-77d0-4da5-b455-ac57fb1867c9
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: vs-2017
ms.workload:
- multiple
ms.openlocfilehash: 20736e7af905bbbc72c1c2bec1e5b79d68259217
ms.sourcegitcommit: b885f26e015d03eafe7c885040644a52bb071fae
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2020
ms.locfileid: "85544650"
---
# <a name="da0024-excessive-gc-cpu-time"></a>DA0024: Übermäßige GC-CPU-Zeit

|Element|Wert|
|-|-|
|Regel-ID|DA0024|
|Kategorie|.NET Framework-Verwendung|
|Profilerstellungsmethode|Alle|
|Meldung|Die GC-Zeitdauer in Prozent ist sehr hoch. Ein hohes Maß an Mehraufwand für die Garbage Collection wurde festgestellt.|
|Regeltyp|Warnung|

 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 10 Samplings erfasst werden, damit diese Regel ausgelöst wird.

## <a name="cause"></a>Ursache
 Die bei der Profilerstellung erfassten Systemleistungsdaten deuten darauf hin, dass für die Garbage Collection im Vergleich zur gesamten Anwendungsverarbeitung übermäßig viel Zeit aufgewendet wird.

## <a name="rule-description"></a>Regelbeschreibung
 Die Microsoft .NET-CLR (Common Language Runtime) verfügt über einen automatischen Speicherverwaltungsmechanismus, durch den der Speicher von Objekten, die von der Anwendung nicht mehr verwendet werden, mithilfe eines Garbage Collectors freigegeben wird. Der Garbage Collector ist generationsorientiert, da angenommen wird, dass viele Speicherbelegungen kurzlebig sind. Lokale Variablen müssen beispielsweise kurzlebig sein. Neu erstellte Objekte beginnen in Generation 0 (gen 0) und werden zu Generation 1, wenn sie nach einer Ausführung der Garbage Collection noch vorhanden sind, und schließlich zu Generation 2, wenn sie von der Anwendung auch weiterhin verwendet werden.

 Objekte in der Generation 0 werden häufig und i. d. R. äußerst effizient gesammelt. Objekte in der Generation 1 werden nicht so häufig und weniger effizient gesammelt. Und langlebige Objekte in der Generation 2 werden schließlich noch seltener gesammelt. Die Collection der Generation 2, bei der es sich um eine vollständige Ausführung der Garbage Collection handelt, ist zudem der aufwändigste Vorgang.

 Diese Regel wird ausgelöst, wenn für die Garbage Collection im Vergleich zur gesamten Anwendungsverarbeitung übermäßig viel Zeit aufgewendet wird.

> [!NOTE]
> Wenn für die Garbage Collection im Vergleich zur gesamten Anwendungsverarbeitung viel, jedoch nicht übermäßig viel Zeit aufgewendet wird, wird anstelle dieser Regel die Warnung [DA0023: Hohe GC-CPU-Zeit](../profiling/da0023-high-gc-cpu-time.md) ausgelöst.

## <a name="how-to-investigate-a-warning"></a>Vorgehensweise zur Überprüfung einer Warnung
 Doppelklicken Sie auf die Meldung im Fenster „Fehlerliste“, um zur Ansicht [Markierungen](../profiling/marks-view.md) der Profilerstellungsdaten zu navigieren. Suchen Sie die Spalte **.NET CLR-Speicher\\GC-Zeitdauer in Prozent**. Überprüfen Sie, ob der Mehraufwand für die Garbage Collection bei verwaltetem Speicher in bestimmten Phasen der Programmausführung besonders häufig auftritt. Vergleichen Sie die Werte der Spalte „GC-Zeitdauer in Prozent“ mit der Garbage Collection-Rate aus den Spalten **Auflistungsanzahl der Generation 0**, **Auflistungsanzahl der Generation 1** und **Auflistungsanzahl der Generation 2**.

 Die Werte der Spalte „GC-Zeitdauer in Prozent“ geben an, wie viel Zeit von einer Anwendung für die Garbage Collection im Vergleich zur Gesamtverarbeitungszeit aufgewendet wird. In einigen Situationen kann der Wert für die GC-Zeitdauer in Prozent hoch sein, ohne dass dies auf eine übermäßige Garbage Collection zurückzuführen ist. Weitere Informationen zur Berechnung des Werts für die GC-Zeitdauer in Prozent finden Sie im Beitrag [Difference Between Perf Data Reported by Different Tools – 4 (Unterschied zwischen Leistungsdaten unterschiedlicher Tools – 4)](https://devblogs.microsoft.com/maoni/archive/difference-between-perf-data-reported-by-different-tools-4.aspx) in **Maoni‘s Weblog** auf MSDN. Treten Seitenfehler auf oder wird die Anwendung aufgrund von Aufgaben mit höherer Priorität auf dem Computer vorzeitig entfernt, werden diese zusätzlichen Verzögerungen bei der Berechnung des Werts für die GC-Zeitdauer in Prozent berücksichtigt.
