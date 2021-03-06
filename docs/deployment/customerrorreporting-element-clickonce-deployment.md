---
title: '&lt;customErrorReporting- &gt; Element (ClickOnce-Bereitstellung) | Microsoft-Dokumentation'
description: Das customErrorReporting-Element gibt einen URI an, der angezeigt wird, wenn anstelle eines Fehler Dialogfelds, das den Ausnahme Stapel anzeigt, ein Fehler auftritt.
ms.custom: SEO-VS-2020
ms.date: 11/04/2016
ms.topic: reference
dev_langs:
- VB
- CSharp
- C++
helpviewer_keywords:
- <customErrorReporting> element [ClickOnce deployment manifest]
ms.assetid: 7d31816e-c692-46b5-9cc9-753284b3bcda
author: mikejo5000
ms.author: mikejo
manager: jillfra
ms.workload:
- multiple
ms.openlocfilehash: 5576912fb428e15a6f8164e52d558e255e184fe3
ms.sourcegitcommit: 0893244403aae9187c9375ecf0e5c221c32c225b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/09/2020
ms.locfileid: "94382519"
---
# <a name="ltcustomerrorreportinggt-element-clickonce-deployment"></a>&lt;customErrorReporting- &gt; Element (ClickOnce-Bereitstellung)
Gibt einen URI an, der bei einem Fehler angezeigt wird.

## <a name="syntax"></a>Syntax

```xml
<customErrorReporting
   uri
/>
```

## <a name="remarks"></a>Hinweise
 Dieses Element ist optional. Ohne diese wird [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] ein Fehler Dialogfeld angezeigt, das den Ausnahme Stapel anzeigt. Wenn das- `customErrorReporting` Element vorhanden ist, [!INCLUDE[ndptecclick](../deployment/includes/ndptecclick_md.md)] zeigt stattdessen den URI an, der durch den-Parameter angegeben wird `uri` . Der Ziel-URI schließt die äußere Ausnahme Klasse, die innere Ausnahme Klasse und die interne Ausnahme Meldung als Parameter ein.

 Verwenden Sie dieses Element, um der Anwendung Fehler Berichterstattungs Funktionen hinzuzufügen. Da der generierte URI Informationen über den Fehlertyp enthält, kann die Website diese Informationen analysieren und anzeigen, z. b. einen passenden Bildschirm zur Problembehandlung.

## <a name="example"></a>Beispiel
 Der folgende Code Ausschnitt zeigt das- `customErrorReporting` Element sowie den generierten URI, der möglicherweise erzeugt wird.

```xml
<customErrorReporting uri=http://www.contoso.com/applications/error.asp />

Example Generated Error:
http://www.contoso.com/applications/error.asp? outer=System.Deployment.Application.InvalidDeploymentException&&inner=System.Deployment.Application.InvalidDeploymentException&&msg=The%20application%20manifest%20is%20signed,%20but%20the%20deployment%20manifest%20is%20unsigned.%20Both%20manifests%20must%20be%20either%20signed%20or%20unsigned.
```

## <a name="see-also"></a>Siehe auch
- [ClickOnce-Bereitstellungs Manifest](../deployment/clickonce-deployment-manifest.md)