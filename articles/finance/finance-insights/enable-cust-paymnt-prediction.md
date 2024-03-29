---
title: Voorspellingen voor klantbetalingen inschakelen
description: In dit artikel wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Finance Insights.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f04ee9db5efe3595dea30d641c5097d6b90c0d77
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898202"
---
# <a name="enable-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen inschakelen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u de functie Voorspellingen voor klantbetalingen kunt inschakelen en configureren in Finance Insights. U schakelt de functie in het werkgebied **Functiebeheer** in en voert de configuratie-instellingen in op de pagina **Finance Insights-configuratie**. Dit artikel bevat ook informatie die u kan helpen bij het effectief gebruik van de functie.

> [!NOTE]
> Voordat u de volgende stappen uitvoert, moet u controleren of u de vereiste stappen in het artikel [Configureren voor Finance Insights](configure-for-fin-insites.md) hebt voltooid.

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
        
   > [!NOTE]
   > Voor de functie **Voorspellingen voor klantbetalingen** moeten meer dan 100 transacties zijn uitgevoerd in de voorgaande zes tot negen maanden. De transacties kunnen vrije-tekstfacturen, verkooporders en klantbetalingen omvatten. Deze gegevens moeten worden verdeeld over de instellingen voor **Op tijd**, **Te laat** en **Erg laat**.    
     

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
