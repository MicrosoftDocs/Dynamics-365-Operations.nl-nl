---
title: Voorspellingen voor klantbetalingen inschakelen
description: In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 16ccd7f2e11f0b46aaa646de272e668d29ccc0c0
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752923"
---
# <a name="enable-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen inschakelen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Financiële inzichten. U schakelt de functie in het werkgebied **Functiebeheer** in en voert de configuratie-instellingen in op de pagina **Finance Insights-configuratie**. Dit onderwerp bevat ook informatie die u kan helpen bij het effectief gebruik van de functie.

> [!NOTE]
> Voordat u de volgende stappen uitvoert, moet u controleren of u de vereiste stappen in het onderwerp [Configureren voor Financiële inzichten](configure-for-fin-insites.md) hebt voltooid.

1. Schakel de functie Voorspellingen voor klantbetalingen in:

    1. Open het het werkgebied **Functiebeheer**.
    2. Selecteer **Controleren op updates**.
    3. Zoek op het tabblad **Alle** naar **Voorspellingen voor klantbetalingen**. Als u die functie niet kunt vinden, zoekt u naar **(Preview) Voorspellingen voor klantbetalingen**. 
    4. Schakel de functie in.

    De functie Voorspellingen voor klantbetalingen is nu ingeschakeld en kan worden geconfigureerd.

2. Configureer de functie Inzichten in klantbetalingen:

    1. Ga naar **Crediteringen en aanmaningen \> Instellen \> Finance Insights \> Voorspellingen voor klantbetalingen**.
    2. Selecteer op de pagina **Finance Insights-configuratie** op het tabblad **Voorspellingen voor klantbetalingen** de optie **De gegevensvelden weergeven die worden gebruikt in het voorspellingsmodel** om de pagina **Gegevensvelden voor voorspellingsmodel** te openen. Hier kunt u de standaardlijst weergeven met velden die worden gebruikt om het AI-voorspellingsmodel te maken voor voorspellingen van klantbetalingen.

        Als u de standaardlijst met velden wilt gebruiken om het voorspellingsmodel te maken, sluit u de pagina **Gegevensvelden voor voorspellingsmodel** en stelt u vervolgens op de pagina **Finance Insights-configuratie** de optie **Functie inschakelen** in op **Ja**.

    3. Geef de transactieperiode 'zeer laat' op om aan te geven wat de **zeer late** voorspellingsbucket voor uw bedrijf betekent.

        Voor elke openstaande factuur wordt de betalingswaarschijnlijkheid in drie buckets voorspeld: **op tijd**, **te laat** en **zeer laat**.

        - **Op tijd**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze op of vóór de vervaldatum van de transactie worden betaald.
        - **Te laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na de vervaldatum van de transactie worden betaald, maar vóór het begin van de 'zeer late' transactieperiode.
        - **Zeer laat**: deze bucket bevat betalingen waarvan wordt voorspeld dat ze na het begin van de 'zeer late' transactieperiode worden betaald.

        > [!NOTE]
        > Als u de 'zeer late' transactieperiode wijzigt en **Drempel voor te laat wijzigen** selecteert nadat het AI-voorspellingsmodel voor klantbetalingen is gemaakt, wordt het bestaande voorspellingsmodel verwijderd en wordt er een nieuw model gemaakt. Met het nieuwe voorspellingsmodel worden transacties naar de 'zeer late' periode verplaatst op basis van de instellingen die zijn ingevoerd om deze te definiëren.

    4. Wanneer u de 'zeer late' transactieperiode hebt gedefinieerd, selecteert u **Voorspellingsmodel maken** om het voorspellingsmodel te maken. In de sectie **Voorspellingsmodel** op de pagina **Finance Insights-configuratie** wordt de status van het voorspellingsmodel weergegeven.

        > [!NOTE]
        > Wanneer het voorspellingsmodel wordt gemaakt, kunt u **Modelaanmaak opnieuw instellen** selecteren om het proces opnieuw te starten.

    De functie is nu geconfigureerd en kan worden gebruikt.

Nadat de functie is ingeschakeld en geconfigureerd en het voorspellingsmodel is gemaakt en werkt, wordt in het gedeelte **Voorspellingsmodel** van de pagina **Finance Insights-parameters** de nauwkeurigheid van het model weergegeven.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
