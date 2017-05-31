---
title: Mobiel werkgebied voor verkooporders
description: Dit onderwerp biedt informatie over het mobiele werkgebied Verkooporders, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunt u overal en altijd op de hoogte blijven van uw verkooporders.
author: YuyuScheller
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 11898146a13756a6bb22a769e37e8773484e0d04
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="sales-orders-mobile-workspace"></a>Mobiel werkgebied voor verkooporders

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over het mobiele werkgebied Verkooporders, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunt u overal en altijd op de hoogte blijven van uw verkooporders. 

<a name="overview-of-the-sales-orders-mobile-workspace"></a>Overzicht van het mobiele werkgebied Verkooporders
---------------------------------------------

Het mobiele werkgebied **Verkooporders** heeft toegang tot Microsoft Dynamics 365 for Operations en stelt u in staat gedetailleerde informatie weer te geven over elke verkooporder. Deze informatie omvat de status van de order, contactgegevens voor de klant en contactgegevens voor degene die de order aanneemt. Het mobiele werkgebied **Verkooporders** geeft een direct overzicht van verkooporders. U kunt alle verkooporders weergeven, verkooporders per klant weergeven of informatie weergeven over een specifieke verkooporder. 

Het mobiele werkgebied bevat twee weergaven waarmee u verkooporders grondig kunt analyseren.

### <a name="view-all-sales-orders"></a>Alle verkooporders weergeven

In deze weergave geeft een overzicht van alle verkooporders.

-   Gebruik een van de volgende filters om de verkooporders te selecteren die u wilt weergeven:
    -   Zoeken op verkooporder
    -   Zoeken op klantaccount
    -   Zoeken op klantnaam
    -   Zoeken op status
    -   Zoeken op vrijgavestatus
    -   Zoeken op aanmaakdatum en -tijd
    
-   Nadat u de verkooporders hebt geselecteerd, kunt u de details van specifieke orders weergeven. U kunt met name de volgende gegevens bekijken:
    -   Klantnaam en adresgegevens
    -   Verschillende datums voor de verkooporder, zoals de gewenste verzenddatum en de bevestigde verzenddatum
    -   Contactgegevens voor de ordermedewerker
    -   Contactgegevens van de klant
    -   Orderregels
    -   Zendingen die tonen hoe en wanneer een verkooporder is verzonden

### <a name="view-orders-for-a-customer"></a>Orders voor een klant weergeven

In deze weergave ziet u een overzicht van de verkooporders per klant.

-   Gebruik een van de volgende filters om orders voor een klant weer te geven:
    -   Zoeken op naam
    -   Zoeken op account

-   Nadat u een klant hebt geselecteerd, kunt u de volgende informatie weergeven:
    -   Naam en groep van klant
    -   Contactgegevens van de klant
    -   Verkooporders van de klant en gegevens van deze verkooporders:
        -   Klantnaam en adresgegevens
        -   Verschillende verkooporderdatums
        -   Contactgegevens voor de ordermedewerker
        -   Contactgegevens van de klant
        -   Orderregels
        -   Zendingen die tonen hoe en wanneer een verkooporder is verzonden

## <a name="prerequisites"></a>Vereisten
Voordat u het mobiele werkgebied **Verkooporders** kunt gebruiken, controleert u of de systeembeheerder de volgende vereisten heeft geregeld.

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
<td>Dynamics 365 for Operations versie 1611 met platformupdate 3 of hoger moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>Als u Dynamics 365 for Operations nog niet hebt geïmplementeerd in uw organisatie, dient de systeembeheerder <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment/">Een Microsoft Dynamics 365 for Operations demo-omgeving implementeren</a> te raadplegen.</td>
</tr>
<tr class="even">
<td>KB 4013633 moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>KB 4013633 (een X++-update of metagegevenshotfix) bevat vier mobiele werkgebieden voor supply chain management. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633:
<ol>
<li>KB 4013633 downloaden van Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">De metagegevenshotfix installeren</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a> op uw Microsoft Dynamics 365 for Operations-systeem.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het mobiele werkgebied <strong>Verkooporders</strong> moet worden gepubliceerd naar de mobiele app voor Dynamics 365 for Operations.</td>
<td>Systeembeheerder</td>
<td><ol>
<li>Start Dynamics 365 for Operations in uw browser.</li>
<li>Selecteer op de pagina <strong>Systeemparameters</strong> de optie <strong>Mobiele werkgebieden beheren</strong>.</li>
<li>Selecteer het werkgebied <strong>Verkooporders</strong>.</li>
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

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-mobile-workspace"></a>Informatie over verkooporders voor een klant weergeven met behulp van het mobiele werkgebied
1.  Selecteer op uw mobiele apparaat het werkgebied **Verkooporders**.
2.  Selecteer **Orders voor een klant weergeven**.
3.  Gebruik rekening- of klantnaamgegevens om de klant te zoeken.
4.  Selecteer de gewenste klant.
5.  Selecteer **Contactgegevens** of **Verkooporders**. Als u **Verkooporders** selecteert, wordt een lijst met verkooporders voor de klant weergegeven.
6.  Selecteer **Verkooporders**. U kunt nu informatie over de verkooporderregels, informatie over verzendingen, contactgegevens voor de klant en contactgegevens voor de ordermedewerker weergeven.





