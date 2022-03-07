---
title: Voorspellingen voor klantbetalingen inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e10aa9342ec9f089ef8ecec5e1221a31c580fc87
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644988"
---
# <a name="enable-customer-payment-predictions-preview"></a>Voorspellingen voor klantbetalingen inschakelen (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten. U schakelt de functie in het werkgebied **Functiebeheer** in en voert de configuratie-instellingen in op de pagina **Parameters voor financiële inzichten**. Dit onderwerp bevat ook informatie die u kan helpen bij het effectief gebruik van de functie.

> [!NOTE]
> Voordat u de volgende stappen uitvoert, moet u controleren of u de vereiste stappen in het onderwerp [Configureren voor Financiële inzichten](configure-for-fin-insites.md) hebt voltooid.

1. Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving. Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving. (Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED, PARTITION) VALUES ('PayPredEnableFeature', 1, 5637144576)`

    > [!NOTE]
    > Als uw implementatie van Microsoft Dynamics 365 Finance een Service Fabric-implementatie is, kunt u deze stap overslaan. Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld. Als de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.

2. Schakel de functie Inzichten in klantbetalingen in:

    1. Ga naar **Systeembeheer \> Werkruimten \> Functiebeheer**.
    2. Zoek de functie met de naam **Inzichten in klantbetalingen (preview)**.
    3. Selecteer **Nu inschakelen**.

    De functie Inzichten in klantbetalingen is nu ingeschakeld en kan worden geconfigureerd.

3. Configureer de functie Inzichten in klantbetalingen:

    1. Ga naar **Crediteringen en aanmaningen \> Instellen \> Financiële inzichten \> Parameters voor financiële inzichten**.

        [![Pagina Parameters voor financiële inzichten voordat de functie is geconfigureerd](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)

    2. Selecteer op de pagina **Parameters voor financiële inzichten** op het tabblad **Inzichten in klantbetalingen** de koppeling **De gegevensvelden weergeven die worden gebruikt in het voorspellingsmodel** om de pagina **Gegevensvelden voor voorspellingsmodel** te openen. Hier kunt u de standaardlijst weergeven met velden die worden gebruikt om het AI-voorspellingsmodel te maken voor voorspellingen van klantbetalingen.

        Als u de standaardlijst met velden wilt gebruiken om het voorspellingsmodel te maken, sluit u de pagina **Gegevensvelden voor voorspellingsmodel** en stelt u vervolgens op de pagina **Parameters voor financiële inzichten** de optie **Functie inschakelen** in op **Ja**.

    3. Geef de transactieperiode 'zeer laat' op om aan te geven wat de **zeer late** voorspellingsbucket voor uw bedrijf betekent.

        Voor elke openstaande factuur wordt de betalingswaarschijnlijkheid in drie buckets voorspeld: **op tijd**, **te laat** en **zeer laat**.

        - **Op tijd**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze op of vóór de vervaldatum van de transactie worden betaald.
        - **Te laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na de vervaldatum van de transactie worden betaald, maar vóór het begin van de 'zeer late' transactieperiode.
        - **Zeer laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na het begin van de 'zeer late' transactieperiode worden betaald.

        > [!NOTE]
        > Als u de 'zeer late' transactieperiode wijzigt en **Drempel voor te laat wijzigen** selecteert nadat het AI-voorspellingsmodel voor klantbetalingen is gemaakt, wordt het bestaande voorspellingsmodel verwijderd en wordt er een nieuw model gemaakt. Met het nieuwe voorspellingsmodel worden transacties naar de 'zeer late' periode verplaatst op basis van de instellingen die zijn ingevoerd om deze te definiëren.

    4. Wanneer u de 'zeer late' transactieperiode hebt gedefinieerd, selecteert u **Voorspellingsmodel maken** om het voorspellingsmodel te maken. In de sectie **Voorspellingsmodel** op de pagina **Parameters voor financiële inzichten** wordt de status van het voorspellingsmodel weergegeven.

        > [!NOTE]
        > Wanneer het voorspellingsmodel wordt gemaakt, kunt u **Modelaanmaak opnieuw instellen** selecteren om het proces opnieuw te starten.

    De functie is nu geconfigureerd en kan worden gebruikt.

Nadat de functie is ingeschakeld en geconfigureerd en het voorspellingsmodel is gemaakt en werkt, wordt in het gedeelte **Voorspellingsmodel** van de pagina **Parameters voor financiële inzichten** de nauwkeurigheid van het model weergegeven, zoals wordt weergegeven in de volgende afbeelding.

[![Nauwkeurigheid van het voorspellingsmodel op de pagina Parameters voor financiële inzichten](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)

## <a name="release-details"></a>Releasegegevens

De openbare preview van Financiële inzichten is beschikbaar voor proefimplementaties in de Verenigde Staten van Amerika, Europa en het Verenigd Koninkrijk. Microsoft voegt incrementeel ondersteuning toe voor meer regio's.

Functies van de openbare preview kunnen en zouden alleen moeten worden ingeschakeld in Tier-2 sandbox-omgevingen. Setup-modellen en AI-modellen die in een sandbox-omgeving zijn gemaakt, kunnen niet naar een productieomgeving worden gemigreerd. Zie voor meer informatie [Aanvullende gebruiksrechtovereenkomst voor Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).

## <a name="privacy-notice"></a>Privacyverklaring

Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.
