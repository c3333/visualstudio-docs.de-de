---
title: Wann sollte ein Quellcodeverwaltungs-VSPackage implementiert werden?
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
- source control packages, about source control packages
ms.assetid: 60b3326e-e7e2-4729-95fc-b682e7ad5c99
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 16f96191115a509e07b5263f1d10d53ea3b2cc9c
ms.sourcegitcommit: 4ae5e9817ad13edd05425febb322b5be6d3c3425
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/11/2020
ms.locfileid: "90037041"
---
# <a name="determine-whether-to-implement-a-source-control-vspackage"></a>Bestimmen, ob ein Quellcodeverwaltungs-VSPackage implementiert werden soll

In diesem Abschnitt werden die Optionen der Quellcodeverwaltungs-Plug-ins und der Quellcodeverwaltungs-VSPackages zur Erweiterung der Quell Code Verwaltungslösungen erläutert, und es werden umfassende Richtlinien zur Auswahl eines geeigneten Integrations Pfads

## <a name="small-source-control-solution-with-limited-resources"></a>Lösung für kleine Quell Code Verwaltung mit eingeschränkten Ressourcen

 Wenn Sie nur über begrenzte Ressourcen verfügen und nicht mit dem Aufwand zum Schreiben eines Quell Code Verwaltungs Pakets belastet werden können, können Sie API-basierte Plug-Ins für die Quellcodeverwaltungs-Plug-ins erstellen. Auf diese Weise können Sie parallel mit Quell Code Verwaltungs Paketen arbeiten, und Sie können bei Bedarf zwischen den Quellcodeverwaltungs-Plug-ins und-Paketen wechseln. Weitere Informationen finden Sie unter [Registrierung und Auswahl](../../extensibility/internals/registration-and-selection-source-control-vspackage.md).

## <a name="large-source-control-solution-with-a-rich-feature-set"></a>Lösung für große Quell Code Verwaltung mit umfangreichem Featuresatz

 Wenn Sie eine Quell Code Verwaltungs Lösung implementieren möchten, die ein umfangreiches Quell Code Verwaltungsmodell bereitstellt, das nicht mit der Quellcodeverwaltungs-Plug-in-API ordnungsgemäß erfasst wird, können Sie ein Quell Code Verwaltungspaket als Integrations Pfad in Erwägung ziehen. Dies trifft vor allem dann zu, wenn Sie stattdessen das Quell Code Verwaltungs Adapter-Paket ersetzen (das mit Quellcodeverwaltungs-Plug-ins kommuniziert und eine einfache Benutzeroberfläche für die Quell Code Verwaltung bereitstellt), sodass Sie die Quell Code Verwaltungs Ereignisse auf benutzerdefinierte Weise behandeln können. Wenn Sie bereits über eine zufriedenstellende Quell Code Verwaltungs Benutzeroberfläche verfügen und diese Funktion in beibehalten möchten [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] , können Sie mit der Option "Quell Code Verwaltungspaket" genau das tun. Das Quell Code Verwaltungspaket ist nicht generisch und ausschließlich für die Verwendung mit [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] IDE vorgesehen.

 Wenn Sie eine Lösung für die Quell Code Verwaltung implementieren möchten, die Flexibilität und eine umfassendere Kontrolle über die Quell Code Verwaltungs Logik und die Benutzeroberfläche bietet, bevorzugen Sie möglicherweise die Integrations Route für das Quell Code Verwaltungspaket. Sie haben folgende Möglichkeiten:

1. Registrieren Sie Ihr eigenes VSPackage für die Quell Code Verwaltung (siehe [Registrierung und Auswahl](../../extensibility/internals/registration-and-selection-source-control-vspackage.md)).

2. Ersetzen Sie die Standardbenutzer Oberfläche der Quell Code Verwaltung durch Ihre benutzerdefinierte Benutzeroberfläche (siehe Benutzer [definierte Benutzeroberfläche](../../extensibility/internals/custom-user-interface-source-control-vspackage.md)).

3. Geben Sie Symbole an, die verwendet werden sollen, und behandeln Sie Projektmappen-Explorer Glyphe-Ereignisse (siehe [Glyphe-Steuer](../../extensibility/internals/glyph-control-source-control-vspackage.md)Element).

4. Behandeln von Ereignissen zum Bearbeiten und Abfragen von Abfragen (siehe Speichern der Abfrage [Bearbeiten](../../extensibility/internals/query-edit-query-save-source-control-vspackage.md)).

## <a name="see-also"></a>Weitere Informationen

- [Erstellen eines Quellcodeverwaltungs-Plug-ins](../../extensibility/internals/creating-a-source-control-plug-in.md)
