---
title: IEEVisualizerServiceProvider | Microsoft-Dokumentation
ms.custom: ''
ms.date: 2018-06-30
ms.prod: visual-studio-dev14
ms.reviewer: ''
ms.suite: ''
ms.technology:
- vs-ide-sdk
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- IEEVisualizerServiceProvider
helpviewer_keywords:
- IEEVisualizerServiceProvider interface
ms.assetid: 859d1a51-1c65-4c8b-ae74-3b74b181ebcd
caps.latest.revision: 18
ms.author: gregvanl
manager: ghogen
ms.openlocfilehash: e27eab6c3547790ca1f66181c04bba085e463c5e
ms.sourcegitcommit: 55f7ce2d5d2e458e35c45787f1935b237ee5c9f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/22/2018
ms.locfileid: "47510148"
---
# <a name="ieevisualizerserviceprovider"></a>IEEVisualizerServiceProvider
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

Die neueste Version dieses Themas finden Sie unter [IEEVisualizerServiceProvider](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/ieevisualizerserviceprovider).  
  
> [!IMPORTANT]
>  In Visual Studio 2015 ist diese Art der Implementierung von ausdrucksauswertungen veraltet. Informationen zu CLR-ausdrucksauswertungen implementieren, finden Sie unter [CLR Ausdrucksauswertungen](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/CLR-Expression-Evaluators) und [Managed Expression Evaluator Sample](https://github.com/Microsoft/ConcordExtensibilitySamples/wiki/Managed-Expression-Evaluator-Sample).  
  
 Diese Schnittstelle bietet Zugriff auf eine Methode, die einen schnellansichtsdienst erstellen können, die verwendet wird, um Typ Schnellansicht Aufgaben für die IDE zu behandeln.  
  
## <a name="syntax"></a>Syntax  
  
```  
IEEVisualizerServiceProvider : IUnknown  
```  
  
## <a name="notes-for-implementers"></a>Hinweise für Implementierer  
 Visual Studio implementiert diese Schnittstelle, um ein Dienstobjekt der Schnellansicht zu erstellen, der wiederum verwendet wird, geben Sie die Klassen-IDs (`CLSID`s) des Typ-Schnellansichten der Visual Studio-IDE.  
  
## <a name="notes-for-callers"></a>Hinweise für Aufrufer  
 Ruft die ausdrucksauswertung (EE) [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md) dieser Schnittstelle abgerufen.  
  
## <a name="methods-in-vtable-order"></a>Methoden in Vtable-Reihenfolge  
  
|Methode|Beschreibung|  
|------------|-----------------|  
|[CreateVisualizerService](../../../extensibility/debugger/reference/ieevisualizerserviceprovider-createvisualizerservice.md)|Erstellt die schnellansichtsdienst|  
  
## <a name="remarks"></a>Hinweise  
 Die `IEEVisualizerServiceProvider` Schnittstelle wird abrufen, während der Implementierung der [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md). Der schnellansichtsdienst, erstellt diese Schnittstelle, wird verwendet, zum Bereitstellen von Funktionen zu einer [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md) Schnittstelle, die die EE für die Implementierung verantwortlich ist. Die EE ist auch verantwortlich für die Implementierung einer [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md) Schnittstelle, die Typ-Schnellansichten anzeigen und ändern den Wert einer Eigenschaft ermöglicht.  
  
 Finden Sie unter [visualisieren und Anzeigen von Daten](../../../extensibility/debugger/visualizing-and-viewing-data.md) Einzelheiten, wie diese Schnittstellen zu interagieren.  
  
## <a name="requirements"></a>Anforderungen  
 Header: ee.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## <a name="see-also"></a>Siehe auch  
 [Schnittstellen für die Ausdrucksauswertung](../../../extensibility/debugger/reference/expression-evaluation-interfaces.md)   
 [EvaluateSync](../../../extensibility/debugger/reference/idebugparsedexpression-evaluatesync.md)   
 [IEEVisualizerDataProvider](../../../extensibility/debugger/reference/ieevisualizerdataprovider.md)   
 [GetEEService](../../../extensibility/debugger/reference/idebugbinder3-geteeservice.md)   
 [IDebugProperty3](../../../extensibility/debugger/reference/idebugproperty3.md)   
 [Visualisieren und Anzeigen von Daten](../../../extensibility/debugger/visualizing-and-viewing-data.md)
