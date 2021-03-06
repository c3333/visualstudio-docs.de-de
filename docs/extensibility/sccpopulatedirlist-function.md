---
title: Sccpopulatedirlist-Funktion | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: conceptual
f1_keywords:
- SccPopulateDirList
helpviewer_keywords:
- SccPopulateDirList function
ms.assetid: dfff634b-b155-498b-a356-6eb252ac4fad
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 4ac1c51ac694acadd2efb0cd7d1c5a3f1d66ebc1
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80700555"
---
# <a name="sccpopulatedirlist-function"></a>SccPopulateDirList-Funktion
Diese Funktion bestimmt, welche Verzeichnisse und (optional) Dateien in der Quell Code Verwaltung gespeichert werden, wenn eine Liste der zu untersuchenden Verzeichnisse angegeben wird.

## <a name="syntax"></a>Syntax

```cpp
SCCRTN SccPopulateDirList(
   LPVOID        pContext,
   LONG          nDirs,
   LPCSTR*       lpDirPaths,
   POPDIRLISTFUNCpfnPopulate,
   LPVOID        pvCallerData,
   LONG          fOptions
);
```

#### <a name="parameters"></a>Parameter
 pContext

in Der Kontext Zeiger für das Quellcodeverwaltungs-Plug-in.

 ndirs

in Anzahl der Verzeichnispfade im `lpDirPaths` Array.

 lpdirpath

in Array der Verzeichnispfade, die untersucht werden sollen.

 pfnauffüllen

in Rückruffunktion, die für jeden Verzeichnispfad und (optional) filename in aufgerufen werden soll `lpDirPaths` (Weitere Informationen finden Sie unter [popdirlistfunc](../extensibility/popdirlistfunc.md) ).

 pvcallerdata

in Der Wert, der unverändert an die Rückruffunktion übermittelt werden soll.

 f-Optionen

in Eine Kombination von Werten, die die Verarbeitung der Verzeichnisse steuern (Weitere Informationen finden Sie im Abschnitt "Auffüllen von Auflistungs Flags" von [Bitflags, die von bestimmten Befehlen](../extensibility/bitflags-used-by-specific-commands.md) für mögliche Werte verwendet werden).

## <a name="return-value"></a>Rückgabewert
 Es wird erwartet, dass die Plug-in-Implementierung der Quell Code Verwaltung diese Funktion einen der folgenden Werte zurückgibt:

|Wert|BESCHREIBUNG|
|-----------|-----------------|
|SCC_OK|Der Vorgang wurde erfolgreich abgeschlossen.|
|SCC_E_UNKNOWNERROR|Ein Fehler ist aufgetreten.|

## <a name="remarks"></a>Bemerkungen
 Nur die Verzeichnisse und (optional) Dateinamen, die sich tatsächlich im Quellcodeverwaltungs-Repository befinden, werden an die Rückruffunktion übermittelt.

## <a name="see-also"></a>Weitere Informationen
- [API-Funktionen von Quellcodeverwaltungs-Plug-Ins](../extensibility/source-control-plug-in-api-functions.md)
- [Von bestimmten Befehlen verwendete Bitflags](../extensibility/bitflags-used-by-specific-commands.md)
- [POPDIRLISTFUNC](../extensibility/popdirlistfunc.md)
- [Fehlercodes](../extensibility/error-codes.md)
