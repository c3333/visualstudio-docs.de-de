---
title: PROVIDER_PROCESS_DATA | Microsoft-Dokumentation
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- PROVIDER_PROCESS_DATA
helpviewer_keywords:
- PROVIDER_PROCESS_DATA structure
ms.assetid: ec2362ed-4a0c-4a09-9d66-8ff04e4f41ee
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: bdaf15d09af3199d026155cf7667f063f5bbe858
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80713782"
---
# <a name="provider_process_data"></a>PROVIDER_PROCESS_DATA
Diese Struktur enthält Informationen zu Prozessen, die auf einem Computer ausgeführt werden.

## <a name="syntax"></a>Syntax

```cpp
typedef struct tagPROVIDER_PROCESS_DATA {
   PROVIDER_FIELDS    Fields;
   PROGRAM_NODE_ARRAY ProgramNodes;
   BOOL               fIsDebuggerPresent;
} PROVIDER_PROCESS_DATA;
```

```csharp
public struct PROVIDER_PROCESS_DATA {
   public uint               Fields;
   public PROGRAM_NODE_ARRAY ProgramNodes;
   public int                fIsDebuggerPresent;
}
```

## <a name="members"></a>Member
 `Fields`\
 Eine Kombination von Flags aus der [PROVIDER_FIELDS](../../../extensibility/debugger/reference/provider-fields.md) Enumeration, die angibt, welche Felder ausgefüllt werden.

 `ProgramNodes`\
 Eine [PROGRAM_NODE_ARRAY](../../../extensibility/debugger/reference/program-node-array.md) Struktur, die ein Array von Programmknoten enthält.

 `fIsDebuggerPresent`\
 Ungleich NULL ( `TRUE` ), wenn der [!INCLUDE[vsprvs](../../../code-quality/includes/vsprvs_md.md)] Debugger ausgeführt wird, andernfalls 0 (NULL `FALSE` ) ().

## <a name="remarks"></a>Bemerkungen
 Diese Struktur wird an die [getproviderprocessdata](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md) -Methode übermittelt, wo Sie ausgefüllt ist.

## <a name="requirements"></a>Anforderungen
 Header: msdbg. h

 Namespace: Microsoft. VisualStudio. Debugger. Interop

 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

## <a name="see-also"></a>Weitere Informationen
- [Structures and Unions](../../../extensibility/debugger/reference/structures-and-unions.md)
- [PROVIDER_FIELDS](../../../extensibility/debugger/reference/provider-fields.md)
- [PROGRAM_NODE_ARRAY](../../../extensibility/debugger/reference/program-node-array.md)
- [GetProviderProcessData](../../../extensibility/debugger/reference/idebugprogramprovider2-getproviderprocessdata.md)
