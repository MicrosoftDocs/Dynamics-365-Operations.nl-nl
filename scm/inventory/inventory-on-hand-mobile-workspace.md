---
title: Mobiel werkgebied voorhanden voorraad
description: Dit onderwerp biedt informatie over het mobiele werkgebied Voorhanden voorraad, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Met dit mobiele werkgebied kunt u altijd en overal mobiele inzichten verkrijgen in gereserveerde en beschikbare voorraad.
author: YuyuScheller
manager: AnnBe
ms.date: 04/21/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267094
ms.assetid: 3fa385ba-894d-4a9e-b394-ef3697abf895
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e703ae80800b993ebca1c7bee455af1be41c7d5f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="inventory-on-hand-mobile-workspace"></a>Mobiel werkgebied voorhanden voorraad

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over het mobiele werkgebied Voorhanden voorraad, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Met dit mobiele werkgebied kunt u altijd en overal mobiele inzichten verkrijgen in gereserveerde en beschikbare voorraad.

<a name="overview-of-the-inventory-on-hand-mobile-workspace"></a>Overzicht van mobiel werkgebied voorhanden voorraad
--------------------------------------------------

Normaal gesproken hebben bedrijven elke dag meerdere verzendingen en meerdere ontvangsten van voorraad. Deze verplaatsingen veranderen voortdurend de status van de voorhanden voorraad. Met het mobiele werkgebied **Voorhanden voorraad** kunt u de status van de voorhanden voorraad voor meerdere bedrijven bekijken, zodat u de meest recente inzichten in de voorraadgegevens op het mobiele apparaat van uw keuze kunt verkrijgen. Ongeacht of u werkzaam bent in het magazijn of voor inkoop, verkoop, productie of beheer of andere rollen vervult, u hebt altijd en overal toegang tot de gegevens over de voorhanden voorraad. Het mobiele werkgebied is een duidelijk overzicht van de voorhanden status over faciliteiten beschikken. U kunt voorhanden voorraad weergeven in faciliteiten, huidige materiaalreserveringen en niet-gereserveerde voorhanden voorraad. U kunt ook artikelnummers invoeren om te zoeken in voorhanden voorraad en een gefilterde zoekopdracht uitvoeren naar voorhanden producten of varianten. Het mobiele werkgebied biedt vooral de volgende functies:

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
Voordat u het mobiele werkgebied **Voorhanden voorraad** kunt gebruiken, controleert u of de systeembeheerder de volgende vereisten heeft geregeld.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Rol</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 for Operations versie 1611 met platformupdate 3 of hoger moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>Als u Dynamics 365 for Operations nog niet hebt geïmplementeerd in uw organisatie, dient de systeembeheerder <a href="http://ax.help.dynamics.com/en/wiki/deploy-an-ax7-demo-environment/">Een Microsoft Dynamics 365 for Operations demo-omgeving implementeren</a> te raadplegen.</td>
</tr>
<tr class="even">
<td>KB 4013633 moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>KB 4013633 (een X++-update of metagegevenshotfix) bevat vier mobiele werkgebieden voor supply chain management. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633:
<ol>
<li>KB 4013633 downloaden van Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/configuring-and-installing-a-metadata-hotfix-package/">De metagegevenshotfix installeren</a>.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/create-and-apply-a-deployable-package/">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="https://ax.help.dynamics.com/en/wiki/apply-a-deployable-package-on-a-dynamics-ax-system/">Pas het implementeerbare pakket toe</a> op uw Microsoft Dynamics 365 for Operations-systeem.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het mobiele werkgebied <strong>Voorhanden voorraad</strong> moet worden gepubliceerd naar de mobiele app voor Dynamics 365 for Operations.</td>
<td>Systeembeheerder</td>
<td><ol>
<li>Start Dynamics 365 for Operations in uw browser.</li>
<li>Selecteer op de pagina <strong>Systeemparameters</strong> de optie <strong>Mobiele werkgebieden beheren</strong>.</li>
<li>Selecteer het werkgebied <strong>Voorhanden voorraad</strong>.</li>
<li>Klik op <strong>Mobiel werkgebied publiceren</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>De mobiele app voor Dynamics 365 for Operations downloaden en installeren
Download en installeer de mobiele app van Microsoft Dynamics 365 for Operations vanuit uw store voor mobiele apps.

-   Voor Android: [Dynamics 365 for Operations in de Google Play Store](https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile)
-   Voor iPhone: [Dynamics 365 for Operations in de iTunes apps store](https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8)

## <a name="sign-in-to-the-dynamics-365-for-operations-mobile-app"></a>Meld u aan bij de mobiele app voor Dynamics 365 for Operations
1.  Start de app op uw mobiele apparaat.
2.  Voer uw Dynamics 365 for Operations-URL in.
3.  Voer het bedrijf in waarbij u zich wilt aanmelden. Voer bijvoorbeeld **USMF** in.
4.  De eerste keer dat u zich aanmeldt, wordt u gevraagd om de gebruikersnaam en het wachtwoord voor uw Dynamics 365 for Operations-account. Voer uw referenties in.
5.  Nadat u zich hebt aangemeld, ziet u de beschikbare werkgebieden voor uw bedrijf. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden kunt opvragen om te vernieuwen. 

    [![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-the-onhand-inventory-for-a-product-by-using-the-inventory-onhand-mobile-workspace"></a>De voorhanden voorraad weergeven voor een product met behulp van het mobiele werkgebied voor voorhanden voorraad
1.  Selecteer op uw mobiele apparaat het werkgebied **Voorhanden voorraad**.
2.  Selecteer **Voorhanden voorraad voor een artikel controleren**. U ziet een lijst van de producten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](http://ax.help.dynamics.com/en/wiki/mobile-development-handbook/) raadplegen.
3.  Als uw artikel niet in de lijst staat, selecteert u **Meer zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op productnummer of schakel over naar een zoekopdracht op productnaam.
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






