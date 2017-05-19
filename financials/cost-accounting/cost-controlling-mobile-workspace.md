---
title: Mobiel werkgebied voor kostenbeheer
description: Dit onderwerp biedt informatie over het mobiele werkgebied Kostenbeheer, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunnen kostenplaatsmanagers altijd en overal informatie over de prestaties van hun kostenplaats bekijken.
author: YuyuScheller
manager: AnnBe
ms.date: 05/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 31a9650774b2ddb70827ffa210154ca10c761236
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="cost-controlling-mobile-workspace"></a>Mobiel werkgebied voor kostenbeheer

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over het mobiele werkgebied Kostenbeheer, dat beschikbaar is voor de mobiele app voor Microsoft Dynamics 365 for Operations. Via dit werkgebied kunnen kostenplaatsmanagers altijd en overal informatie over de prestaties van hun kostenplaats bekijken. 

<a name="overview-of-the-cost-controlling-mobile-workspace"></a>Overzicht van het mobiele werkgebied Kostenbeheer
-------------------------------------------------

Het mobiele werkgebied **Kostenbeheer** biedt een directe weergave van de huidige prestaties van kostenplaatsen door werkelijke kosten ten opzichte van de gebudgetteerde kosten te vergelijken. U kunt inzoomen op statuswaarden van afzonderlijke kostenelementen. Bijvoorbeeld: een werknemer ontvangt een uitnodiging voor een internationale conferentie, maar de organisatie moet alle reiskosten betalen. De werknemer vraagt zijn manager of hij de conferentie mag bijwonen. De manager opent snel het mobiele werkgebied **Kostenbeheer** op haarmobiele telefoon om te zien of zij budget heeft zodat de werknemer de conferentie kan bijwonen.

### <a name="data-security"></a>Gegevensbeveiliging

De gegevens in het mobiele werkgebied **Kostenbeheer** worden beveiligd via gebruikersreferenties. Kostenplaatsmanagers mag alleen gegevens voor hun eigen kostenplaats bekijken. De beveiliging op toegangsniveau wordt beheerd binnen de module **Kostprijsboekhouding**. Kostenaccountants definiëren de configuratie van het mobiele werkgebied **Kostenbeheer** in de module **Kostprijsboekhouding**. Nadat het werkgebied is gepubliceerd naar de mobiele app van Microsoft Dynamics 365 for Operations, is het beschikbaar in de app. Hierdoor kunnen alle kostenplaatsmanagers in de organisatie gegevens in dezelfde indeling bekijken.

### <a name="actions-views-and-links"></a>Acties, weergaven en koppelingen

Het mobiele werkgebied **Kostenbeheer** voor de Dynamics 365 for Operations-app biedt de volgende acties, weergaven en koppelingen:

-   **Acties:**
    -   Gebruik **Configuratie selecteren** om een indeling te selecteren.
    -   Gebruik **Kostenplaats selecteren** om de kostenplaatsen te selecteren waarvoor u gegevens wilt filteren. **Opmerking:** welke kostenplaatsen in de lijst worden weergegeven, is afhankelijk van de toegang die wordt verleend in de module **Kostprijsboekhouding**.
-   **Weergaven:** op basis van de acties die zijn geselecteerd en de configuratie in de module **Kostprijsboekhouding**, kunt u de volgende informatie weergeven in de kaarten.
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

    Wanneer u een koppeling selecteert, wordt een kaart voor elk kostenelement weergegeven. De volgende bedragen worden weergegeven op elke kaart: Werkelijk, Budget, Budgetafwijking, Budgetafwijking in %, Herzien budget, Herziene budgetafwijking en Herziene budgetafwijking in %. 
    
    [![Kaart voor een kostenelement ](./media/cost-controlling.png)](./media/cost-controlling.png)

## <a name="prerequisites"></a>Vereisten
Voordat u het mobiele werkgebied **Kostenbeheer** kunt gebruiken, controleert u of de systeembeheerder de volgende vereisten heeft geregeld.

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
<td>Het mobiele werkgebied <strong>Kostenbeheer</strong> moet worden gepubliceerd naar de mobiele app voor Dynamics 365 for Operations.</td>
<td>Systeembeheerder</td>
<td><ol>
<li>Start Dynamics 365 for Operations in uw browser.</li>
<li>Selecteer op de pagina <strong>Systeemparameters</strong> de optie <strong>Mobiele werkgebieden beheren</strong>.</li>
<li>Selecteer het werkgebied <strong>Overzicht van kostenobjecten</strong>.</li>
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





