---
title: Mobiel werkgebied voor verkooporders
description: Dit onderwerp biedt informatie over het mobiele werkgebied Verkooporders. Via dit werkgebied kunt u overal en altijd op de hoogte blijven van uw verkooporders.
author: Mirzaab
manager: tfehr
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267134
ms.assetid: 0ce96511-002b-4de7-b31e-4303f94edc84
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: dbd364978f2d204dafc25e14c55073fe2591b82f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974955"
---
# <a name="sales-orders-mobile-workspace"></a>Mobiel werkgebied voor verkooporders

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het mobiele werkgebied **Verkooporders**. Via dit werkgebied kunt u overal en altijd op de hoogte blijven van uw verkooporders. 

Dit mobiele werkgebied is bedoeld om samen te worden gebruikt met de mobiele app van Finance and Operations.

## <a name="overview"></a>Overzicht
In het mobiele werkgebied **Verkooporders** kunt u gedetailleerde informatie over elke verkooporder weergeven. Deze informatie omvat de status van de order, contactgegevens voor de klant en contactgegevens voor degene die de order aanneemt. Het mobiele werkgebied **Verkooporders** geeft een direct overzicht van verkooporders. U kunt alle verkooporders weergeven, verkooporders per klant weergeven of informatie weergeven over een specifieke verkooporder. 

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
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-supply-chain-management"></a>Vereisten als u Supply Chain Management gebruikt 
Als Sales naar Supply Chain Management is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Verkooporders** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a>Vereisten als u versie Dynamics 365 for Operations 1611 met platformupdate 3 of hoger gebruikt
Als Dynamics 365 for Operations versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren. 

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

<td>KB 4013633 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Verkooporders</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metagegevens-hotfix downloaden uit  Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Het mobiele werkgebied <strong>Verkooporders</strong> publiceren.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren
Download en installeer de mobiele Finance and Operations-app:

-   [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
-   [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app

1.  Start de app op uw mobiele apparaat.
2.  Voer uw Dynamics 365-URL in.
3.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
4.  Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.

[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-information-about-sales-orders-for-a-customer-by-using-the-sales-order-mobile-workspace"></a>Informatie over verkooporders voor een klant weergeven met het mobiele werkgebied Verkooporders

1.  Selecteer op uw mobiele apparaat het werkgebied **Verkooporders**.
2.  Selecteer **Orders voor een klant weergeven**.
3.  Gebruik rekening- of klantnaamgegevens om de klant te zoeken.
4.  Selecteer de gewenste klant.
5.  Selecteer **Contactgegevens** of **Verkooporders**. Als u **Verkooporders** selecteert, wordt een lijst met verkooporders voor de klant weergegeven.
6.  Selecteer **Verkooporders**. U kunt nu informatie over de verkooporderregels, informatie over verzendingen, contactgegevens voor de klant en contactgegevens voor de ordermedewerker weergeven.
