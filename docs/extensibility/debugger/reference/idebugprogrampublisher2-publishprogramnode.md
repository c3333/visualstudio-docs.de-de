---
title: IDebugProgramPublisher2::P ublishprogramnode | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugProgramPublisher2::PublishProgramNode
helpviewer_keywords:
- IDebugProgramPublisher2::PublishProgramNode
ms.assetid: d4b72e04-f726-46cf-8e56-5203ff205b12
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: df68e72ee8597805bf02cb9c6e1c3a0bcaf8a449
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80721668"
---
# <a name="idebugprogrampublisher2publishprogramnode"></a>IDebugProgramPublisher2::PublishProgramNode
Macht einen Programmknoten für die Verwendung durch Debug-engines (des) und den Sitzungs-Debug-Manager (SDM) verfügbar.

## <a name="syntax"></a>Syntax

```cpp
HRESULT PublishProgramNode(
   IDebugProgramNode2 *pProgramNode
);
```

```csharp
int PublishProgramNode(
   IDebugProgramNode2 pProgramNode
);
```

## <a name="parameters"></a>Parameter
`pProgramNode`\
in Ein [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md) -Objekt, das den zu verfügbaren Programmknoten darstellt.

## <a name="return-value"></a>Rückgabewert
 Wenn die Ausführung erfolgreich ist, wird `S_OK`, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen
 Diese Methode ermöglicht es Programmen, Informationen zu Abfragen, bevor Sie zum Debuggen ausgewählt und gestartet werden.

 Um einen Programmknoten aus der Verfügbarkeit zu entfernen, müssen Sie die [unpublishprogramnode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md) -Methode aufrufen.

## <a name="see-also"></a>Weitere Informationen
- [IDebugProgramPublisher2](../../../extensibility/debugger/reference/idebugprogrampublisher2.md)
- [IDebugProgramNode2](../../../extensibility/debugger/reference/idebugprogramnode2.md)
- [UnpublishProgramNode](../../../extensibility/debugger/reference/idebugprogrampublisher2-unpublishprogramnode.md)
