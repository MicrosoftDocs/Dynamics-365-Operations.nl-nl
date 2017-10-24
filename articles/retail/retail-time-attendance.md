---
title: Tijd en aanwezigheid detailhandel
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van tijd en aanwezigheid in Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ebbf3c72b4c34cba95ecd2fb3ce506af393acc34
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="retail-time-and-attendance"></a>Tijd en aanwezigheid in detailhandel

[!include[banner](includes/banner.md)]


In dit onderwerp worden de scenario's beschreven die worden ondersteund voor beheer van tijd en aanwezigheid in Microsoft Dynamics 365 for Retail. 

<a name="manage-worker-setup-and-scheduling"></a>Het instellen en inplannen van medewerkers beheren
----------------------------------

### <a name="initial-configuration"></a> initiële configuratie

-   Voer de stappen in de configuratiewizard uit.
-   Werknemers registreren als tijdregistratiewerknemers.

### <a name="plan-worker-schedules"></a>De planning van de werknemersplannen

-   Profielen toepassen met behulp van de werkplanner. Voor meer informatie zie <https://technet.microsoft.com/en-us/library/aa551234.aspx>.

Voor informatie over de configuratiestappen zie <https://technet.microsoft.com/en-us/library/aa496971.aspx>.

### <a name="retail-specific-configuration"></a>Detailhandelspecifieke configuratie

-   Schakel een functionaliteitprofiel voor tijdklok in voor medewerkers voor wie u tijdregistratie wilt inschakelen. Klik op **POS-functionaliteitsprofielen** &gt; **Functies** &gt; **POS-tijdregistraties** &gt; **Tijdregistratie inschakelen**.
-   Configureer verkooppuntmachtigingsgroepen om de machtiging Registraties tijdklok weergeven in te schakelen. Met deze machtiging kan een gebruiker de prikklokregistraties van andere werknemers in de winkel bekijken (en van alle andere winkels waaraan de gebruiker is gekoppeld via het adresboek). U wilt mogelijk deze machtiging inschakelen voor een managerrol maar niet voor de rol van een kassamedewerker. Klik op **POS-machtigingsgroepen** &gt; **Registraties tijdklok weergeven**.

## <a name="register-time"></a>Tijd registreren
### <a name="cashier-and-non-cashier-time-registrations"></a>Tijdregistraties van kassiers en niet-kassiers

-   Op POS:
    -   Inklokbewerkingen:
        -   Meld u aan met een niet-ladebewerking of een nieuwe ploegendienst.
        -   Selecteer een tijdklokbewerking.
        -   Selecteer de gewenste bewerking:
            -   Inklokken
            -   Pauze voor werk
            -   Lunchpauze
            -   Uitklokken

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Huidige status</th>
    <th>Beschikbare bewerkingen</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>Inklokken</td>
    <td><ul>
    <li>Pauze voor werk</li>
    <li>Lunchpauze</li>
    <li>Uitklokken</li>
    </ul></td>
    </tr>
    <tr class="even">
    <td>Pauze voor werk</td>
    <td>Inklokken</td>
    </tr>
    <tr class="odd">
    <td>Lunchpauze</td>
    <td>Inklokken</td>
    </tr>
    <tr class="even">
    <td>Uitklokken</td>
    <td>Inklokken</td>
    </tr>
    </tbody>
    </table>

    [![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)
-   Bekijk het bevestigingsbericht weergeven, en controleer of de huidige activiteitstijd correct is.
-   Logboek:
    -   Klik op **Logboek** om prikklokactiviteit weer te geven.
    -   Gebruik de tijdsfilters om verschillende tijdvensters te selecteren.
    -   Als u met meerdere opslaglocaties werkt, ziet u hier uw tijdregistraties uit alle winkels waar u tijd hebt geregistreerd. U kunt het opslagfilter gebruiken om tijdregistraties van een geselecteerde opslag te bekijken.

<!-- -->

-   Verschillende tijdzones:
    -   Als u tijd weergeeft vanaf een andere locatie (voor het kassierslogboek of door **Registraties tijdklok weergeven** te gebruiken voor een managerscenario), en die locatie zich in een andere tijdzone bevindt, worden de tijdrecords die u ziet, omgezet naar uw plaatselijke tijdzone. U bent bijvoorbeeld een manager voor twee winkels, één in Arizona en andere in Nevada. Een kassamedewerker klokt zich in om 9:00 uur 's ochtends in Arizona. Op dat moment is de tijd in Nevada 8:00 's morgens. Daarom wordt de tijdregistratie gemarkeerd als 8 A.M. als u zich in de winkel in Nevada bevindt en de records voor tijdregistratie bekijkt.

## <a name="view-worker-time-registrations"></a>Tijdregistraties werknemers weergeven
### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a>Bekijk de tijdregistraties van de werknemers en filter op opslag- of activiteitstype

Op POS:

-   Selecteer **Registraties tijdklok weergeven**.
-   U ziet de activiteiten van de tijdklokregistratie van alle werknemers die zijn toegewezen aan dezelfde opslag als waaraan u bent toegewezen.
-   U kunt het activiteitstype gebruiken en filters opslaan om tijdregistraties te filteren.

## <a name="process-and-manage-time-registrations"></a>Tijdregistraties verwerken en beheren
Een gebruiker in Dynamics 365 for Retail volgt de werkstroom om tijdregistraties te berekenen, goed te keuren en naar de salarisadministratie over te brengen.

### <a name="primary-operations"></a>Primaire bewerkingen

-   Berekenen
-   Goedkeuren
-   Indienen voor salarisadministratie

### <a name="other-common-operations"></a>Overige veelgebruikte bewerkingen

-   Massaal uitklokken
-   Verzuim registreren

Voor meer informatie over het verwerken van tijd- en aanwezigheidsregistraties zie <https://technet.microsoft.com/en-us/library/aa573180.aspx>.




