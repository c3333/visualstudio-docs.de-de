---
title: 'Idebugarrayobject:: getElements | Microsoft-Dokumentation'
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- IDebugArrayObject::GetElement
helpviewer_keywords:
- IDebugArrayObject::GetElement method
ms.assetid: 08b44341-7bf1-4a8c-8b79-98ae5785b195
author: acangialosi
ms.author: anthc
manager: jillfra
ms.workload:
- vssdk
dev_langs:
- CPP
- CSharp
ms.openlocfilehash: e29fe09905119057224b45b455e4f56e5ce904af
ms.sourcegitcommit: 6cfffa72af599a9d667249caaaa411bb28ea69fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "80736183"
---
# <a name="idebugarrayobjectgetelement"></a>IDebugArrayObject::GetElement
Ruft ein Element des-Arrays ab.

## <a name="syntax"></a>Syntax

```cpp
HRESULT GetElement( 
   DWORD          dwIndex,
   IDebugObject** ppElement
);
```

```csharp
int GetElement(
   [In] uint dwIndex,
   out IDebugObject ppElement
);
```

## <a name="parameters"></a>Parameter
`dwIndex`\
in Der Element Index.

`ppElement`\
vorgenommen Gibt eine [idebugobject](../../../extensibility/debugger/reference/idebugobject.md) -Schnittstelle zurück, die das-Element darstellt.

## <a name="return-value"></a>Rückgabewert
 Wenn erfolgreich, wird S_OK zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen
 Diese Methode sieht alle Elemente eines Array Objekts als eindimensionales Array, auch wenn das Array Objekt mehrdimensional ist. Bei Angabe des `myarray[3][2][6]` -Arrays und eines `dwIndex` Parameters von 20 würde diese Methode z. b. das-Element von zurückgeben `myarray[1][1][2]` , und ein- `dwIndex` Parameter von 21 würde das-Element von zurückgeben `myarray[1][1][3]` . Verwenden Sie die [GetCount](../../../extensibility/debugger/reference/idebugarrayobject-getcount.md) -Methode, um die Gesamtzahl der Elemente im Array zu bestimmen.

## <a name="see-also"></a>Weitere Informationen
- [IDebugArrayObject](../../../extensibility/debugger/reference/idebugarrayobject.md)
