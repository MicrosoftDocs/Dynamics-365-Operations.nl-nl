---
title: Het scenario productievertraging
description: In dit artikel wordt het scenario Productievertraging beschreven, dat een melding genereert als de productiedoorvoer onder een bepaalde drempelwaarde daalt.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreScenarioConfigurationWizardV2, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 25ccbda1628544f14dc32d9bea3f2162ad47d79e
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690016"
---
# <a name="the-production-delays-scenario"></a>Het scenario productievertraging

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Het scenario *productievertraging* genereert een melding als de productiedoorvoer onder een bepaalde drempelwaarde daalt. In dit scenario wordt een *onderdeel uit*-signaal naar de Microsoft Azure IoT-hub verzonden voor elk geproduceerd artikel. In Dynamics 365 Supply Chain Management wordt de ordervertraging berekend op basis van de geplande duur van de productieorder, het aantal artikelen dat moet worden geproduceerd, hoe lang de taak actief is en hoeveel *onderdeel uit*-signalen zijn ontvangen. Er wordt een vertragingsmelding gegenereerd als het aantal *onderdeel uit*-signalen voor de taak onder de drempelwaarde daalt.

## <a name="scenario-dependencies"></a>Afhankelijkheden voor dit scenario

Het scenario *productievertragingen* heeft de volgende afhankelijkheden:

- Er kan alleen een waarschuwing worden geactiveerd als een productieorder wordt uitgevoerd op een toegewezen machine.
- Er moet een signaal dat overeenkomt met een *onderdeel uit*-signaal voor een toegewezen machine met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.
- Een Unix-eigenschap tijdstempel, waarbij de waarde wordt uitgedrukt in milliseconden (ms), moet aanwezig zijn in het Azure IoT Hub-bericht.

## <a name="prepare-demo-data-for-the-product-delays-scenario"></a>Demogegevens voorbereiden voor het scenario productvertragingen

Als u een demonstratiesysteem wilt gebruiken om het scenario *productvertragingen* te testen, gebruikt u een systeem waarop de [demonstratiegegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd, selecteert u de rechtspersoon *USMF* (bedrijf) en bereidt u de aanvullende demonstratiegegevens voor, zoals wordt beschreven in deze sectie. U kunt deze sectie overslaan als u uw eigen sensoren en gegevens gebruikt.

### <a name="set-up-sensor-simulator"></a>Een sensorsimulator instellen

Als u dit scenario wilt uitproberen zonder een fysieke sensor te gebruiken, kunt u een simulator instellen om de vereiste signalen te genereren. Meer informatie over dit onderwerp vindt u in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md).

### <a name="verify-that-resource-3118-is-used-for-product-p0111"></a>Controleren of resource 3118 wordt gebruikt voor product P0111

Een productieorder wordt gepland en vrijgegeven. Daarom wordt een productietaak vrijgegeven voor resource *3118* (*Foam cutting machine*). Volg deze stappen om te controleren of resource *3118* wordt gebruikt voor product *P0111* in uw demonstratiegegevens.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *P0111*.
1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Weergave** de optie **Route**.
1. Selecteer op de pagina **Route**, op het tabblad **Overzicht** onderaan de pagina, de regel waarop het veld **Bewerkingsnr.** is ingesteld op *30*.
1. Ga naar het tabblad **Resourcevereisten** onderaan de pagina en controleer of dat resource *3118* (*Foam cutting machine*) is gekoppeld aan de bewerking.

### <a name="create-and-release-a-production-order-for-product-p0111"></a>Een productieorder voor het product P0111 maken en deze vrijgeven

Volg deze stappen om een productieorder voor product *P0111* te maken en vrij te geven.

1. Ga naar **Productiebeheer \> Productieorders \> Alle productieorders**.
1. Ga naar de pagina **Alle productieorders** en selecteer in het actievenster de optie **Nieuwe batchorder**.
1. Stel in het dialoogvenster **Batch maken** de volgende waarden in:

    - **Artikelnummer:** *P0111*
    - **Hoeveelheid:** *10*

1. Selecteer **Maken** om de order te maken en terug te keren naar de pagina **Alle productieorders**.
1. Gebruik het veld **Filter** om te zoeken naar productieorders waarbij het veld **Artikelnummer** is ingesteld op *P0111*. Zoek en selecteer vervolgens de productieorder die u zojuist hebt gemaakt.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Raming**.
1. Selecteer in het dialoogvenster **Raming** **OK** om de raming uit te voeren.
1. Selecteer in het actievenster op het tabblad **Productieorder** in de groep **Proces** de optie **Vrijgave**.
1. Noteer het nummer van de batchorder die u hebt gemaakt, die u ziet in het dialoogvenster **Vrijgave**.
1. Selecteer **OK** om de order vrij te geven.

### <a name="configure-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer configureren

Als u de interface voor de uitvoering van de productielijn nog niet hebt geconfigureerd om taken weer te geven die zijn toegewezen aan resource *3118* (*Foam cutting machine*), doe dit dan nu. Zie de volgende secties voor instructies:

- [De uitvoeringsinterface voor de werkvloer configureren](sdi-scenario-equipment-downtime.md#config-pfe)
- [De zoekoptie inschakelen voor de uitvoeringsinterface voor de werkvloer](sdi-scenario-equipment-downtime.md#enable-pfe-search)

### <a name="start-the-first-job-in-the-batch-order"></a>De eerste taak in de batchorder starten

Volg deze stappen om de eerste taak in de batchorder te starten.

1. Ga naar **Productiebeheer \> Productie-uitvoering \> Uitvoering werkvloer**.
1. Typ **123** in het veld *Badge-ID*. Selecteer vervolgens **Aanmelden**.
1. Als u wordt gevraagd om een reden voor afwezigheid, selecteert u een van de kaarten voor afwezigheid en selecteert u vervolgens **OK**.
1. Voer in het veld **Zoeken** het batchordernummer in dat u eerder hebt genoteerd. Selecteer vervolgens de toets **Terug**.
1. Selecteer de order en selecteer **Taak beginnen**.
1. Selecteer in het dialoogvenster **Taak beginnen** de knop **Starten**.

## <a name="set-up-the-production-delays-scenario"></a>Het scenario voor productievertragingen instellen

Volg deze stappen om het scenario *productvertragingen* in te stellen Supply Chain Management.

1. Ga naar **Productiebeheer \> Instellingen \> Sensor Data Intelligence \> Scenario's**.
1. Selecteer in het vak van het scenario **productvertragingen** de optie **Configureren** om de configuratiewizard voor dit scenario te openen.
1. Selecteer op de pagina **Sensoren** de optie **Nieuw** om een sensor toe te voegen aan het raster. Stel er daarna de volgende velden voor in:

    - **Sensor-ID**: voer de id in van de sensor die u gebruikt Als u de Raspberry Pi Azure IoT Online Simulator gebruikt en deze hebt ingesteld zoals beschreven in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md), voer dan *Productievertraging* op.
    - **Beschrijving van de sensor**: voer een beschrijving van de sensor in.

1. Herhaal nu de vorige stap voor elke extra sensor die u wilt toevoegen. U kunt later op elk moment terug komen en meer sensoren toevoegen.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Toewijzing van bedrijfsrecord** in de sectie **Sensoren** de record voor een van de sensoren die u zojuist hebt toegevoegd.
1. Selecteer in het gedeelte **Toewijzing van bedrijfsrecord** de optie **Nieuw** om een rij aan het raster toe te voegen.
1. Stel in de nieuwe rij het veld **Bedrijfsrecord** in op de resource die u wilt bewaken met de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit in op *3118, Foam cutting machine*.
1. Selecteer **Volgende**.
1. Volg deze stappen op de pagina **Afwijkingsdrempel productievertraging** als u de demonstratiegegevens gebruikt die u eerder in dit artikel hebt gemaakt:

    1. Selecteer de kolomkop **Artikelrelatie** om een vervolgkeuzedialoogvenster te openen met zoekfilters voor de kolom. Geef *P0111* op in het zoekvak en selecteer **Toepassen**.
    2. Selecteer de regel waarin het veld **Bewerking** is ingesteld op *Bijsnijden* (Trim/Cut). Stel het veld **Meldingsdrempel voor vertraging (%)** in op de drempel (als een percentage) waarvoor een melding moet worden verzonden.

1. Selecteer **Volgende**.
1. Selecteer op de pagina **Sensors activeren** in het raster de sensor die u toegevoegd hebt en selecteer vervolgens **Activeren**. Voor elke geactiveerde sensor in het raster wordt een vinkje weergegeven in de kolom **Actief**.
1. Selecteer **Voltooien**.

## <a name="work-with-the-production-delays-scenario"></a>Werken met het scenario voor productievertragingen

### <a name="view-production-delay-data-on-the-resource-status-page"></a>Gegevens voor productvertragingen weergeven op de pagina Resourcestatus

Op de pagina **Resourcestatus** kunnen supervisors een tijdlijn controleren van signalen die worden ontvangen van de sensoren die zijn toegekend aan elke machineresource. Volg deze stappen om de tijdlijn te configureren:

1. Ga naar **Productiebeheer \> Productieregistratie \> Resourcestatus**.
1. Stel in het dialoogvenster **Configureren** de volgende velden in:

    - **Resource**: selecteer de resources die u wilt bewaken. Als u met de demonstratiegegevens werkt, selecteert u *3118*.
    - **Tijdreeks 1:** selecteer de record (metrische sleutel) met de volgende notatie voor de naam: *ProductionJobDelayed:WerkelijkeHoeveelheid:&lt;TaakID&gt;*.
    - **Weergavenaam**: voer hier *Onderdeel uit-signaal* in.
