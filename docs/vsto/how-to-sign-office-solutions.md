---
title: 'Gewusst wie: Signieren von Office-Lösungen'
ms.date: 02/02/2017
ms.topic: how-to
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- certificates [Office development in Visual Studio], Office solutions
- security [Office development in Visual Studio], signing Office solutions
- signing manifests [Office development in Visual Studio]
author: John-Hart
ms.author: johnhart
manager: jillfra
ms.workload:
- office
ms.openlocfilehash: 23afc171fd97620b3e6801b8d199da6890198d8b
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "85545755"
---
# <a name="how-to-sign-office-solutions"></a>Gewusst wie: Signieren von Office-Lösungen
  Wenn Sie eine Lösung signieren, können Sie der Lösung mithilfe des Zertifikats als Beweis Vertrauen gewähren. Sie können das gleiche Zertifikat für mehrere Lösungen verwenden, und alle Lösungen werden ohne zusätzliche Sicherheitsrichtlinien Updates als vertrauenswürdig eingestuft.

 [!INCLUDE[appliesto_all](../vsto/includes/appliesto-all-md.md)]

 Wenn Sie Anwendungs-und Bereitstellungs Manifeste manuell mithilfe der Manifest Generation and Editing Tool (*mage.exe* und *mageui.exe*) bearbeiten, müssen Sie die Manifeste erneut signieren, bevor Sie Sie verwenden können. Weitere Informationen finden Sie unter Gewusst [wie: Erneutes Signieren von Anwendungs-und Bereitstellungs Manifesten](../deployment/how-to-re-sign-application-and-deployment-manifests.md).

## <a name="sign-by-using-a-certificate"></a>Signieren mit einem Zertifikat
 Ein Zertifikat ist eine Datei, die einen eindeutigen Schlüssel und die Identität des Lösungs Verlegers enthält. Sie können Zertifikate von einer Zertifizierungsstelle erwerben oder ein eigenes Zertifikat erstellen und von einer Zertifizierungsstelle signieren.

 Visual Studio signiert Office-Projektmappen mit einem temporären Zertifikat zum Aktivieren des Debuggens. Sie sollten das temporäre Zertifikat in bereitgestellten Lösungen nicht als Beweis verwenden.

### <a name="to-sign-an-office-solution-by-using-a-certificate"></a>So signieren Sie eine Office-Projekt Mappe mithilfe eines Zertifikats

1. Klicken Sie im Menü **Projekt** auf**Eigenschaften**von _SolutionName_.

2. Klicken Sie auf die Registerkarte **Signierung** .

3. Wählen Sie **ClickOnce-Manifeste signieren**aus.

4. Suchen Sie das Zertifikat, indem **Sie auf aus Speicher auswählen** klicken oder **aus Datei auswählen** und zum Zertifikat navigieren.

5. Um sicherzustellen, dass das richtige Zertifikat verwendet wird, klicken Sie auf **Weitere Details** , um die Zertifikat Informationen anzuzeigen.

## <a name="see-also"></a>Weitere Informationen

- [Sichere Office-Lösungen](../vsto/securing-office-solutions.md)
- [Gewähren von Vertrauenswürdigkeit für Office-Lösungen](../vsto/granting-trust-to-office-solutions.md)
- [Seite "Signierung", Projekt-Designer](../ide/reference/signing-page-project-designer.md)
