---
title: Mobiel werkgebied voor onkostenbeheer
description: Dit onderwerp biedt informatie over het mobiele werkgebied Onkostenbeheer, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunnen gebruikers een ontvangstbewijs vastleggen en uploaden, zodat zij dit later aan een onkostennota kunnen koppelen. Het mobiele werkgebied stelt gebruikers tevens in staat snel een onkostenregel te maken op basis van een bevoegd ontvangstbewijs.
author: annbe
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: end user, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: annbe
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4e3202de8e5288bbd52e8c28922374de147cc99f
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="expense-management-mobile-workspace"></a>Mobiel werkgebied voor onkostenbeheer

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over het mobiele werkgebied Onkostenbeheer, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunnen gebruikers een ontvangstbewijs vastleggen en uploaden, zodat zij dit later aan een onkostennota kunnen koppelen. Het mobiele werkgebied stelt gebruikers tevens in staat snel een onkostenregel te maken op basis van een bevoegd ontvangstbewijs.

<a name="overview-of-the-expense-management-mobile-workspace"></a>Overzicht van het mobiele werkgebied Onkostenbeheer
---------------------------------------------------

Veel organisaties vereisen dat een kopie van een ontvangstbewijs aan een reisgerelateerde of zakelijke onkostennota wordt gekoppeld die een werknemer indient voor terugbetaling. Het mobiele werkgebied **Onkostenbeheer** stelt gebruikers in staat snel nieuwe onkostenregels te maken op het mobiele apparaat van hun keuze met behulp van een bijgevoegde foto van een ontvangstbewijs. Gebruikers kunnen ook een foto van een ontvangstbewijs maken en deze vervolgens later aan een onkostennota koppelen. Het mobiele werkgebied **Onkostenbeheer** stelt gebruikers met name in staat het volgende te doen:

-   Een foto van een ontvangstbewijs maken en deze uploaden naar Microsoft Dynamics 365 for Operations. Een gebruiker kan vervolgens deze foto later aan een onkostennota koppelen.
-   Een bestand uploaden als een vastgelegd ontvangstbewijs. Een gebruiker kan daarna daty bestand later aan een onkostennota koppelen.
-   Een nieuwe onkostenregel maken met behulp van een bijgevoegd ontvangstbewijs. Een gebruiker kan vervolgens later het regelartikel toevoegen aan een onkostennota en deze indienen voor goedkeuring en terugbetaling.

In de overige secties van dit onderwerp wordt uitgelegd hoe het mobiele werkgebied **Onkostenbeheer** moet worden geïmplementeerd en gebruikt.

## <a name="prerequisites"></a>Vereisten
Voordat u het mobiele werkgebied **Onkostenbeheer** kunt gebruiken, controleert u of de systeembeheerder de volgende vereisten heeft geregeld.

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
<td>Als u Dynamics 365 for Operations nog niet hebt geïmplementeerd in uw organisatie, dient uw systeembeheerder <a href="/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Een Microsoft Dynamics 365 for Operations demo-omgeving implementeren</a> te raadplegen.</td>
</tr>
<tr class="even">
<td>KB 4019015 moet worden geïmplementeerd.</td>
<td>Systeembeheerder</td>
<td>KB 4019015 (een X++-update of metagegevenshotfix) bevat vier mobiele werkgebieden voor supply chain management. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4019015:
<ol>
<li>Download KB 4019015 van Microsoft Dynamics Lifecycle Services (LCS).</li>
<li><a href="/dynamics365/operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">De metagegevenshotfix installeren</a>.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Een implementeerbaar pakket maken</a> dat de <strong>ApplicationSuite</strong> en <strong>ExpenseMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Pas het implementeerbare pakket toe</a> op uw Microsoft Dynamics 365 for Operations-systeem.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Het mobiele werkgebied <strong>Onkostenbeheer</strong> moet worden gepubliceerd naar de mobiele app voor Dynamics 365 for Operations.</td>
<td>Systeembeheerder</td>
<td><ol>
<li>Start Dynamics 365 for Operations in uw browser.</li>
<li>Selecteer op de pagina <strong>Systeemparameters</strong> de optie <strong>Mobiele werkgebieden beheren</strong>.</li>
<li>Selecteer het werkgebied <strong>Onkostenbeheer</strong>.</li>
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
5.  Nadat u zich hebt aangemeld, ziet u de beschikbare werkgebieden voor uw bedrijf. Houd er rekening mee dat als uw systeembeheerder een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden kunt opvragen om te vernieuwen. 

[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Een ontvangstbewijs vastleggen met behulp van het mobiele werkgebied Onkostenbeheer
1.  Selecteer op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2.  Selecteer **Ontvangstbewijs vastleggen**.
3.  Selecteer **Foto maken** of **Afbeelding kiezen**.
4.  Als u **Foto maken** hebt geselecteerd, gaat u als volgt te werk:
    1.  U gaat naar de camera op uw mobiele apparaat, zodat u een foto van het ontvangstbewijs kunt maken. Wanneer u klaar bent met het maken van een foto, klikt u op **OK** om de foto te accepteren.
    2.  Optioneel: voer een naam in voor de foto en voer eventuele notities in.

     **Of:**  volg deze stappen als u **Afbeelding kiezen** hebt geselecteerd:
    1.  Selecteer een afbeelding in de lijst.
    2.  Optioneel: voer een naam in voor de afbeelding en voer eventuele notities in.

5.  Selecteer **Gereed**.

## <a name="quick-expense-entry-by-using-the-expense-management-mobile-workspace"></a>Snelle invoer van onkosten met behulp van het mobiele werkgebied Onkostenbeheer
1.  Selecteer op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2.  Selecteer **Snelle onkosteninvoer**.
3.  Selecteer de categorie voor de onkostenpost. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden maximaal 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) raadplegen. Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
4.  Voer de transactiedatum van de onkostenpost in.
5.  Optioneel: voer de verkoper voor de onkostenpost in.
6.  Voer het bedrag van de onkostenpost in.
7.  Selecteer de valuta van de onkostenpost. U ziet een lijst van de valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden maximaal 400 valuta's geladen, maar een ontwikkelaar kan dit aantal wijzigen. Voor meer informatie moeten ontwikkelaars [Mobiel platform van Dynamics 365 for Operations](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform) raadplegen. Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om een online zoekopdracht in Dynamics 365 for Operations uit te voeren. Zoek op valuta of schakel over naar zoeken op naam.
8.  Selecteer **Foto maken** of **Afbeelding kiezen**.
9.  Als u **Foto maken** hebt geselecteerd, gaat u naar de camera op uw mobiele apparaat, zodat u een foto van het ontvangstbewijs kunt maken. Wanneer u klaar bent met het maken van een foto, klikt u op **OK** om de foto te accepteren.  Of als u **Afbeelding kiezen** hebt geselecteerd, selecteert u een afbeelding in de lijst.
10. Selecteer **Gereed**.






