---
title: Hinzufügen eines Attributs zu einem Projekt Element | Microsoft-Dokumentation
description: Erfahren Sie, wie Sie ein Attribut zu einem Projekt Element in Visual Studio hinzufügen, indem Sie die shellinterop-Methoden getitemattribute und setitemattribute verwenden.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- attributes [Visual Studio], adding to a project item
ms.assetid: 404a71d5-cce5-44e7-9eaf-d747c794fedb
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 79f96be0d9b2ba661c29cdc1a25d7348bcff6eb1
ms.sourcegitcommit: d6207a3a590c9ea84e3b25981d39933ad5f19ea3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "95597911"
---
# <a name="add-an-attribute-to-a-project-item"></a>Hinzufügen eines Attributs zu einem Projekt Element
Mit den Methoden <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.GetItemAttribute%2A> und wird <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> der Wert der Attribute eines Projekt Elements erhalten und festgelegt. "", Wenn das Attribut nicht bereits vorhanden ist, wird das Attribut erstellt, und die Metadaten werden den Projekt Element Metadaten hinzugefügt.

## <a name="add-an-attribute-to-a-project-item"></a>Hinzufügen eines Attributs zu einem Projekt Element

- Im folgenden Code werden das <xref:EnvDTE.DTE> Automation-Objekt und die- <xref:Microsoft.VisualStudio.Shell.Interop.IVsBuildPropertyStorage.SetItemAttribute%2A> Methode verwendet, um einem Projekt Element ein Attribut hinzuzufügen. Die Projekt Element-ID wird aus dem Projekt Elementnamen "Program.cs" abgerufen. Das Attribut "MyAttribute" wird diesem Projekt Element hinzugefügt und erhält den Wert "myValue".

    ```csharp
    EnvDTE.DTE dte = (EnvDTE.DTE)Package.GetGlobalService(typeof(EnvDTE.DTE));
    EnvDTE.Project project = dte.Solution.Projects.Item(1);

    string uniqueName = project.UniqueName;
    IVsSolution solution = (IVsSolution)Package.GetGlobalService(typeof(SVsSolution));
    IVsHierarchy hierarchy;
    solution.GetProjectOfUniqueName(uniqueName, out hierarchy);
    IVsBuildPropertyStorage buildPropertyStorage = hierarchy as IVsBuildPropertyStorage;
    if (buildPropertyStorage != null)
    {
        uint itemId;
        string fullPath = (string)project.ProjectItems.Item("Program.cs").Properties.Item("FullPath").Value;
        hierarchy.ParseCanonicalName(fullPath, out itemId);
        buildPropertyStorage.SetItemAttribute(itemId, "MyAttribute", "MyValue");
    }

    ```

## <a name="see-also"></a>Siehe auch
- [Persistente Daten in der MSBuild-Projektdatei](../extensibility/internals/persisting-data-in-the-msbuild-project-file.md)
