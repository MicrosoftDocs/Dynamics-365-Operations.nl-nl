---
title: Meldingen voor uitvoering van wave
description: In dit onderwerp worden meldingen voor uitvoeringen van waves beschreven en wordt uitgelegd hoe u deze instelt.
author: mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: af3983db1a96116a88914411a26f1ac5d4857ae9
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103234"
---
# <a name="wave-execution-notifications"></a>Meldingen voor uitvoering van wave

[!include [banner](../includes/banner.md)]

De functie *Wave-uitvoeringsmeldingen* maakt gebruik van zakelijke gebeurtenissen en het Actiecentrum om meldingen te leveren die verband houden met de uitvoering van een wave. U kunt hiermee de typen gebeurtenissen opgeven die meldingen genereren, de magazijnen die ze genereren en de gebruikers die ze ontvangen.

De knop **Berichten weergeven** (belsymbool) aan de rechterkant van de navigatiebalk geeft aan wanneer een bericht uit het Actiecentrum beschikbaar is voor de huidige gebruiker. De gebruiker kan de knop **Berichten weergeven** selecteren om het Actiecentrum te openen en de berichten te bekijken.

Zakelijke gebeurtenissen vinden plaats wanneer bedrijfsprocessen worden uitgevoerd. Bedrijfsprocessen bestaan uit taken. Tijdens een bedrijfsproces voeren de gebruikers die eraan deelnemen zakelijke acties uit om die taken te voltooien. Zakelijke gebeurtenissen bieden een mechanisme waarmee externe systemen meldingen vanuit toepassingen voor financiën en bedrijfsactiviteiten kunnen ontvangen. Op deze manier kunnen de systemen zakelijke acties uitvoeren als reactie op de zakelijke gebeurtenissen. Zie [Overzicht van zakelijke gebeurtenissen](../../fin-ops-core/dev-itpro/business-events/home-page.md) voor meer informatie.

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>De functie Meldingen voor uitvoering van wave in- of uitschakelen

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Meldingen voor uitvoering van wave* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Scenario: meldingen voor batchuitvoeringen van waves naar het Actiecentrum verzenden

In dit scenario wordt de end-to-end stroom weergegeven voor het verzenden van meldingen over fouten bij het uitvoeren van wavebatches naar een specifieke rol via het Actiecentrum.

### <a name="make-demo-data-available"></a>Demogegevens beschikbaar maken

Voor dit scenario moeten demogegevens zijn geïnstalleerd en moet u de rechtspersoon **USMF** selecteren.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Zorg ervoor dat waves worden uitgevoerd in batchmodus

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het sneltabblad **Waveverwerking** de optie **Waves verwerken in batch** in op *Ja*.

> [!NOTE]
> Als u meldingen voor het uitvoeren van wavebatches wilt uitschakelen, stelt u de optie **Batchmeldingen voor waveverwerking uitschakelen** in op *Ja*.

### <a name="configure-a-wave-notification-policy"></a>Een wavemeldingsbeleid configureren

Wavemeldingsbeleid definieert de typen meldingen die worden verzonden en de gebruikers die een melding ontvangen.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavemeldingsbeleid**.
1. Maak een record met de volgende instellingen:

    - **Wavemeldingsbeleid:** *24BatchError*
    - **Beschrijving**: *Wavebatchfout voor magazijn 24*
    - **Melding verzenden bij**: *Alleen fout*
    - **Naar rol:** *Systeembeheerder*

        > [!NOTE]
        > Omdat dit scenario demogegevens gebruikt, wordt de rol *Systeembeheerder* geselecteerd omwille van de eenvoud. Daarom ontvangt u de meldingen omdat u bent aangemeld als systeembeheerder. In de praktijk moet u echter meestal een meer specifieke rol selecteren om te informeren over fouten bij het uitvoeren van wavebatches, zoals *Magazijnmanager*.

1. Selecteer **Opslaan** in het actievenster.

### <a name="configure-a-wave-template"></a>Een wavesjabloon configureren

Met wavesjablonen kunt u specifieke exemplaren van wavemethoden koppelen aan corresponderende wavelabelsjablonen.

1. Ga naar **Magazijnbeheer \> Instellen \> Waves \> Wavesjablonen**.
1. Stel in het lijstvenster het veld **Type wavesjabloon** in op *Verzending* en selecteer vervolgens de wavesjabloon *24 Standaardverzending* voor magazijn 24.
1. Stel op het sneltabblad **Algemeen** het veld **Wavemeldingsbeleid** in op *24BatchError*.

### <a name="configure-a-work-template"></a>Een werksjabloon configureren

Werksjablonen worden tijdens de uitvoering van de wave gebruikt om werk te genereren. Voor dit scenario zou wave-uitvoering een fout moeten veroorzaken. Door de werksjabloonquery in te stellen om een niet-bestaand magazijn te gebruiken, zorgt u ervoor dat de uitvoering van de wave mislukt en er een melding wordt verzonden.

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel in het lijstvenster het veld **Type werksjabloon** in op *Verkooporders* en selecteer vervolgens de werksjabloon *24 SO Stage* voor magazijn 24.
1. Selecteer **Query bewerken** in het actievenster.
1. Bewerk in het dialoogvenster query-editor op het tabblad **Bereik** de volgende rij (of voeg deze toe als deze niet bestaat):

    - **Tabel:** *Tijdelijke werktransacties*
    - **Afgeleide tabel:** *Tijdelijke werktransacties*
    - **Veld:** *Magazijn*
    - **Criteria**: wijzig de waarde van *24* in *Fout*.

1. Selecteer **OK** en bevestig de wijziging.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Een verkooporder maken en vrijgeven naar het magazijn

1. Ga naar **Verkoop en marketing \> Verkooporder \> Alle verkooporders**.
1. Maak een verkooporder met de volgende instellingen:

    - **Klantrekening:** *US-001*
    - **Magazijn:** *24*

1. Voeg op het sneltabblad **Verkooporderregels** een verkooporderregel toe met de volgende instellingen:

    - **Artikelnummer:** *A0001*
    - **Hoeveelheid:** *10*

    > [!NOTE]
    > Deze artikelen en hoeveelheden zijn slechts voorbeelden. Er moet voldoende voorraad aanwezig zijn in het opgegeven magazijn.

1. Terwijl de nieuwe regel nog steeds is geselecteerd op het sneltabblad **Verkooporderregels**, selecteert u **Voorraad \> Reservering** op de werkbalk.
1. Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren**. Sluit de pagina vervolgens.
1. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Vrijgeven naar magazijn**.

### <a name="notifications-from-wave-batch-job-execution"></a>Meldingen van uitvoering van wavebatchtaken

Afhankelijk van de installatie van uw zakelijke gebeurtenissen ontvangt u uiteindelijk een melding over een storing bij de uitvoering van de wave. Het bericht uit het Actiecentrum lijkt op het volgende voorbeeld en bevat een koppeling naar de wave die is mislukt.

> **Fout tijdens uitvoering van wave**  
> Er is een fout opgetreden tijdens het uitvoeren van wave USMF-000000001.  
> Laatste berichten: Er is geen werk gemaakt voor Wave USMF-000000001.
>
> **STATUS**  
> Actief
>
> Wavegegevens openen

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
