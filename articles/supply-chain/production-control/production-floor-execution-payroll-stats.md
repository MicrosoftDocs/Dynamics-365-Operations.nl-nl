---
title: Verlofsaldi weergeven in de uitvoeringsinterface voor de werkvloer
description: Dit artikel bevat een voorbeeldscenario waarin u ziet hoe u Microsoft Dynamics 365 Supply Chain Management zo instelt dat salarisstatistieken worden gebruikt om werknemers een overzicht te geven van hun verlofsaldo voor het huidige jaar.
author: johanhoffmann
ms.date: 04/22/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-04-22
ms.dyn365.ops.version: 10.0.XX
ms.openlocfilehash: 2a6b6f52bfa7539b7c9bb5841536b0d564d0274c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852268"
---
# <a name="show-vacation-balances-in-the-production-floor-execution-interface"></a>Verlofsaldi weergeven in de uitvoeringsinterface voor de werkvloer

[!include [banner](../includes/banner.md)]

Dit artikel bevat een voorbeeldscenario waarin u ziet hoe u Microsoft Dynamics 365 Supply Chain Management zo instelt dat salarisstatistieken worden gebruikt om elke werknemer een overzicht te geven van diens verlofsaldo voor het huidige jaar. Werknemers kunnen hun verlofsaldo zien in het dialoogvenster **Mijn dag** in de uitvoeringsinterface voor de werkvloer.

In dit scenario wordt de Deense verlofwet gebruikt, waarbij het verlofjaar loopt van 1 september tot en met 31 augustus. In dit scenario heeft uw bedrijf een nieuwe werknemer aangenomen, die een saldo van 10 vakantiedagen krijgt voor de rest van het huidige verlofjaar.

## <a name="turn-on-the-required-features"></a>De vereiste functies inschakelen

Als u dit scenario wilt uitvoeren, moet u de weergave *Mijn dag* inschakelen voor de functie uitvoeringsinterface voor de werkvloer in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Informatie over het inschakelen van deze en andere functies voor de uitvoeringsinterface voor de werkvloer vindt u in [De uitvoeringsinterface voor de werkvloer configureren](production-floor-execution-configure.md).

## <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u dit scenario wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

## <a name="create-a-new-pay-type"></a>Een nieuw salaristype maken

Begin met het maken van een nieuw *salaristype* voor het bijhouden van de verlofdagen van de werknemers (ook wel *verlofsaldo* genoemd). Salaristypen worden doorgaans gebruikt om het salaris van werknemers te berekenen. Het salaristype dat u hier maakt, wordt echter gebruikt om een saldo te berekenen.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Salarisadministratie \> Salaristypen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Salaristype**: *5151-1*
    - **Beschrijving:** *Teller voor verlofdagen van werknemer*
    - **Opnemen in exporteren**: *Nee*

## <a name="update-the-pay-agreement"></a>De salarisovereenkomst bijwerken

In deze sectie bewerkt u een bestaande *salarisovereenkomst* door het nieuwe salaristype toe te voegen en de regels in te stellen die bepalen hoe het verlofsaldo van elke werknemer wordt aangepast wanneer verlofdagen worden geregistreerd.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Salarisadministratie \> Salarisovereenkomsten**.
1. Selecteer de salarisovereenkomst waarvoor u het verlofbeleid wilt instellen. Als u werkt met de standaardvoorbeeldgegevens van USMF, is er slechts één salarisovereenkomst: *Man*.
1. Zorg ervoor dat de geselecteerde salarisovereenkomst geldig is voor de huidige datum. Als u met standaardvoorbeeldgegevens van USMF werkt, kan het veld **Einddatum** van de salarisovereenkomst *Man* worden ingesteld op een datum die in het verleden ligt. Wijzig zo nodig de waarde naar een datum die ongeveer twee jaar in de toekomst ligt.
1. Klik in het actievenster op **Overeenkomstregels**.
1. Stel op de pagina **Salarisovereenkomstregels** op het sneltabblad **Overzicht** de volgende waarden in op de werkbalk:

    - Selecteer in de eerste vervolgkeuzelijst de waarde **Maandag**.
    - Selecteer in de tweede vervolgkeuzelijst de waarde **Afwezigheid**.

1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij het veld **Salaristype** in op het salaristype dat u voor dit scenario hebt gemaakt (*5151-1*). Laat alle andere instellingen op de standaardwaarden.
1. Met de nieuwe rij nog steeds geselecteerd stelt u op het sneltabblad **Algemeen** de volgende waarden in:

    - **Verzuimcodegroep**: *Vakantie*
    - **Vaste hoeveelheid gebruiken**: *Ja*
    - **Constant**: *-1*

1. Selecteer in het actievenster **Dag kopiëren**.
1. Stel in het dialoogvenster **Dag kopiëren** de volgende waarden in:

    - **Dinsdag**, **Woensdag**, **Donderdag** en **Vrijdag**: *Ja*
    - **Overschrijven**: *Ja*
    - **Afwezigheid**: *Ja*

1. Selecteer **OK**.

## <a name="create-a-payroll-statistic-group"></a>Een salarisstatistiekgroep maken

Met *salarisstatistiekgroepen* kunt u statistieken instellen voor registraties van werknemers gedurende een periode. In dit scenario gebruikt u een salarisstatistiekgroep om het aantal verlofdagen te berekenen dat werknemers tijdens een verlofperiode verdienen. In Denemarken loopt de verlofperiode van 1 september tot en met 31 augustus.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Salarisadministratie \> Salarisstatistiekgroepen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Groep salarisstatistieken:** *VAC*
    - **Beschrijving:** *Verlofsaldo*
    - **Overboeking** *Nee*

1. Met de nieuwe rij nog steeds geselecteerd selecteert u de optie **Instellen** in het actievenster.
1. Selecteer op de pagina **Instellen** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij het veld **Salaristype** in op *5151-1*.
1. Selecteer het veld **Periodecode** en houdt het vast (of klik erop met de rechtermuisknop) en selecteer vervolgens **Details weergeven**. U kunt nu de periodecode instellen die u later aan dit veld wilt toewijzen.
1. Selecteer op de pagina **Periodetypen** in het actievenster de optie **Nieuw** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Periodetypen:** *VerlofJaar*
    - **Beschrijving:** *Verlofjaar*
    - **Frequentie:** *Jaren*

1. Met de nieuwe rij nog steeds geselecteerd selecteert u de optie **Perioden genereren** in het actievenster.
1. Stel in het dialoogvenster **Perioden genereren** de volgende waarden in:

    - **Geef begindatum van de periode op:** *1 september 2021*
    - **Lengte van periode:** *5*

1. Selecteer **OK**.
1. Sluit de pagina **Periodetypen** en ga terug naar de pagina **Salarisstatistiekgroepen**.
1. Stel het veld **Periodecode** in op het periodetype dat u zojuist hebt gemaakt (*VerlofJaar*).

## <a name="create-a-statistical-balance-setup"></a>Een configuratie van statistisch saldo maken

In deze sectie maakt u een *statistische-saldo-configuratie* die is gekoppeld aan de salarisstatistiekgroep die u in de vorige sectie hebt gemaakt. Later koppelt u deze statistische-saldo-configuratie aan de weergave **Mijn dag** in de uitvoeringsinterface voor de werkvloer. In de weergave **Mijn dag** worden de verlofsaldi weergeven voor het salaristype dat is toegewezen aan de bijbehorende salarisstatistiekgroep.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Salarisadministratie \> Configuratie van statistisch saldo**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in:

    - **Groep salarisstatistieken:** *VAC*
    - **Externe naam:** *Verlofsaldo*
    - **Flextijd:** *Nee*

## <a name="create-a-manual-premium"></a>Een handmatige premie maken

Door middel van *handmatige premies* worden doorgaans werknemers extra salaris verleend voor extra werk. In dit scenario maakt u een handmatige premie waarmee u het initiële verlofsaldo kunt instellen voor elke werknemer.

1. Ga naar **Tijd en aanwezigheid \> Instellingen \> Salarisadministratie \> Handmatige premies**.
1. Selecteer **Nieuw** in het actievenster om een record toe te voegen.
1. Stel in de nieuwe record de volgende waarden in:

    - **Premies:** *Verlof*
    - **Beschrijving:** *Aanpassingen in het verlofsaldo van werknemers*
    - **Salaristype**: *5151-1*

## <a name="set-a-workers-initial-vacation-balance-and-adjust-it-by-one-day"></a>Het initiële verlofsaldo van een werknemer instellen en dit met één dag aanpassen

Salarisadministrateurs kunnen op de pagina **Goedkeuren** de dagelijkse registraties van werknemers controleren en goedkeuren. In dit scenario neemt u de rol op van een beheerder, zodat u het oorspronkelijke verlofsaldo voor een werknemer kunt instellen en verlofdagen kunt registreren die de werknemer opneemt.

1. Ga naar **Tijd en aanwezigheid \> Controleren en goedkeuren \> Goedkeuren**.
1. Stel in het dialoogvenster **Goedkeuren** de volgende velden in:

    - **Goedkeuringsgroep**: Selecteer de goedkeuringsgroep waar u bij hoort. Als u werkt met de standaardvoorbeeldgegevens van USMF, is er slechts één goedkeuringsgroep: *AdmMan*.
    - **Hele groep weergeven, 1 dag**: Selecteer de optie en stel vervolgens het veld in op de huidige datum.

1. Selecteer **OK**.
1. Op de pagina **Goedkeuren** wordt een lijst getoond met records die aan uw criteria voldoen. Selecteer de werknemer die u wilt goedkeuren. Als u werkt met standaardvoorbeeldgegevens van USMF, selecteert u *000496* (*Christina Portra*).
1. De geselecteerde werknemer 10 dagen verlof toekennen:

    1. Met de werknemer nog steeds geselecteerd selecteert u de optie **Premieregels** in het actievenster.
    1. Selecteer op de pagina **Premieregels** in het actievenster **Nieuw** om een rij aan het raster toe te voegen.
    1. Stel in de nieuwe rij de volgende waarden in:

        - **Premies:** *Verlof*
        - **Hoeveelheid:** *10*

    1. Sluit de pagina **Premieregels**.

1. Registreer op de pagina **Goedkeuren** het feit dat de werknemer een van haar verlofdagen heeft gebruikt op de huidige datum:

    1. Met de werknemer nog steeds geselecteerd selecteert u in het onderste gedeelte van de pagina op het tabblad **Overzicht** de optie **Nieuw** op de werkbalk om een rij aan het raster toe te voegen.
    1. Stel in de nieuwe rij de volgende waarden in:

        - **Journaalregistratietype**: *Verlof*
        - **Verwijzing**: *Verlof*

    1. Selecteer in het bovenste deel van de pagina de optie **Overboeking** op de werkbalk om het verlofsaldo toe te passen en de inhouding te berekenen.

## <a name="configure-the-production-floor-execution-interface-so-that-it-includes-the-my-day-dialog-box"></a>De uitvoeringsinterface voor de werkvloer configureren zodat deze het dialoogvenster Mijn dag bevat

In deze sectie voegt u een knop **Mijn dag** toe aan de uitvoeringsinterface voor de werkvloer. Werknemers kunnen vervolgens met deze knop het dialoogvenster **Mijn dag** openen.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer configureren**.
1. Selecteer een configuratie, bijvoorbeeld *Standaard*.
1. Selecteer **Tabbladen ontwerpen** in het actievenster.
1. Selecteer op de pagina **Tabbladen ontwerpen** in het lijstdeelvenster de waarde *Alle taken* om de instellingen voor het tabblad weer te geven. In het veld **Hoofdweergave** moet u nu de waarde *Alle taken* zien staan.
1. Selecteer **Bewerken** in het actievenster.
1. Selecteer op het sneltabblad **Secundaire werkbalk** in de kolom **Beschikbare acties** de waarde **Mijn dag**. Selecteer vervolgens de knop pijl-rechts om de waarde te verplaatsen naar de kolom **Geselecteerde acties**.

## <a name="check-your-balance-in-the-production-floor-execution-interface"></a>Uw saldo controleren in de uitvoeringsinterface voor de werkvloer

In deze sectie meldt u zich aan bij de uitvoeringsinterface voor de werkvloer als de werknemer voor wie u eerder verloftijd hebt ingesteld. Vervolgens opent u het dialoogvenster **Mijn dag** om uw verlofsaldo weer te geven.

1. Ga naar **Productiebeheer \> Instellen \> Productie-uitvoering \> Uitvoering werkvloer**.
1. Als u wordt gevraagd een configuratie te selecteren, selecteert u de configuratie die u eerder in dit scenario hebt ingesteld (*Standaard*).
1. Meld u aan als de gebruiker die u eerder in dit scenario hebt geconfigureerd. Als u werkt met standaardvoorbeeldgegevens van USMF, kunt u zich aanmelden door *123* in te voeren in het veld **Badge-id**. Deze badge-ID komt overeen met Christina Portra.
1. Selecteer in de werkbalk links de optie **Mijn dag**.
1. Controleer de sectie **Saldi** in het dialoogvenster. In dit gedeelte moet nu worden getoond dat u een saldo hebt van negen verlofdagen.
