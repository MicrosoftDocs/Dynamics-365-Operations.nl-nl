---
title: Een experiment instellen
description: In dit artikel wordt beschreven hoe u een experiment in een service van derden instelt.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946161"
---
# <a name="set-up-an-experiment"></a>Een experiment instellen

Nadat u [een hypothese hebt gedefinieerd en hebt bepaald welke metrische gegevens voor succes u wilt gebruiken](experimentation-identify.md), moet u uw experiment instellen in de service van derden. In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke artikelen behandeld.

[ ![Traject van gebruiker voor experimenten - instellen.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Uw experiment in de service van derden instellen
U moet een service van derden hebben gekozen om uw experiment uit te voeren en te controleren en om de experimentconnector in te stellen. Deze voorwaarden worden vermeld in [Experimenten in Dynamics 365 Commerce](experimentation-overview.md).

Voer de stappen uit die nodig zijn om uw experiment te maken in de service van derden. Als de connector juist is geconfigureerd, wordt de volledige lijst met experimenten die u in de service van derden hebt ingesteld, binnen ongeveer 5 minuten in Commerce Site Builder weergegeven.

## <a name="set-up-your-success-metrics"></a>Uw metrische gegevens voor succes instellen
Voor elk experiment zijn metrische gegevens nodig om de impact van de variaties te meten en de hypothese te valideren. Voer de volgende stappen uit om de berekening van metrische gegevens in de service van derden via live telemetrie-gebeurtenissen in te schakelen in Dynamics 365 Commerce.

Volg deze stappen om uw metrische gegevens voor succes in te stellen voor kant-en-klare modules.

1. Selecteer in Commerce Site Builder **Pagina's** in het linkernavigatievenster en selecteer vervolgens de pagina waarvoor u metrische gegevens wilt verzamelen. 
1. Ga naar de sectie **Bij te houden gebeurtenis-ID´s** in het eigenschappenvenster aan de rechterzijde van de pagina of module die u wilt bijhouden.
1. Selecteer **Weergeven**. Er wordt een lijst weergegeven met alle klikgebeurtenis-id's. Kopieer de gebeurtenis die u wilt bijhouden en plak de gebeurtenissleutel op de opgegeven locatie in de service van derden. Als u meer dan één gebeurtenis nodig hebt, kopieert u de sleutels een voor een. 
1. Voor paginaweergaven gebruikt u de SHA-256-hashwaarde van de paginanaam in Site Builder en voegt u hieraan `.PageView` toe. De gebeurtenis-id voor `Homepage.PageView` zou bijvoorbeeld `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9` zijn.
1. Voer eventuele andere stappen uit voor het bijhouden van metrische gegevens zoals in de service van derden is vereist.

Volg deze stappen om de klikgebeurtenissen te instrumenteren voor aangepaste moduleklikken:

1. Gebruik de onderstaande functie om een object **TelemetryContent** voor te bereiden. Met deze functie worden de paginanaam, de modulenaam en het door de SDK geleverde standaard telemetrieobject als invoer gebruikt.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Hier volgt een voorbeeld: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Maak de nettoladinggegevens die informatie bevatten over wat er moet worden vastgelegd. Voor knoppen en andere statische besturingselementen kunt u **etext** opnemen, zoals 'Nu winkelen' of 'Zoeken'. En voor componenten met klikken, bijvoorbeeld klikken op een productkaart, kunt u de **recid** verzenden. Dit is de record-id van het product of de product-id.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Als voorbeeld voor statische besturingselementen geeft u de tekenreeks voor de knoptekst door zoals hieronder wordt weergegeven:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Als een voorbeeld van productklikken geeft u de recordId voor het product door zoals hieronder wordt weergegeven:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Roep de functie **OnClick** aan om de gebeurtenis te registreren.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Hier volgt een voorbeeld:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Vorige stap
[Een hypothese opstellen en metrische gegevens bepalen voor een experiment](experimentation-identify.md) 


## <a name="next-step"></a>Volgende stap
[Een experiment verbinden en bewerken](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
