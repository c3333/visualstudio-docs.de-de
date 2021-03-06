---
title: IDebugBreakEvent2 | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugBreakEvent2
helpviewer_keywords:
- IDebugBreakEvent2 interface
ms.assetid: 57dfdbc2-4e68-4dbf-9579-006cd6fb1c62
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
ms.openlocfilehash: 1af6ce13de529fef5e16b3bc1be7053f0e1347b6
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80735391"
---
# <a name="idebugbreakevent2"></a>IDebugBreakEvent2
Diese Schnittstelle weist den sitzungsdebug-Manager (SDM) darauf hin, dass eine asynchrone Unterbrechung erfolgreich abgeschlossen wurde.

## <a name="syntax"></a>Syntax

```
IDebugBreakEvent2 : IUnknown
```

## <a name="notes-for-implementers"></a>Hinweise für Implementierer
 Die de implementiert diese Schnittstelle, um Benutzer Umbrüche in einem Programm zu unterstützen. Die [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md) -Schnittstelle muss auf demselben Objekt wie diese Schnittstelle implementiert werden (SDM verwendet [QueryInterface](/cpp/atl/queryinterface) für den Zugriff auf die- `IDebugEvent2` Schnittstelle).

## <a name="notes-for-callers"></a>Hinweise für Aufrufer
 Der SDM ruft [cauanbreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md) auf, wenn der Benutzer angefordert hat, dass das Programm, das gedeppt wird, angehalten werden soll. Wenn das Programm erfolgreich angehalten wurde, sendet der de das `IDebugBreakEvent2` Ereignis. Dieses Ereignis wird mithilfe der [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md) -Rückruffunktion gesendet, die von SDM beim Anfügen an das gedestete Programm bereitgestellt wird.

## <a name="remarks"></a>Bemerkungen
 Beispielsweise kann ein Benutzer im Menü **Debuggen** den Befehl **Alle unterbrechen** auswählen, um das Programm zu verlassen, das eine Endlosschleife ausführen soll. Der SDM weist das Programm an, durch den Aufruf von [caust Break](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)anzuhalten. Der de sendet, `IDebugBreakEvent2` Wenn das Programm beendet wird.

## <a name="requirements"></a>Anforderungen
 Header: msdbg. h

 Namespace: Microsoft. VisualStudio. Debugger. Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Weitere Informationen
- [CauseBreak](../../../extensibility/debugger/reference/idebugprogram2-causebreak.md)
- [IDebugEvent2](../../../extensibility/debugger/reference/idebugevent2.md)
- [IDebugEventCallback2](../../../extensibility/debugger/reference/idebugeventcallback2.md)
