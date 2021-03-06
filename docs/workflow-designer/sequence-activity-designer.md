---
title: Workflow-Designer-Sequence-Aktivitäts Designer
description: Erfahren Sie, wie die Sequence-Aktivität eine geordnete Auflistung von untergeordneten Aktivitäten enthält, die in der Reihenfolge ausgeführt werden.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- System.Activities.Statements.Sequence.UI
ms.assetid: 51c8d3cb-4d43-458f-9631-b63755f9ac94
author: TerryGLee
ms.author: tglee
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: b9e7e6e9114405bc1575e0256dd63211a4fb6d08
ms.sourcegitcommit: ed26b6e313b766c4d92764c303954e2385c6693e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94433972"
---
# <a name="sequence-activity-designer"></a>Sequence-Aktivitätsdesigner

Die <xref:System.Activities.Statements.Sequence>-Aktivität enthält eine geordnete Auflistung von untergeordneten Aktivitäten, die in der angegebenen Reihenfolge ausgeführt werden.

Eine andere Möglichkeit, eine Gruppe von Aktivitäten in einer bestimmten Reihenfolge auszuführen, besteht in der Verwendung einer <xref:System.Activities.Statements.Flowchart>-Aktivität. Verwenden Sie ggf. das Flussdiagramm, wenn ein einfacher Verzweigungs-oder Schleifen Programmfluss vorhanden ist, den Sie [Diagramms](../workflow-designer/flowchart-activity-designer.md) modellieren möchten.

## <a name="using-the-sequence-activity-designer"></a>Verwenden des Sequence-Aktivitätsdesigners

Ziehen Sie zum Hinzufügen einer- <xref:System.Activities.Statements.Sequence> Aktivität den **Sequence** -Aktivitäts Designer aus der **Toolbox** , und legen Sie ihn auf der Workflow-Designer Oberfläche ab. Um dieser Aktivität eine untergeordnete Aktivität hinzuzufügen <xref:System.Activities.Statements.Sequence> , ziehen Sie eine andere Aktivität aus der **Toolbox** , und legen Sie Sie auf dem Dreieck im Feld mit dem Hinweis Text "Aktivität hier ablegen" ab.

### <a name="sequence-activity-properties-in-the-workflow-designer"></a>Eigenschaften der Sequence-Aktivität im Workflow-Designer

In der folgenden Tabelle werden die <xref:System.Activities.Statements.Sequence>-Eigenschaften aufgeführt, und es wird beschrieben, wie sie im Designer verwendet werden. Diese Eigenschaften können im Eigenschaftenraster oder auf der Designeroberfläche bearbeitet werden.

|Eigenschaftenname|Erforderlich|Verwendung|
|-|--------------|-|
|<xref:System.Activities.Activity.DisplayName%2A>|FALSE|Gibt den benutzerfreundlichen Namen der <xref:System.Activities.Statements.Sequence>Aktivität im Header an. Der Standardwert ist Sequence. Der Wert kann im Eigenschaftenraster oder direkt im Header des Aktivitätsdesigners bearbeitet werden.<br /><br /> Obwohl der <xref:System.Activities.Activity.DisplayName%2A> nicht zwingend erforderlich ist, wird empfohlen, einen Anzeigenamen zu verwenden.|

## <a name="see-also"></a>Siehe auch

- [Flussdiagramm](../workflow-designer/flowchart-activity-designer.md)
- [Ablaufsteuerung](../workflow-designer/control-flow-activity-designers.md)