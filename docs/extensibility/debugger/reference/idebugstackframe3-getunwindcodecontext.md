---
title: 'IDebugStackFrame3:: getunwindcodecontext | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugStackFrame3::GetUnwindCodeContext
helpviewer_keywords:
- IDebugStackFrame3::GetUnwindCodeContext method
ms.assetid: b25f7e7d-2b24-48e4-93b3-829e61d73ebf
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: 488f675c39bb01c87aca13a9bef8cc4a715ecf18
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80719500"
---
# <a name="idebugstackframe3getunwindcodecontext"></a>IDebugStackFrame3::GetUnwindCodeContext
Gibt den Code Kontext zurück, der einen Speicherort darstellt, wenn ein Stapel Entladevorgang aufgetreten ist.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetUnwindCodeContext(
   IDebugCodeContext2 **ppCodeContext
);
```

```csharp
int GetUnwindCodeContext(
   out IDebugCodeContext2 ppCodeContext
);
```

## <a name="parameters"></a>Parameter
`ppCodeContext`\
vorgenommen Gibt ein [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md) -Objekt zurück, das den Code Kontext Speicherort darstellt, wenn eine Stapel Entladung aufgetreten ist.

## <a name="return-value"></a>Rückgabewert
 Wenn die Ausführung erfolgreich ist, wird `S_OK`, andernfalls ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen
 Obwohl diese Methode möglicherweise einen Code Kontext für den Speicherort nach einer Stapel Entladung zurückgibt, bedeutet dies nicht unbedingt, dass die Stapel Entladung tatsächlich im aktuellen Stapel Rahmen auftreten kann.

## <a name="see-also"></a>Weitere Informationen
- [IDebugStackFrame3](../../../extensibility/debugger/reference/idebugstackframe3.md)
- [IDebugCodeContext2](../../../extensibility/debugger/reference/idebugcodecontext2.md)
