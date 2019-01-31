---
title: Bereitstellen eines ASP.NET-Docker-Containers für Azure Container Registry (ACR) | Microsoft-Dokumentation
description: Erfahren Sie, wie Sie Visual Studio-Tools für Docker zum Bereitstellen einer ASP.NET Core-Web-App für eine Containerregistrierung verwenden.
services: azure-container-service
documentationcenter: .net
author: mlearned
manager: jillfra
ms.assetid: e5e81c5e-dd18-4d5a-a24d-a932036e78b9
ms.service: azure-container-service
ms.devlang: dotnet
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: NA
ms.date: 05/21/2018
ms.author: mlearned
ms.openlocfilehash: 8ba7244ffc482c33409bc280617b60ce1e85b504
ms.sourcegitcommit: 2193323efc608118e0ce6f6b2ff532f158245d56
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2019
ms.locfileid: "55140766"
---
# <a name="deploy-an-aspnet-container-to-a-container-registry-using-visual-studio"></a>Bereitstellen eines ASP.NET-Containers an eine Containerregistrierung mithilfe von Visual Studio

## <a name="overview"></a>Übersicht

Docker ist eine einfache Container-Engine, in gewisser Weise mit einem virtuellen Computer vergleichbar, die Sie zum Hosten von Anwendungen und Diensten verwenden können.
Dieses Tutorial führt Sie durch die Verwendung von Visual Studio zum Veröffentlichen Ihrer Containeranwendung für eine [Azure-Containerregistrierung](https://azure.microsoft.com/services/container-registry).

Wenn Sie kein Azure-Abonnement besitzen, können Sie ein [kostenloses Konto](https://azure.microsoft.com/free/dotnet/?utm_source=acr-publish-doc&utm_medium=docs&utm_campaign=docs) erstellen, bevor Sie beginnen.

## <a name="prerequisites"></a>Erforderliche Komponenten

Zum Abschließen dieses Tutorials benötigen Sie Folgendes:

* Installieren der neuesten Version von [Visual Studio 2017](https://azure.microsoft.com/downloads/) mit der Workload „ASP.NET und Webentwicklung“
* Installieren von [Docker für Windows](https://docs.docker.com/docker-for-windows/install/)

## <a name="1-create-an-aspnet-core-web-app"></a>1. Erstellen einer ASP.NET Core-Web-App
Die folgenden Schritte führen Sie durch die Erstellung einer einfachen ASP.NET Core-App, die in diesem Tutorial verwendet wird.

[!INCLUDE [create-aspnet5-app](../azure/includes/create-aspnet5-app.md)]

## <a name="2-publish-your-container-to-azure-container-registry"></a>2. Veröffentlichen Ihres Containers in Azure Container Registry
1. Klicken Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf das Projekt, und wählen Sie **Veröffentlichen**.
2. Wählen Sie im Dialogfeld „Ziel veröffentlichen“ die Registerkarte **Container Registry**.
3. Wählen Sie **Neue Azure-Containerregistrierung**, und klicken Sie auf **Veröffentlichen**.
4. Geben Sie die gewünschten Werte im Feld **Neue Azure-Containerregistrierung erstellen** ein.

    | Einstellung      | Empfohlener Wert  | BESCHREIBUNG                                |
    | ------------ |  ------- | -------------------------------------------------- |
    | **DNS-Präfix** | Global eindeutiger Name | Name, der Ihre Containerregistrierung eindeutig identifiziert. |
    | **Abonnement** | Auswählen Ihres Abonnements | Das zu verwendende Azure-Abonnement. |
    | **[Ressourcengruppe](/azure/azure-resource-manager/resource-group-overview)** | myResourceGroup |  Name der Ressourcengruppe, in der die Containerregistrierung erstellt werden soll. Wählen Sie **Neu** aus, um eine neue Ressourcengruppe zu erstellen.|
    | **[SKU](https://docs.microsoft.com/azure/container-registry/container-registry-skus)** | Standard | Dienstebene der Containerregistrierung  |
    | **Registrierungsstandort** | Ein Standort in Ihrer Nähe | Wählen Sie einen Standort in einer [Region](https://azure.microsoft.com/regions/) in Ihrer Nähe oder in der Nähe anderer Dienste aus, die Ihre Containerregistrierung verwenden werden. |

    ![Visual Studio-Dialogfeld zum Erstellen einer Azure-Containerregistrierung](media/vs-azure-tools-docker-hosting-web-apps-in-docker/vs-acr-provisioning-dialog.png)

5. Klicken Sie auf **Erstellen**

Sie können jetzt den Container aus der Registrierung auf einen beliebigen Host ziehen, auf dem Docker-Images ausgeführt werden können. Beispiel: [Azure Container Instances](/azure/container-instances/container-instances-tutorial-deploy-app).