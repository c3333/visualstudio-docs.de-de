---
title: Visual Studio-Befehls Tabelle (. Vsct-Dateien | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- VSCT files, overview
- Visual Studio command table configuration files (VSCT), overview
ms.assetid: 1313adb4-add4-4e74-90e2-f4be522f5259
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 24ebac7aee2294d2ad8cee06cd88102bb8d3fd78
ms.sourcegitcommit: 4b29efeb3a5f05888422417c4ee236e07197fb94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2020
ms.locfileid: "90012346"
---
# <a name="visual-studio-command-table-vsct-files"></a>VSCT-Dateien (Visual Studio Command Table)
Eine Befehls Tabellen-Konfigurationsdatei ist eine Textdatei, die den Satz von Befehlen beschreibt, die ein VSPackage enthält. Der [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] Befehls tabellencompiler (vsct) kompiliert XML-basierte Konfigurationsdateien (vsct-Dateien) in binäre Befehls Tabellenausgabe Dateien (CTO). Die resultierenden CTO-Dateien sind identisch mit denen, die mit dem CTC-Compiler (Command Table) erstellt werden, um CTC-Konfigurationsdateien zu kompilieren. XML-basierte vsct-Dateien haben jedoch einige Vorteile, z. b. XML-Editor und XML-IntelliSense.

 Weitere Informationen zur Syntax und Semantik von vsct-Dateien finden Sie unter [Entwerfen einer XML-Befehls Tabelle (). Vsct-Dateien](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)

## <a name="in-this-section"></a>In diesem Abschnitt
 [Entwerfen von Dateien für XML-Befehlstabellen (VSCT)](../../extensibility/internals/designing-xml-command-table-dot-vsct-files.md)

 Beschreibt, wie vsct-Dateien entworfen werden.

 [Gewusst wie: Erstellen einer VSCT-Datei](../../extensibility/internals/how-to-create-a-dot-vsct-file.md)

 Vergleicht die Methoden zum Erstellen einer vsct-Datei. Beschreibt den Prozess zum manuellen Erstellen einer neuen vsct-Datei.

## <a name="related-sections"></a>Verwandte Abschnitte
 [VSCT-XML-Schemareferenz](../../extensibility/vsct-xml-schema-reference.md)

 Enthält Details zu den einzelnen Abschnitten der XML-Konfigurationsdatei der Befehls Tabelle.

 [Konfiguration der Befehls Tabelle (. CTC-Dateien (CTC)](/previous-versions/bb165153(v=vs.100)) stellen eine Übersicht über das veraltete CTC-Dateiformat dar.

 [Hinzufügen von Benutzeroberflächenelementen mit VSPackages](../../extensibility/internals/how-vspackages-add-user-interface-elements.md)

 Beschreibt die Spezifikation des Befehls Tabellen Formats.

 [Ressourcen in VSPackages](../../extensibility/internals/resources-in-vspackages.md)

 Beschreibt, wie verwaltete und nicht verwaltete Ressourcen in verwalteten VSPackages verwendet werden.

 [Befehle, Menüs und Symbolleisten](../../extensibility/internals/commands-menus-and-toolbars.md)

 Erläutert, wie eine Benutzeroberfläche mit Menüs, Symbolleisten und Kombinationsfeldern für Befehle erstellt wird.