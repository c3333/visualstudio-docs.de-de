---
title: Verwenden der Node.js-REPL
description: Visual Studio bietet Unterstützung für die Interaktion mit der Node.js-Runtime
ms.custom: ''
ms.date: 12/04/2018
ms.technology: vs-nodejs
ms.topic: conceptual
ms.devlang: javascript
author: mikejo5000
ms.author: mikejo
manager: douge
dev_langs:
- JavaScript
ms.workload:
- nodejs
ms.openlocfilehash: 7b980634a95c14413dd07649893a26b21de6f78d
ms.sourcegitcommit: a715de2ba8c703f37aa2102567b1aa2c0f05a117
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2018
ms.locfileid: "53441884"
---
# <a name="work-with-the-nodejs-interactive-window"></a>Arbeiten mit dem interaktiven Node.js-Fenster

Node.js-Tools für Visual Studio umfassen ein interaktives Fenster für die installierte Node.js-Runtime. In diesem Fenster können Sie JavaScript-Code eingeben und die Ergebnisse sofort sehen. Außerdem können Sie npm-Befehle ausführen, um mit dem aktuellen Projekt zu interagieren. Das interaktive Fenster ist auch als eine REPL (**R**ead/**E**valuate/**P**rint **L**oop) bekannt.

## <a name="open-the-interactive-window"></a>Öffnen des interaktiven Fensters

Sie können das interaktive Fenster öffnen, indem Sie im Projektmappen-Explorer mit der rechten Maustaste auf den Node.js-Projektknoten klicken und dann **Interaktives Node.js-Fenster** auswählen.

![Das interaktive Node.js-Fenster im Projektkontextmenü](../javascript/media/interactivewindow-open-from-project.png)

Die Standardtastenkombination zum Öffnen des interaktiven Node.js-Fensters lautet **STRG + K, N**. Alternativ können Sie das Fenster über die Symbolleiste öffnen, indem Sie auf **Ansicht** > **Windows** > **Interaktives Node.js-Fenster** klicken.

## <a name="use-the-repl"></a>Verwenden der REPL

Sobald Sie das Fenster geöffnet haben, können Sie Befehle eingeben.

![Interaktives Node.js-Fenster](../javascript/media/interactivewindow.png)

Das interaktive Fenster enthält mehrere integrierte Befehle, denen ein Punkt als Präfix vorangestellt wird, um sie von den JavaScript-Funktionen zu unterscheiden, die Sie deklarieren. Die folgenden Befehle werden unterstützt:

**.cls, .clear:** löscht den Inhalt des Editorfensters, Verlauf und Ausführungskontext bleiben erhalten.

**.help:** zeigt Hilfe zum angegebenen Befehl oder zu allen verfügbaren Befehlen und Tastenzuordnungen an, wenn kein spezifischer Befehl angegeben wird.

**.info:** zeigt Informationen zur aktuell verwendeten ausführbaren Node.js-Datei an.

**.npm:** führt einen npm-Befehl aus. Wenn die Projektmappe mehrere Projekte enthält, geben Sie das Zielprojekt mit `.npm [projectname] <npm arguments>` an.

**.reset:** setzt die Ausführungsumgebung in den ursprünglichen Zustand zurück. Der Verlauf wird beibehalten.

**.save:** speichert die aktuelle REPL-Sitzung in einer Datei.