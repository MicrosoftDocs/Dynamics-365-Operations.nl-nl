---
title: Het scenario productkwaliteit
description: Dit artikel bevat informatie over het scenario productkwaliteit. In dit scenario wordt een sensor gebruikt om de kwaliteit van een productbatch te meten en wordt een waarschuwing gegenereerd als een meting buiten een gedefinieerde drempel valt.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreScenarioManagement, IoTIntCoreNotification, IoTIntMfgResourceStatusConfiguration, IoTIntMfgResourceStatus
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 8c4808ea3a0389c2a8699f0e11ea154705a6916d
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428314"
---
# <a name="the-product-quality-scenario"></a>Het scenario productkwaliteit

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

In het scenario *productkwaliteit* wordt een sensor geconfigureerd om de kwaliteit van een productbatch op de werkvloer te meten. Als een meting buiten een gedefinieerde drempel voor het product valt, wordt een melding weergegeven op het dashboard van de supervisor. Een sensor meet bijvoorbeeld het vochtgehalte van een voedingsproduct dat uit de productieregel afkomstig is. Als de meting buiten de toegestane minimum- of maximumwaarde voor vochtgehalte voor het product valt, wordt een melding gegenereerd.

## <a name="scenario-dependencies"></a>Afhankelijkheden voor dit scenario

Het scenario *Productkwaliteit* heeft de volgende afhankelijkheden:

- Er kan alleen een waarschuwing worden gegenereerd als een productieorder wordt uitgevoerd op een toegewezen machine en die machine een product met een toegewezen batchkenmerk produceert.
- Er moet een signaal dat overeenkomt met het batchkenmerk met een unieke eigenschapsnaam naar de IoT-hub worden verzonden.

## <a name="prepare-demo-data-for-the-product-quality-scenario"></a>Demogegevens voorbereiden voor het scenario productkwaliteit

Als u een demonstratiesysteem wilt gebruiken om het scenario *productkwaliteit* te testen, gebruikt u een systeem waarop de [demonstratiegegevens](../../fin-ops-core/fin-ops/get-started/demo-data.md) zijn geïnstalleerd, selecteert u de rechtspersoon *USMF* (bedrijf) en bereidt u de aanvullende demonstratiegegevens voor, zoals wordt beschreven in deze sectie. U kunt deze sectie overslaan als u uw eigen sensoren en gegevens gebruikt.

In deze sectie stelt u de demonstratiegegevens in, zodat u vrijgegeven product *P0111* (*Composite Case)* kunt gebruiken met het scenarion *productkwaliteit*. In dit scenario wordt bijgehouden of een batchkenmerkwaarde die wordt gemeten met een sensor, buiten de gedefinieerde drempel voor een batchkenmerk valt dat aan het product is gekoppeld.

### <a name="set-up-a-sensor-simulator"></a>Een sensorsimulator instellen

Als u dit scenario wilt uitproberen zonder een fysieke sensor te gebruiken, kunt u een simulator instellen om de vereiste signalen te genereren. Meer informatie over dit onderwerp vindt u in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md).

### <a name="associate-a-batch-attribute-and-resource-with-product-p0111"></a>Een batchkenmerk en resource koppelen aan product P0111

Volg deze stappen om een batchkenmerk te koppelen aan product *P0111* (*Composite Case*) en om te controleren of resource *3118* (*Foam cutting machine*) voor dit product wordt gebruikt.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer het product waarvan het veld **Artikelnummer** is ingesteld op *P0111*.
1. Klik op het tabblad **Voorraad beheren** van het Actievenster in de groep **Batchkenmerken** op **Productgebonden**.
1. Selecteer op de pagina **Productgebonden** de optie **Nieuw** om een productgebonden batchkenmerk te maken.
1. Stel in de koptekst de volgende velden in:

    - **Kenmerkcode**: selecteer de scope van kenmerken die u wilt controleren (*Tabel*, *Groep* of *Alle*). Selecteer *Tabel* voor dit scenario, omdat u altijd slechts één kenmerk zult controleren.
    - **Kenmerkrelatie**: selecteer het kenmerk dat u gebruikt voor het scenario *productkwaliteit* voor het controleren van de waarde. Selecteer bijvoorbeeld *Concentratie*, een kenmerk dat in de standaarddemogegevens is opgenomen.

1. Definieer op het sneltabblad **Waarden** in de velden **Minimum** en **Maximum** het bereik met acceptabele waarden dat het kenmerk moet melden om te slagen voor de kwaliteitscontrole. Als een sensor een waarde buiten dit bereik meldt, wordt deze door het systeem als een kwaliteitsovertreding geconstateerd. De andere velden op dit sneltabblad zijn niet relevant voor het scenario *productkwaliteit*. De standaardwaarden die u hier momenteel ziet, zijn afkomstig uit de demonstratiegegevens. Laat deze daarom zoals ze zijn en sluit de pagina **Productgebonden** om terug te keren naar de pagina **Vrijgegeven productdetails** voor artikel *P0111*.
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

## <a name="set-up-the-product-quality-scenario"></a>Het scenario productkwaliteit instellen

Volg deze stappen om het scenario *productkwaliteit* in te stellen in Supply Chain Management.

1. Ga naar **Productiebeheer \> Instellingen \> Sensor Data Intelligence \> Scenario's**.
1. Selecteer in het vak van het scenario **productkwaliteit** de optie **Configureren** om de configuratiewizard voor dit scenario te openen.
1. Selecteer op de pagina **Sensoren** de optie **Nieuw** om een sensor toe te voegen aan het raster. Stel er daarna de volgende velden voor in:

    - **Sensor-ID**: voer de id in van de sensor die u gebruikt Als u de Raspberry Pi Azure IoT Online Simulator gebruikt en deze hebt ingesteld zoals beschreven in [Een gesimuleerde sensor instellen voor tests](sdi-set-up-simulated-sensor.md), voer dan *Kwaliteit* op.
    - **Beschrijving van de sensor**: voer een beschrijving van de sensor in.

1. Herhaal nu de vorige stap voor elke extra sensor die u wilt toevoegen. U kunt later op elk moment terug komen en meer sensoren toevoegen.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Toewijzing van bedrijfsrecord** in de sectie **Sensoren** de record voor een van de sensoren die u zojuist hebt toegevoegd.
1. Selecteer in het gedeelte **Toewijzing van bedrijfsrecord** de optie **Nieuw** om een rij aan het raster toe te voegen.
1. In de nieuwe rij moet het veld **Type bedrijfsrecord** automatisch zijn ingesteld op *Resources(WrkCtrTable)*. Stel het veld **Bedrijfsrecord** in op de resource die u wilt bewaken met de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit in op *3118, Foam cutting machine*.
1. Direct nadat u een type bedrijfsrecord hebt geselecteerd voor de rij die u in de vorige stap hebt toegevoegd, wordt automatisch een tweede rij aan het raster toegevoegd. In deze rij moet het veld **Type bedrijfsrecord** zijn ingesteld op *Batchkenmerken(PdsBatchAttrib)*. Stel het veld **Bedrijfsrecord** in op het batchkenmerk dat u wilt bewaken met de geselecteerde sensor. Als u gebruik maakt van de demogegevens die u eerder in dit artikel hebt gemaakt, stelt u dit in op *Concentratie, Concentratiepercentage*.
1. Selecteer **Volgende**.
1. Selecteer op de pagina **Sensors activeren** in het raster de sensor die u toegevoegd hebt en selecteer vervolgens **Activeren**. Voor elke geactiveerde sensor in het raster wordt een vinkje weergegeven in de kolom **Actief**.
1. Selecteer **Voltooien**.

## <a name="work-with-the-product-quality-scenario"></a>Werken met het scenario productkwaliteit

### <a name="view-product-quality-data-on-the-resource-status-page"></a>Productkwaliteitsgegevens weergeven op de pagina Resourcestatus

Op de pagina **Resourcestatus** kunnen supervisors een tijdlijn controleren van het signaal van de productkwaliteit dat wordt ontvangen van de sensoren die zijn toegekend aan elke machineresource. Volg deze stappen om de tijdlijn te configureren:

1. Ga naar **Productiebeheer \> Productieregistratie \> Resourcestatus**.
1. Stel in het dialoogvenster **Configureren** de volgende velden in:

    - **Resource**: selecteer de resources die u wilt bewaken. Als u met de demonstratiegegevens werkt, selecteert u *3118*.
    - **Tijdreeks 1**: selecteer de record (metrische sleutel) met de volgende notatie voor de naam: *productQuality:&lt;TaakID:&gt;:&lt;Kenmerknaam&gt;*
    - **Weergavenaam**: voer hier *Batchkenmerkwaarden* in.

De onderstaande afbeelding toont een voorbeeld van productkwaliteitsgegevens op de pagina **Resourcestatus**, wanneer de waarde binnen het bereik van acceptabele waarden valt.

![Productkwaliteitsgegevens op de pagina Resourcestatus wanneer de waarde binnen het bereik valt.](media/sdi-product-quality-in-range.png "Productkwaliteitsgegevens op de pagina Resourcestatus wanneer de waarde binnen het bereik valt")

In de volgende afbeelding ziet u een voorbeeld van kwaliteitsgegevens van producten wanneer een waarde buiten een bereik wordt gedetecteerd.

![Productkwaliteitsgegevens op de pagina Resourcestatus wanneer een waarde buiten het bereik is gedetecteerd.](media/sdi-product-quality-out-of-range.png "Productkwaliteitsgegevens op de pagina Resourcestatus wanneer een waarde buiten het bereik is gedetecteerd")

### <a name="view-product-quality-data-on-the-notifications-page"></a>Productkwaliteitsgegevens weergeven op de pagina Meldingen

Op de pagina **Meldingen** kunnen supervisors de meldingen weergeven die worden gegenereerd wanneer de sensor een batchkenmerkwaarde meet die buiten de gedefinieerde drempel voor het batchkenmerk valt. Elke melding geeft een overzicht van de productietaak die wordt beïnvloed door de uitval en geeft de optie om de beïnvloede taak opnieuw toe te kennen aan een andere resource.

Om de pagina **Meldingen** te openen, gaat u naar **Productiebeheer \> Query's en rapporten \> Sensor Data Intelligence \> Meldingen**.

In de volgende afbeelding ziet u een voorbeeld van een melding voor productkwaliteit.

![Voorbeeld van een melding voor productkwaliteit.](media/sdi-product-quality-notification.png "Voorbeeld van een melding voor productkwaliteit")
