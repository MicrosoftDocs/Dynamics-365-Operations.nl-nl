---
title: Gids voor het oplossen van problemen met gegevensintegratie
description: Dit onderwerp bevat informatie over het oplossen van problemen met gegevensintegratie tussen Microsoft Dynamics 365 for Finance and Operations en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca62a6b3aa64ec2383ee3ded3b7bbf4650a41166
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797270"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Gids voor het oplossen van problemen met gegevensintegratie

## <a name="enable-plugin-trace-in-common-data-service-and-check-the-dual-write-plugin-error-details"></a>Schakel Plug-in traceren in Common Data Service in en controleer de foutgegevens met betrekking tot de invoegtoepassing voor Twee keer wegschrijven

Als er zich een probleem of fout voordoet met de synchronisatie van Twee keer wegschrijven, kunt u de fouten in het traceerlogboek controleren:

1. Voordat u de fouten kunt inspecteren, moet u Plug-in traceren inschakelen met behulp van de instructies in [Plug-in registreren](https://docs.microsoft.com/en-us/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs). Nu kunt u de fouten inspecteren.
2. Meld u aan bij Dynamics 365 for Sales.
3. Klik op het pictogram Instellingen (een tandwiel) en selecteer **Geavanceerde instellingen**.
4. Kies in het menu **Instellingen** de optie **Aanpassen > Traceerlogboek plug-in**.
5. Klik op de typenaam **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** om de foutdetails weer te geven.

## <a name="check-dual-write-synchronization-errors-in-finance-and-operations"></a>De synchronisatiefouten voor Twee keer wegschrijven controleren in Finance and Operations

U kunt de fouten tijdens het testen controleren met behulp van de volgende stappen:

+ Meld u aan bij LCS (LifeCycle Services).
+ Open het LCS-project dat u hebt gekozen om tests met twee keer wegschrijven uit te voeren.
+ Ga naar Cloudomgevingen.
+ VM voor extern bureaublad naar Finance and Operations met lokaal account dat wordt weergegeven in LCS.
+ Open Logboeken. 
+ Navigeer naar **Logboeken Toepassingen en Services > Microsoft > Dynamics > AX-DualWriteSync > Operationeel**. De fouten en details worden weergegeven.

## <a name="how-to-unlink-and-link-another-common-data-service-environment-from-finance-and-operations"></a>Een andere Common Data Service-omgeving (los)koppelen vanuit Finance and Operations

U kunt koppelingen bijwerken door de volgende stappen uit te voeren:

+ Navigeer naar de Finance and Operations-omgeving.
+ Open Gegevensbeheer.
+ Klik op **Koppeling naar CDS for Apps**.
+ Selecteer alle actieve toewijzingen en klik op **Stoppen**. 
+ Selecteer alle toewijzingen en klik op **Verwijderen**.

    > [!NOTE]
    > De optie **Verwijderen** wordt niet weergegeven als de sjabloon **CustomerV3-account** is geselecteerd. Hef de selectie zo nodig op. **CustomerV3-account** is een oudere ingerichte sjabloon en werkt met de oplossing Prospect naar contant geld. Omdat deze wereldwijd is vrijgegeven, wordt deze weergegeven onder alle sjablonen.

+ Klik op **Koppeling met omgeving verbreken**.
+ Klik ter bevestiging op **Ja**.
+ Volg de stappen in de [installatiehandleiding](https://aka.ms/dualwrite-docs) om de nieuwe omgeving te koppelen.

