---
title: Mobiel werkgebied voor onkostenbeheer
description: Dit onderwerp biedt informatie over het mobiele werkgebied voor Onkostenbeheer. Via dit werkgebied kunnen gebruikers een ontvangstbewijs vastleggen en uploaden, zodat zij dit later aan een onkostennota kunnen koppelen. Gebruikers kunnen ook snel een onkostenregel maken met behulp van een bijgevoegd ontvangstbewijs en hun onkostennota's beheren.
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 69eeb90387ca5765c163c7d482295ea104cc078c
ms.openlocfilehash: 7ce4c9d13a8686c82af8acad39d68858e52ba520
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="expense-management-mobile-workspace"></a>Mobiel werkgebied voor onkostenbeheer

[!include[banner](../includes/banner.md)]

Dit onderwerp bevat informatie over het mobiele werkgebied voor **Onkostenbeheer**. Via dit werkgebied kunnen gebruikers een ontvangstbewijs vastleggen en uploaden, zodat zij dit later aan een onkostennota kunnen koppelen. Gebruikers kunnen ook snel een onkostenregel maken met behulp van een bijgevoegd ontvangstbewijs en hun onkostennota's beheren. Fiatteurs kunnen bovendien het mobiele werkgebied **Onkostenbeheer** gebruiken voor het weergeven van onkostenrapporten die aan hen zijn toegewezen, en deze goedkeuren of afwijzen.


Dit mobiele werkgebied is bedoeld om te worden gebruikt met de mobiele app Microsoft Dynamics 365 for Unified Operations.


## <a name="overview"></a>Overzicht

Veel organisaties vereisen dat een kopie van een ontvangstbewijs aan een reisgerelateerde of zakelijke onkostennota wordt gekoppeld die een werknemer indient voor terugbetaling. Het mobiele werkgebied **Onkostenbeheer** stelt gebruikers in staat snel nieuwe onkostenregels te maken op het mobiele apparaat van hun keuze met behulp van een bijgevoegde foto van een ontvangstbewijs. Gebruikers kunnen ook een foto van een ontvangstbewijs maken en deze vervolgens later aan een onkostennota koppelen. Werknemers kunnen ook onkostennota's maken en beheren en deze vervolgens ter goedkeuring en terugbetaling indienen via hun mobiele apparaat.


Gebruikers kunnen met het mobiele werkgebied **Onkostenbeheer** de volgende taken uitvoeren:

- Een foto maken van een ontvangstbewijs en deze uploaden naar Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. U kunt vervolgens deze foto later aan een onkostennota koppelen.
- Een bestand uploaden als een vastgelegd ontvangstbewijs. U kunt vervolgens dat bestand later aan een onkostennota koppelen.
- Een nieuwe onkostenregel maken met behulp van een bijgevoegd ontvangstbewijs. U kunt vervolgens later het regelartikel toevoegen aan een onkostennota en deze indienen voor goedkeuring en terugbetaling.

Als u werkt met Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017), kunt u ook deze functies gebruiken:

- Een nieuwe onkostennota maken.
- Creditcardtransacties en overige eerder gemaakte kosten koppelen aan een onkostennota.
- Nieuwe onkosten maken voor een onkostennota.
- Een ontvangstbewijs koppelen aan alle onkosten voor een onkostennota door middel van een foto van het ontvangstbewijs of door het uploaden van een bestand met een vastgelegd ontvangstbewijs.
- Afhankelijk van het onkostenbeleid van het bedrijf de lijst met gasten aan een onkostenpost toevoegen.
- Afhankelijk van het onkostenbeleid van het bedrijf de uitgaven specificeren.
- Een onkostennota indienen ter goedkeuring en vergoeding.
- Goedkeuren of afwijzen van onkostennota's waaraan u bent toegewezen als fiatteur.

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Vereisten als u Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) gebruikt 
Als Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Onkostenbeheer** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

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
<td>KB 4019015 implementeren.</td>
<td>Systeembeheerder</td>
<td>KB 4019015 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Onkostenbeheer</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4019015.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">De metagegevenshotfix van Microsoft Dynamics Lifecycle Services (LCS) downloaden</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de <strong>ApplicationSuite</strong> en <strong>ExpenseMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>
</ol></td>
</tr>
<tr class="even">
<td>Mobiel werkgebied voor <strong>Onkostenbeheer</strong> publiceren.</td>
<td>Systeembeheerder</td>
<td>Zie <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Mobiel werkgebied publiceren</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>De mobiele app voor Dynamics 365 for Operations downloaden en installeren
Download en installeer de mobiele app Dynamics 365 for Unified Operations:

- [Voor Android-telefoons](https://go.microsoft.com/fwlink/?linkid=850662)
- [Voor iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Aanmelden bij de mobiele app
1. Start de app op uw mobiele apparaat.
2. Voer uw Dynamics 365-URL in.
4. De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.
5. Nadat u zich hebt aangemeld, worden de beschikbare werkgebieden voor uw bedrijf weergegeven. Houd er rekening mee dat als uw systeembeheerder later een nieuw werkgebied publiceert, u de lijst met mobiele werkgebieden moet vernieuwen.


[![Opvragen om te vernieuwen](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Een ontvangstbewijs vastleggen met behulp van het mobiele werkgebied Onkostenbeheer

1. Open op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2. Selecteer **Ontvangstbewijs vastleggen**.
3. Selecteer **Foto maken** of **Afbeelding kiezen**.
4. Volg één van deze stappen:

    - Als u **Foto maken** hebt geselecteerd, gaat u als volgt te werk:

        1. U gaat naar de camera op uw mobiele apparaat, zodat u een foto van het ontvangstbewijs kunt maken. Wanneer u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
        2. Optioneel: voer een naam in voor de foto en voer eventuele notities in.

    - Volg deze stappen als u **Afbeelding kiezen** hebt geselecteerd:

        1. Selecteer een afbeelding in de lijst.
        2. Optioneel: voer een naam in voor de afbeelding en voer eventuele notities in.

5. Selecteer **Gereed**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Snelle invoer van onkosten met behulp van het mobiele werkgebied Onkostenbeheer
1. Open op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2. Selecteer **Snelle onkosteninvoer**.
3. Selecteer de categorie voor de onkostenpost. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
4. Voer de transactiedatum van de onkostenpost in.
5. Optioneel: voer de verkoper voor de onkostenpost in.
6. Voer het bedrag van de onkostenpost in.
7. Selecteer de valuta van de onkostenpost. U ziet een lijst van de valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta's geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
8. Selecteer **Foto maken** of **Afbeelding kiezen**.
9. Volg één van deze stappen:

    - Als u **Foto maken** hebt geselecteerd, gaat u naar de camera op uw mobiele apparaat, zodat u een foto van het ontvangstbewijs kunt maken. Wanneer u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
    - Als u **Afbeelding kiezen** hebt geselecteerd, selecteert u een afbeelding in de lijst.

10. Selecteer **Gereed**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Een onkostennota goedkeuren met behulp van het mobiele werkgebied Onkostenbeheer (update van juli 2017)
1. Open op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2. **Goedkeuringen van onkosten** bevat het aantal onkostennota's dat ter goedkeuring aan u is toegewezen. Het aantal wordt ongeveer elke 30 minuten bijgewerkt. Selecteer **Goedkeuringen van onkosten**.

    De lijst bevat de onkostennota's die ter goedkeuring aan u zijn toegewezen.
    
3. Selecteer een onkostennota om de onkostendetails weer te geven.
4. Selecteer een kostenpost om de details weer te geven. De informatie die wordt weergegeven voor een kostenpost bevat details over het ontvangstbewijs, gasten en een specificatie.
5. Terug op de pagina **Onkostennota** kiest u of u de onkostennota goedkeurt of afwijst.
6. Voer opmerkingen in voor de goedkeuringsactie.
7. Selecteer **Gereed**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Een nieuw onkostennota maken en ter goedkeuring indien met het mobiele werkgebied Onkostenbeheer (update van juli 2017)
1. Open op uw mobiele apparaat het werkgebied **Onkostenbeheer**.
2. Selecteer **Onkosteninvoer**.
3. Selecteer **Nieuw rapport** of selecteer een bestaande onkostennota in de lijst.
4. Geef voor nieuwe onkostennota's het doel en aanvullende informatie op. Deze informatie is afhankelijk van de manier waarop Onkostenbeheer is geconfigureerd voor uw bedrijf.
5. Selecteer **Gereed**.
6. Selecteer **Koppelen** om bestaande onkosten, zoals creditcardtransacties, toe te voegen aan de onkostennota.
7. Selecteer een of meer kostenposten in de lijst.
8. Selecteer **Gereed**.
9. Selecteer **Nieuwe onkosten** als u een nieuwe kostenpost wilt toevoegen aan de onkostennota.
10. Selecteer de categorie voor de onkostenpost. U ziet een lijst van onkostencategorieën die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw categorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op onkostencategorie of schakel over naar zoeken op onkostentype.
11. Optioneel: voer de verkoper voor de onkostenpost in.
12. Voer de transactiedatum van de onkostenpost in.
13. Voer het bedrag van de onkostenpost in.
14. Selecteer de valuta van de onkostenpost. U ziet een lijst van de valutacodes die in uw app zijn geladen voor offline gebruik. Standaard worden 400 valuta's geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw valuta niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op valuta of schakel over naar zoeken op naam.
15. Selecteer **Gereed**.
16. Selecteer **Meer details toevoegen** om meer details toe te voegen aan de onkosten. Welke velden beschikbaar zijn, is afhankelijk van de configuratie van Onkostenbeheer voor uw bedrijf.
17. Als het bedrijfsbeleid een ontvangstbewijs voor de onkosten vereist, selecteert u **Ontvangstbewijzen** en gaat u als volgt te werk:

    1. Selecteer **Ontvangst vastleggen** of **Ontvangstbestand bijvoegen**.
    2. Volg één van deze stappen:

        - Volg deze stappen als u **Ontvangst vastleggen** hebt geselecteerd:

            1. Selecteer **Foto maken** of **Afbeelding kiezen**.
            2. Volg één van deze stappen:

                - Als u **Foto maken** hebt geselecteerd, gaat u als volgt te werk:

                    1. U gaat naar de camera op uw mobiele apparaat, zodat u een foto van het ontvangstbewijs kunt maken. Wanneer u klaar bent met het maken van een foto, selecteert u **OK** om de foto te accepteren.
                    2. Optioneel: voer een naam in voor de foto en voer eventuele notities in.

                - Volg deze stappen als u **Afbeelding kiezen** hebt geselecteerd:

                    1. Selecteer een afbeelding in de lijst.
                    2. Optioneel: voer een naam in voor de afbeelding en voer eventuele notities in.

            3.  Selecteer **Gereed**.

        - Volg deze stappen als u **Ontvangstbewijs koppelen** hebt geselecteerd:

            1.  Selecteer een of meer afbeeldingen in de lijst.
            2.  Selecteer **Gereed**.

    3. Selecteer de knop **Terug** om terug te gaan naar de onkostendetails.

18. Als het bedrijfsbeleid gasten voor de onkosten vereist, selecteert u **Gasten** en gaat u als volgt te werk:

    1. Selecteer **Gast**, **Vorige gasten** of **Collega's**.
    2. Volg één van deze stappen:

        - Als u **Gast** hebt geselecteerd, gaat u als volgt te werk:

            1. Geef de naam op van de gast.
            2. Optioneel: voer de organisatie en/of het land van de gast in.
            3. Optioneel: voer de functie van de gast in.
            4. Selecteer **Gereed**.

        - Volg deze stappen als u **Vorige gasten** hebt geselecteerd:

            1. Selecteer een of meer eerdere gasten in de lijst. U ziet een lijst met eerdere gasten die u hebt toegevoegd aan vorige onkostenrapporten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw eerdere gast niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam of schakel over naar zoeken op organisatie, land of functie.
            2. Selecteer **Gereed**.

        - Als u **Collega's** hebt geselecteerd, gaat u als volgt te werk:

            1. Selecteer een of meer collega's in de lijst. U ziet een lijst met collega's die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw collega niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek op naam of schakel over naar zoeken op bedrijf of functie.
            2. Selecteer **Gereed**.

    3. Selecteer de knop **Terug** om terug te gaan naar de onkostendetails.

19. Als het bedrijfsbeleid een specificatie voor de onkosten vereist, selecteert u **Specificeren** en gaat u als volgt te werk:

    1. Selecteer de eerste datum om te specificeren.
    2. Selecteer **Specificatie toevoegen**.
    3. Selecteer de subcategorie voor de specificatie van de onkosten. U ziet een lijst met subcategorieën voor onkosten die in uw app zijn geladen voor offline gebruik. Standaard worden 50 artikelen geladen, maar een ontwikkelaar kan dit aantal wijzigen. Ontwikkelaars vinden meer informatie in het onderwerp [Mobiel platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md). Als uw subcategorie niet in de lijst staat, selecteert u **Zoeken** om online te zoeken. Zoek naar onkostensubcategorie op naam.
    4. Voer het transactiebedrag in voor de specificatie.
    5. Voer de transactiedatum in als deze is vereist.
    6. Selecteer **Gereed**.
    7. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle specificaties voor de geselecteerde datum.
    8. Voor extra dagen selecteert u **Kopiëren naar volgende dag** om de specificaties te kopiëren naar de volgende dag. U kunt ook de datum selecteren en specificaties toevoegen zoals u voor de eerste datum hebt gedaan.
    9. Nadat u de onkosten hebt gespecificeerd, selecteert u de knop **Terug** om terug te keren naar de onkostendetails.

20. Selecteer de knop **Terug** om terug te gaan naar de pagina **Onkostennota**.
21. Herhaal de voorgaande stappen totdat u klaar bent met het toevoegen van alle onkosten.
22. Selecteer **Indienen**.
23. Voer opmerkingen in voor de fiatteur.
24. Selecteer **Gereed**.

