---
title: Einstellungen für die Auslastungstestprotokollierung
ms.date: 10/19/2016
ms.topic: conceptual
helpviewer_keywords:
- load tests, logging, modifying
ms.assetid: 9649226a-857d-41ef-8ec7-047b6e498033
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.openlocfilehash: 0c0a9967f1248c6dc23c5d70be35788ad9e05eb2
ms.sourcegitcommit: cc841df335d1d22d281871fe41e74238d2fc52a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/18/2020
ms.locfileid: "75566305"
---
# <a name="modify-load-test-logging-settings"></a>Ändern von Einstellungen für die Auslastungstestprotokollierung

Das Auslastungstestergebnis für den abgeschlossenen Auslastungstest enthält Leistungsindikatorsamplings und Fehlerinformationen, die in regelmäßigen Abständen von den Testcomputern in einem Protokoll erfasst wurden. Im Verlauf eines Auslastungstestlaufs kann eine große Anzahl von Leistungsindikatorsamplings erfasst werden. Die Menge der gesammelten Leistungsdaten hängt von der Länge des Testlaufs, dem Samplingintervall, der Anzahl von Testcomputern und der Anzahl zu erfassender Indikatoren ab. Da bei einem großen Auslastungstest die gesammelte Menge von Leistungsdaten leicht mehrere Gigabytes betragen kann, können Sie ggf. die Häufigkeit ändern, mit der Daten im Protokoll gespeichert werden. Weitere Informationen finden Sie unter [Testcontroller und Test-Agents](configure-test-agents-and-controllers-for-load-tests.md).

[!INCLUDE [web-load-test-deprecated](includes/web-load-test-deprecated.md)]

Der *Testcontroller* spoolt während der Testausführung alle gesammelten Beispieldaten des Auslastungstests in ein Datenbankprotokoll. Weitere Daten, z. B. Details zur zeitlichen Steuerung und Fehlerdetails, werden nach Abschluss des Tests in die Datenbank geladen.

|Aufgabe|Verwandte Themen|
|-|-----------------------|
|**Speichern von Protokollen bei einem Auslastungstestfehler:** Sie können angeben, ob das Testprotokoll gespeichert werden soll, wenn ein Auslastungstest fehlschlägt.|-   [Vorgehensweise: Angeben, ob Testfehler in Testprotokollen gespeichert werden](../test/how-to-specify-if-test-failures-are-saved-to-test-logs.md)|
|**Festlegen der maximalen Dateigröße für die Protokolldatei:** Sie können die XML-Konfigurationsdatei für den Testcontrollerdienst bearbeiten, um die gewünschte maximale Dateigröße für die Protokolldatei anzugeben.|Ändern Sie `<add key="LogSizeLimitInMegs" value="20"/>` in der *QTCcontroller.exe.config* XML-Konfigurationsdatei.|

## <a name="see-also"></a>Weitere Informationen

- [Konfigurieren der Laufzeiteinstellungen für Auslastungstests](../test/configure-load-test-run-settings.md)
