---
title: Lauf Zeit Details der Quell Code Verwaltung | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control [Visual Studio SDK], runtime details
ms.assetid: 1acd30e0-f98c-4bde-b9cd-4076845887df
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 92ce5e822ec7360b3b1a4010d250a4349443c142
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80705036"
---
# <a name="source-control-runtime-details"></a>Laufzeitdetails für die Quellcodeverwaltung
Ein Projekt wird der Quell Code Verwaltung hinzugefügt, wenn der Benutzer der Quell Code Verwaltung eine Datei im Projekt hinzufügt, oder über einen Automatisierungs Controller, z. b. einen Assistenten. Ein Projekt gibt nicht für sich selbst an, dass es sich unter Quell Code Verwaltung befindet. die Quell Code Verwaltung wird unterstützt, muss aber manuell hinzugefügt werden.

## <a name="registering-with-a-source-control-package"></a>Registrieren mit einem Quell Code Verwaltungspaket
 Wenn eine Datei in Ihrem Projekt zur Quell Code Verwaltung hinzugefügt wird, ruft die Umgebung auf, um Ihnen vier nicht transparente Zeichen folgen zur <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A> Verfügung zu stellen, die vom Quell Code Verwaltungssystem als Cookies verwendet werden. Speichern Sie diese Zeichen folgen in der Projektdatei. Diese Zeichen folgen müssen an den Quellcodeverwaltungs-Stub (die Visual Studio-Komponente, die Quell Code Verwaltungs Pakete verwaltet) beim Start des Projekt Typs durch Aufrufen von weitergeleitet werden <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A> . Dadurch wird das entsprechende Quell Code Verwaltungspaket geladen, und der-Befehl wird an die-Implementierung von weitergeleitet `IVsSccManager2::RegisterSccProject` .

## <a name="see-also"></a>Weitere Informationen
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccManager2.RegisterSccProject%2A>
- <xref:Microsoft.VisualStudio.Shell.Interop.IVsSccProject2.SetSccLocation%2A>
- [Unterstützen der Quellcodeverwaltung](../../extensibility/internals/supporting-source-control.md)
