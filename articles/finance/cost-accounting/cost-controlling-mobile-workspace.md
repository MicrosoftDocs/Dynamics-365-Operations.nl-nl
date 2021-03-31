---
title: Mobiel werkgebied voor kostenbeheer
description: Dit onderwerp bevat informatie over het mobiele werkgebied Kostenbeheer. Via dit werkgebied kunnen kostenplaatsmanagers altijd en overal informatie over de prestaties van hun kostenplaats bekijken.
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMMobileCostObjectOverviewDetailsCurrentPeriod, CAMMobileCostObjectList, CAMMobileCostObjectOverviewDetailsPreviousPeriod, CAMMobileCostObjectOverview, CAMMobileCostObjectOverviewDetailsYearToDate, CAMMobileCostControlWorkspaceConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f75a868acd8ae7e77c7080e2afe81788490bcccb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226408"
---
# <a name="cost-controlling-mobile-workspace"></a>Mobiel werkgebied voor kostenbeheer

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat informatie over het mobiele werkgebied **Kostenbeheer**. Via dit werkgebied kunnen kostenplaatsmanagers altijd en overal informatie over de prestaties van hun kostenplaats bekijken.

Dit mobiele werkgebied is bedoeld om samen te worden gebruikt met de mobiele app van Finance and Operations.

## <a name="overview"></a>Overzicht
Het mobiele werkgebied **Kostenbeheer** biedt een directe weergave van de huidige prestaties van kostenplaatsen door werkelijke kosten ten opzichte van de gebudgetteerde kosten te vergelijken. U kunt inzoomen op de status van afzonderlijke kostenelementen.

Bijvoorbeeld: een werknemer ontvangt een uitnodiging voor een internationale conferentie, maar de organisatie moet alle reiskosten betalen. De werknemer vraagt zijn/haar manager of hij/zij de conferentie mag bijwonen. De manager opent het mobiele werkgebied **Kostenbeheer** op haar/zijn mobiele apparaat om te zien of er budget is zodat de werknemer de conferentie kan bijwonen.

### <a name="data-security"></a>Gegevensbeveiliging
De gegevens in het mobiele werkgebied **Kostenbeheer** worden beveiligd via gebruikersreferenties. Kostenplaatsmanagers mag alleen gegevens voor hun eigen kostenplaats bekijken. De beveiliging op toegangsniveau wordt beheerd binnen de module **Kostprijsboekhouding**.

Kostenaccountants definiëren de configuratie van het mobiele werkgebied **Kostenbeheer** in de module **Kostprijsboekhouding**. Nadat het werkgebied is gepubliceerd naar de mobiele app, is het beschikbaar in de app. Hierdoor kunnen alle kostenplaatsmanagers in de organisatie gegevens in dezelfde indeling bekijken.

### <a name="actions-views-and-links"></a>Acties, weergaven en koppelingen
Het mobiele werkgebied **Kostenbeheer** bevat de volgende acties, weergaven en koppelingen:

-   **Acties:**

    -   Gebruik **Configuratie selecteren** om een indeling te selecteren.
    -   Gebruik **Kostenplaats selecteren** om de kostenplaatsen te selecteren waarvoor u gegevens wilt filteren.
    
        > [!NOTE]
        > Welke kostenplaatsen in de lijst worden weergegeven, is afhankelijk van de toegang die wordt verleend in de module **Kostprijsboekhouding**.

-   **Weergaven:** op basis van de acties die zijn geselecteerd en de configuratie in de module **Kostprijsboekhouding**, kunt u de volgende informatie weergeven in de kaarten:

    -   Werkelijk versus budget (huidige periode)
    -   Werkelijk versus herzien budget (huidige periode)
    -   Werkelijk versus budget (vorige periode)
    -   Werkelijk versus herzien budget (vorig periode)
    -   Werkelijk versus budget (jaar tot heden)
    -   Werkelijk versus herzien budget (jaar tot heden)

    De volgende bedragen worden weergegeven op elke kaart: werkelijk, budget, afwijking en afwijking %.

-   **Koppelingen:**

    -   Details voor huidige periode
    -   Details voor vorige periode
    -   Details voor jaar tot heden

    Wanneer u een koppeling selecteert, wordt een kaart voor elk kostenelement weergegeven. De volgende bedragen worden weergegeven op elke kaart: Werkelijk, Budget, Budgetafwijking, Budgetafwijking %, Herzien budget, Herziene budgetafwijking en Herziene budgetafwijking %.
    
    [![Kaart voor een kostenelement ](./media/Cost-controlling.png)](./media/Cost-controlling.png)

## <a name="prerequisites"></a>Vereisten
De vereisten verschillen, afhankelijk van de versie van Microsoft Dynamics 365 die voor uw organisatie is geïmplementeerd.

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-finance"></a>Vereisten als u Microsoft Dynamics 365 Finance gebruikt
Als Finance is geïmplementeerd in uw organisatie, moet de systeembeheerder het mobiele werkgebied **Kostenbeheer** publiceren. Zie voor meer informatie [Een mobiel werkgebied publiceren](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Vereisten als u versie 1611 met platformupdate 3 of hoger gebruikt
Als versie 1611, met platformupdate 3 of hoger voor uw organisatie is geïmplementeerd, moet de systeembeheerder de volgende vereisten uitvoeren.

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

<td>KB 4013633 is een X++-update of metagegevenshotfix die het mobiele werkgebied <strong>Kostenbeheer</strong> bevat. Uw systeembeheerder moet de volgende stappen uitvoeren voor het implementeren van KB 4013633.
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Metagegevens-hotfix downloaden uit  Microsoft Dynamics Lifecycle Services (LCS)</a>.</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">De metagegevenshotfix installeren</a>.</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Een implementeerbaar pakket maken</a> dat de ApplicationSuite en <strong>SCMMobile</strong>-modellen bevat en het implementeerbare pakket vervolgens uploaden naar LCS.</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Het implementeerbare pakket toepassen</a></li>

</ol></td>
</tr>
<tr class="even">
<td>Het mobiele werkgebied <strong>Kostenbeheer</strong> publiceren.</td>
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

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a>De prestaties van de kostenplaats weergeven met behulp van het mobiele werkgebied Kostenbeheer

1.  Selecteer op uw mobiele apparaat het werkgebied **Kostenbeheer**.
2.  Selecteer **Kostenbeheer**.
3.  Selecteer **Acties**.
4.  Selecteer **Configuratie selecteren** om een indeling voor kostenbeheer te selecteren.
5.  Selecteer **Gereed**.
6.  Selecteer **Acties**.
7.  Selecteer **Kostenobject selecteren** om de kostenplaatsen te selecteren waartoe u toegang hebt gekregen.
8.  Selecteer **Gereed**.
9.  Geef de prestaties van uw kostenplaats weer.
10. Selecteer de koppeling **Details voor huidige periode**.
11. Geef de prestaties van afzonderlijke kostenelementen weer.
12. U kunt ook zoeken naar specifieke kostenelementen.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]