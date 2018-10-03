---
title: 'DA0503: Durchschnittliche Arbeitsseite in Bytes für den Prozess, für den die Profilerstellung ausgeführt wird | Microsoft-Dokumentation'
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-debug
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- vs.performance.503
- vs.performance.DA0503
- vs.performance.rules.DA0503
ms.assetid: 9047a494-eaaf-4679-b422-c64e8bde77a4
caps.latest.revision: 13
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.openlocfilehash: e71d7e630505d44392610ab5ba94c19b3928f7f9
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2018
ms.locfileid: "47512830"
---
# <a name="da0503-average-working-set-in-bytes-for-the-process-being-profiled"></a>DA0503: Durchschnittliche Arbeitsseite in Bytes für den Prozess, für den die Profilerstellung ausgeführt wird
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

Die neueste Version dieses Themas finden Sie unter [DA0503: Durchschnittliche Arbeitsseite in Bytes für den Prozess, dessen Profil erstellt](https://docs.microsoft.com/visualstudio/profiling/da0503-average-working-set-in-bytes-for-the-process-being-profiled).  
  
Regel-Id | DA0503 |  
| Kategorie | Ressourcenüberwachung |  
| Profilerstellungsmethode | Alle |  
| Nachricht | Diese Informationen war nur zu Informationszwecken gesammelt. Vom Leistungsindikator für die Verarbeitung von Arbeitsseiten wird die Belegung des physischen Speichers durch den Prozess ermittelt, für den die Profilerstellung ausgeführt wird. Dem gemeldeten Wert handelt den berechneten Durchschnittswert aus allen Messintervallen. |  
| Regeltyp | Informationen |  
  
 Wenn Sie Profile mithilfe der Sampling-, .NET-Arbeitsspeicher- oder Ressourcenkonfliktmethode Profile erstellen, müssen mindestens 10 Samplings erfasst werden, damit diese Regel ausgelöst wird.  
  
## <a name="rule-description"></a>Regelbeschreibung  
 Diese Meldung gibt Aufschluss über die durchschnittliche Menge an physischem Speicher, die gerade von der Arbeitsseite verwendet wird (in Bytes). Die Prozessarbeitsseite stellt Seiten aus dem Prozessadressbereich dar, die sich gegenwärtig im physischen Speicher befinden.  
  
 Der gemeldete Wert enthält residente Seiten aus freigegebenen Arbeitsspeichersegmenten, auf die vom Prozess verwiesen wurde. In den berücksichtigten freigegebenen Arbeitsspeichersegmenten sind auch freigegebene DLLs enthalten, auf die vom Prozess verwiesen wird. Aufgrund von freigegebenen Arbeitsspeichersegmenten kann der Wert der Prozessarbeitsseite die Menge des virtuellen Arbeitsspeichers übersteigen, der vom Prozess belegt wird.  
  
 Bei dem gemeldeten Wert handelt es sich um den Durchschnittswert aller Messintervalle, in denen der Prozess, dessen Profil erstellt wird, aktiv war.  
  
 Die Größe der Prozessarbeitsseite spiegelt die Menge des virtuellen Arbeitsspeichers wider, die aktiv vom Prozess verwendet wird. Sie wird auch von der Menge an physischem Speicher (oder RAM) beeinflusst, die zum Ausführen der Anwendung verfügbar ist, sowie von der Auslastung dieses physischen Speichers durch andere ausgeführte Prozesse. Bei einer Beschränkung des physischen Speichers können sich für den Wert der Prozessarbeitsseite deutliche Schwankungen auftreten, wenn vom Betriebssystem versucht wird, die Speicherauslastung durch die aktive Prozesse auszugleichen, indem in regelmäßigen Abständen Seiten mit relativ geringer Aktivität aus Prozessarbeitsseiten gekürzt werden.  
  
 Weitere Informationen zu Prozessarbeitsseiten finden Sie unter [Working Set (Arbeitsseite)](http://go.microsoft.com/fwlink/?LinkId=177830) in der Dokumentation zur Speicherverwaltung unter Windows auf MSDN.  
  
## <a name="how-to-use-rule-data"></a>Verwenden von Regeldaten  
 Mithilfe des Regelwerts können Sie die Leistung anderer Versionen oder Builds des Programms vergleichen oder die Leistung der Anwendung in unterschiedlichen Profilerstellungsszenarios nachvollziehen.  
  
 Doppelklicken Sie auf die Meldung im Fenster „Fehlerliste“, um zur Ansicht [Markierungen](../profiling/marks-view.md) der Profilerstellungsdaten zu navigieren. Suchen Sie die Spalten **Prozess\Arbeitsseite** und **Arbeitsspeicher\Seiten/s**. Vergleichen Sie die beiden Spalten, um zu ermitteln, ob in bestimmten Phasen der Programmausführung ein erhöhtes Maß an E/A-Auslagerungsaktivitäten feststellbar ist.


