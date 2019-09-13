---
title: Gids voor het oplossen van problemen met gegevensintegratie
description: Dit onderwerp bevat informatie voor het oplossen van problemen met gegevensintegratie tussen Microsoft Dynamics 365 for Finance and Operations en Common Data Service.
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
ms.openlocfilehash: 5e71729dafd2ad85a01b055363d1c7056b5558b2
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873100"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Gids voor het oplossen van problemen met gegevensintegratie

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Schakel logboeken voor invoegtoepassing traceren in Common Data Service in en controleer de foutgegevens met betrekking tot de invoegtoepassing voor Twee keer wegschrijven

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Als er een probleem of fout optreedt tijdens de synchronisatie van twee keer wegschrijven, voert u de volgende stappen uit om de fouten in het traceerlogboek te controleren.

1. Voordat u de fouten kunt inspecteren, moet u traceerlogboeken voor invoegtoepassingen inschakelen. Zie voor instructies de sectie "Traceerlogboek weergeven" in de [Zelfstudie: een invoegtoepassing schrijven en registreren](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Nu kunt u de fouten inspecteren.

2. Meld u aan bij Microsoft Dynamics 365 for Sales.
3. Selecteer de knop **Instellingen** (het tandwielsymbool) en selecteer **Geavanceerde instellingen**.
4. Kies in het menu **Instellingen** de optie **Aanpassen \> Traceerlogboek invoegtoepassing**.
5. Selecteer de typenaam **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin** om de foutdetails weer te geven.

## <a name="inspect-dual-write-synchronization-errors-in-finance-and-operations"></a>De synchronisatiefouten voor Twee keer wegschrijven inspecteren in Finance and Operations

Volg deze stappen om fouten tijdens het testen te controleren.

1. Meld u aan bij Microsoft Dynamics LCS (LifeCycle Services).
2. Open het LCS-project waarvoor u tests met twee keer wegschrijven wilt uitvoeren.
3. Selecteer **Cloudomgevingen**.
4. Maak een verbinding van een extern bureaublad met de Dynamics 365 for Finance and Operations virtuele machine (VM) door gebruik te maken van een lokaal account in LCS.
5. Open Logboeken. 
6. Ga naar **Logboeken Toepassingen en Services \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operationeel**. De fouten en details worden weergegeven.

## <a name="unlink-one-common-data-service-environment-from-finance-and-operations-and-link-another-environment"></a>Een Common Data Service-omgeving (los)koppelen vanuit Finance and Operations

Voer de volgende stappen uit om de koppelingen bij te werken.

1. Ga naar de Finance and Operations-omgeving.
2. Open Gegevensbeheer.
3. Selecteer **Koppeling naar CDS for Apps**.
4. Selecteer alle toewijzingen die worden uitgevoerd en selecteer **Stoppen**.
5. Selecteer alle toewijzingen en selecteer vervolgens **Verwijderen**.

    > [!NOTE]
    > De optie **Verwijderen** is niet beschikbaar als de sjabloon **CustomerV3-account** is geselecteerd. Maak de selectie van deze sjabloon waar nodig leeg. **CustomerV3-account** is een oudere ingerichte sjabloon en werkt met de oplossing Prospect naar contant geld. Omdat deze wereldwijd is vrijgegeven, wordt deze weergegeven onder alle sjablonen.

6. Selecteer **Koppeling met omgeving verbreken**.
7. Selecteer **Ja** om de bewerking te bevestigen.
8. Volg de stappen in de [installatiehandleiding](https://aka.ms/dualwrite-docs) om de nieuwe omgeving te koppelen.
