---
title: 'Gewusst wie: Hinzufügen eines Projekt Ausgabe Verweises | Microsoft-Dokumentation'
description: Erfahren Sie, wie Sie einen Projekt Ausgabe Verweis hinzufügen, sodass Sie nicht-SharePoint-Projektassemblys (oder XAP-Dateien in Silverlight-Projekten) in SharePoint bereitstellen können.
ms.custom: SEO-VS-2020
ms.date: 02/02/2017
ms.topic: how-to
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- project output references [SharePoint development in Visual Studio]
- SharePoint development in Visual Studio, project output references
- SharePoint development in Visual Studio, advanced packaging tools
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 03980eea9d16cde2b6f079e0b33973958fed7a7f
ms.sourcegitcommit: ad2c820b280b523a7f7aef89742cdb719354748f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "94849869"
---
# <a name="how-to-add-a-project-output-reference"></a>Gewusst wie: Hinzufügen eines Projekt Ausgabe Verweises
  Wenn Sie nicht-SharePoint-projekterassemblys (oder XAP-Dateien in Silverlight-Projekten) in SharePoint bereitstellen möchten, fügen Sie Sie als Projekt Ausgabe Verweis hinzu.

 Dieser Prozess erstellt eine Projektmappenbuild-Abhängigkeit zwischen den beiden Projekten. Projekte, die Projekt Ausgabe verweisen zugeordnet sind, werden erstellt, bevor das SharePoint-Projekt erstellt und bereitgestellt wird.

### <a name="to-add-a-project-output-reference"></a>So fügen Sie einen Projekt Ausgabe Verweis hinzu

1. Laden Sie eine Projekt Mappe, die mindestens ein SharePoint-Projekt und ein nicht-SharePoint-Projekt enthält.

2. Wählen Sie in **Projektmappen-Explorer** ein Element im SharePoint-Projekt Knoten aus.

3. Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Projekt Ausgabe Verweise** aus, und wählen Sie dann die Schaltfläche mit den Auslassungs Punkten (![ASP.NET Mobile Designer Ellipse](../sharepoint/media/mwellipsis.gif "Auslassungszeichen im ASP.NET Mobile-Designer")) Daneben aus.

4. Wählen Sie im Dialogfeld **Projekt Ausgabe Verweise** die Schaltfläche **Hinzufügen** aus.

5. Wählen Sie im Bereich Eigenschaften den Pfeil neben der Eigenschaft **Bereitstellungstyp** aus, und wählen Sie dann einen geeigneten Wert für das nicht-SharePoint-Element, auf das verwiesen wird, z. b. **Element File**.

6. Wählen Sie den Pfeil neben **Projekt Name** aus, wählen Sie den Namen des nicht-SharePoint-Projekt Elements aus, und klicken Sie dann auf die Schaltfläche **OK** .

## <a name="see-also"></a>Siehe auch
- [Bereitstellen von Pack- und Bereitstellungsinformationen in Projektelementen](../sharepoint/providing-packaging-and-deployment-information-in-project-items.md)
- [Gewusst wie: Markieren von Steuerelementen als sichere Steuerelemente](../sharepoint/how-to-mark-controls-as-safe-controls.md)
- [Packen und Bereitstellen von SharePoint-Lösungen](../sharepoint/packaging-and-deploying-sharepoint-solutions.md)
