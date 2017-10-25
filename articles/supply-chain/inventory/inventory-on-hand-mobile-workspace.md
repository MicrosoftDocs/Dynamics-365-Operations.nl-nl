---
title: Mobiel werkgebied voorhanden voorraad
description: Dit onderwerp biedt informatie over het mobiele werkgebied Voorhanden voorraad. Met dit mobiele werkgebied kunt u altijd en overal mobiele inzichten verkrijgen in gereserveerde en beschikbare voorraad.
author: Mirzaab
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 04d459a2fd0fdf9c201d9e96b37234846eb9ccf0
ms.openlocfilehash: 1029b9f041f318577779658650e07d8377823fea
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobiel werkgebied voorhanden voorraad

[!include[banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Voorhanden voorraad**. Met dit mobiele werkgebied kunt u altijd en overal inzichten verkrijgen in gereserveerde en beschikbare voorraad.

Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations.

## <a name="overview"></a>Overzicht
Normaal gesproken hebben bedrijven elke dag meerdere verzendingen en meerdere ontvangsten van voorraad. Deze verplaatsingen veranderen voortdurend de status van de voorhanden voorraad. Met het mobiele werkgebied **Voorhanden voorraad** kunt u de status van de voorhanden voorraad voor meerdere bedrijven bekijken, zodat u de meest recente inzichten in de voorraadgegevens op het mobiele apparaat van uw keuze kunt verkrijgen. Ongeacht of u werkzaam bent in het magazijn of voor inkoop, verkoop, productie of beheer of andere rollen vervult, u hebt altijd en overal toegang tot de gegevens over de voorhanden voorraad. 

Het mobiele werkgebied is een duidelijk overzicht van de voorhanden status over faciliteiten beschikken. U kunt voorhanden voorraad weergeven in faciliteiten, huidige materiaalreserveringen en niet-gereserveerde voorhanden voorraad. U kunt ook artikelnummers invoeren om te zoeken in voorhanden voorraad en een gefilterde zoekopdracht uitvoeren naar voorhanden producten of varianten. 

Het mobiele werkgebied biedt vooral de volgende functies:

-   U kunt zoeken op productnummer of productnaam om producten te vinden waarvoor u de status van de voorhanden voorraad wilt weergeven.
-   Voor de geselecteerde producten kunt u de volgende informatie weergeven:

    -   Voorhanden voorraad per vestiging
    -   Voorhanden voorraad per magazijn
    -   Voorhanden voorraad per locatie
    -   Voorhanden voorraad per batch (voor batchproducten)
    -   Voorhanden voorraad per voorraadstatus
    
-   Voorhanden voorraad van producten wordt weergegeven op de volgende manieren:

    -   Op basis van fysieke voorraad (deze weergave geeft de totale hoeveelheid.)
    -   Op basis van fysieke gereserveerde voorraad (deze weergave geeft de gereserveerde hoeveelheid.)
    -   Op basis van fysieke beschikbare voorraad (deze weergave geeft de beschikbare hoeveelheid waarvoor geen reserveringen zijn.)

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Vereisten als u Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) gebruikt 
Als Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Voorhanden voorraad** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Vereisten als u Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger gebruikt.
Als Microsoft Dynamics 365 for Operations, versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder aan de volgende vereisten voldoen. 

<table>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>KB 4013633 implementeren.</td>
<td>Systeembeheerder</td>

<td>KB 4013633 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Voorhanden voorraad</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">De metagegevenshotfix van Microsoft Dynamics Lifecycle Services (LCS) downloaden</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Het mobiele werkgebied <strong>Voorhanden voorraad</strong> publiceren.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Dynamics 365 for Unified Operations:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app

1.  Start de app op uw mobiele apparaat.
2.  Voer uw Dynamics 365-URL in.
3.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
4.  Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

    [![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-on-hand-inventory-for-a-product-by-using-the-inventory-on-hand-mobile-workspace"></a>De voorhanden voorraad weergeven voor een product met behulp van het mobiele werkgebied Voorhanden voorraad

1.  Selecteer op uw mobiele apparaat het werkgebied **Voorhanden voorraad**.

2.  Selecteer **Voorhanden voorraad voor een artikel controleren**. U ziet een lijst van de producten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).
3.  Als uw item niet in de lijst staat, selecteert u **Meer zoeken**. Zoek op productnummer of schakel over naar een zoekopdracht op productnaam.

4.  Selecteer een product. Als het artikel een afbeelding heeft, wordt de afbeelding weergegeven.
5.  Selecteer een van de volgende opties om de status van de voorhanden voorraad weer te geven:

    -   Voorhanden voorraad per vestiging weergeven
    -   Voorhanden voorraad per magazijn weergeven
    -   Voorhanden voorraad per locatie weergeven
    -   Voorhanden voorraad per batch (voor batchproducten) weergeven
    -   Voorhanden voorraad per voorraadstatus weergeven

    Voorhanden voorraad van producten wordt weergegeven op de volgende manieren:
    -   Op basis van fysieke voorraad (deze weergave geeft de totale hoeveelheid.)
    -   Op basis van fysieke gereserveerde voorraad (deze weergave geeft de gereserveerde hoeveelheid.)
    -   Op basis van beschikbare fysieke voorraad (deze weergave geeft de beschikbare hoeveelheid waarvoor geen reserveringen zijn.)
