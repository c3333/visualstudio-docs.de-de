---
title: Modulansicht | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- vs.performance.view.modules
helpviewer_keywords:
- Modules view
- profiling tools reports, Modules view
- profiling tools, Modules view
ms.assetid: 4314a404-2120-425b-be42-180cd4bac840
author: mikejo5000
ms.author: mikejo
manager: jillfra
monikerRange: vs-2017
ms.workload:
- multiple
ms.openlocfilehash: 89d9146b3f724b4883f21a43689a495eef252777
ms.sourcegitcommit: cc841df335d1d22d281871fe41e74238d2fc52a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "74778517"
---
# <a name="modules-view"></a>Modulansicht
In der Modulansicht werden die Module der Profilerstellungsdaten aufgelistet. Jedes Modul ist der Stammknoten einer hierarchischen Struktur. Die Profilfunktionen des Moduls, für die ein Sampling ausgeführt wurde, werden unter dem Modulknoten aufgeführt. Wenn die Profilerstellungsdaten mithilfe der Samplingmethode gesammelt wurden, werden Zeileninformationen unter dem Funktionsknoten aufgelistet, und Anweisungszeigerdaten werden unter dem Zeilenknoten aufgelistet.

 Erweitern oder reduzieren Sie den Modulnamen, um die Ansicht der Modulleistungsdaten anzuzeigen oder zu schließen.

 Klicken Sie zum Hinzufügen oder Entfernen von Spalten mit der rechten Maustaste in das Berichtsfenster, und wählen Sie anschließend **Spalten hinzufügen/entfernen** aus. Sie können die Daten durch Klicken auf einen Spaltennamen sortieren. Weitere Informationen finden Sie unter [Vorgehensweise: Anpassen von Spalten in der Berichtsansicht](../profiling/how-to-customize-report-view-columns.md).

 Welche Spalten in der Modulansicht verfügbar sind, ist abhängig von der Profilerstellungsmethode (Sampling oder Instrumentierung), die zum Sammeln der Daten verwendet wurde, und davon, ob in der Profilerstellungsausführung .NET-Arbeitsspeicherdaten gesammelt wurden.

## <a name="see-also"></a>Weitere Informationen
- [Modulansicht](../profiling/modules-view-sampling-data.md)
- [Modulansicht](../profiling/modules-view-instrumentation-data.md)
- [Modulansicht: .NET-Speicherinstrumentierungsdaten](../profiling/modules-view-dotnet-memory-instrumentation-data.md)
- [Modulansicht: Sampling](../profiling/modules-view-dotnet-memory-sampling-data.md)
- [Modulansicht](../profiling/modules-view-contention-data.md)
