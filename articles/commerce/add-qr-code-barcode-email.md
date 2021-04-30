---
title: Een QR-code of streepjescode toevoegen aan transactionele e-mails en ontvangstberichten
description: In dit onderwerp wordt uitgelegd hoe u QR-codes en streepjescodes die order-id's vertegenwoordigen kunt invoegen in transactionele e-mails en ontvangstberichten in Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 03/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Commerce, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-02-16
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 791b244c867ea4263f08250abf220a1b75784cad
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907858"
---
# <a name="add-a-qr-code-or-bar-code-to-transactional-and-receipt-emails"></a>Een QR-code of streepjescode toevoegen aan transactionele e-mails en ontvangstberichten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u QR-codes en streepjescodes die order-id's vertegenwoordigen kunt invoegen in transactionele e-mails en ontvangstberichten in Microsoft Dynamics 365 Commerce.

U kunt eenvoudig QR-codes en streepjescodes in transactionele e-mails opnemen, zodat het opzoekproces voor orders in een detailhandelomgeving wordt versneld. Als u QR-codes en streepjescodes wilt invoegen in e-mails, gebruikt u een HTML **\<img\>**-code waarin wordt gevraagd om een QR-code of streepjescodeafbeelding van een generatie- en renderingservice. Microsoft levert deze service niet. Er bestaat echter een groot aantal gratis of voordelige services waarmee u QR-codes of streepjescodes kunt gebruiken die dynamisch worden gegenereerd op basis van een waarde die wordt doorgegeven in een queryreeks.

## <a name="add-a-qr-code-or-bar-code-to-a-transactional-email"></a>Een QR-code of streepjescode toevoegen aan een transactionele e-mail

Volg deze stappen om een QR-code of streepjescode in te voegen in een transactioneel e-mailbericht dat als onderdeel van een e-commerce-aankoop wordt verzonden.

1. Open de bron-HTML voor de transactionele e-mailsjabloon en voeg een HTML **\<img\>**-code toe die naar uw QR-code- of streepjescodeservice wijst. Hier volgt een voorbeeld.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%salesid%&param1=value1&param2=value2" alt="%salesid%" />
    ```

    Hier volgt een uitleg van het voorafgaande voorbeeld:

    - **UW\_QR\_CODE\_STREEPJES\_CODE\_SERVICE** stelt het domein van uw QR-code- of streepjescodeservice voor.
    - **gegevens** vertegenwoordigt de parameter die door de QR-code- of streepjescodeservice wordt gebruikt voor de ontvangst van de inhoud die moet worden weergegeven als QR-code of streepjescode.

        De waarde **%salesid%** moet aan deze parameter worden toegewezen. In dit voorbeeld wordt de waarde ook gebruikt als alt-tekst voor de afbeelding.

    - **param1** en **param2** staan voor extra optionele parameters.

1. Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie** en upload de bijgewerkte HTML naar de juiste transactionele e-mailsjabloon.

> [!NOTE]
> De parameters kunnen per provider verschillen voor de QR-code- en streepjescodeservice. Neem daarom contact op met uw serviceprovider om de parameters te bevestigen waaraan u waarden moet toewijzen.

## <a name="add-a-qr-code-or-bar-code-to-a-receipt-email"></a>Een QR-code of streepjescode toevoegen aan een ontvangstbericht 

Volg deze stappen om een QR-code of streepjescode in te voegen in een ontvangstbericht dat kan worden verzonden nadat een inkoop op het POS is gedaan.

1. Open de bron-HTML voor de e-mailsjabloon voor ontvangstbericht en voeg een HTML **\<img\>**-code toe die naar uw QR-code- of streepjescodeservice wijst. Hieronder volgt een voorbeeld.

    ```HTML
    <img src="https://YOUR_QR_CODE_BAR_CODE_SERVICE?data=%receiptid%&param1=value1&param2=value2" alt="%receiptid%" />
    ```

    Hier volgt een uitleg van het voorafgaande voorbeeld:

    - **UW\_QR\_CODE\_STREEPJES\_CODE\_SERVICE** stelt het domein van uw QR-code- of streepjescodeservice voor.
    - **gegevens** vertegenwoordigt de parameter die door de QR-code- of streepjescodeservice wordt gebruikt voor de ontvangst van de inhoud die moet worden weergegeven als QR-code of streepjescode.

        De waarde **%receiptid%** moet aan deze parameter worden toegewezen. In dit voorbeeld wordt de waarde ook gebruikt als alt-tekst voor de afbeelding.

    - **param1** en **param2** staan voor extra optionele parameters.

1. Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Parameters \> E-mailsjablonen van organisatie** en upload de bijgewerkte HTML naar de e-mailsjabloon met de e-mail-id **emailrecpt**.

> [!NOTE]
> De parameters kunnen per provider verschillen voor de QR-code- en streepjescodeservice. Neem daarom contact op met uw serviceprovider om de parameters te bevestigen waaraan u waarden moet toewijzen.

## <a name="additional-resources"></a>Aanvullende bronnen

[E-mailontvangstbewijzen verzenden vanuit Modern POS](email-receipts.md)

[E-mailsjablonen maken voor transactiegebeurtenissen](email-templates-transactions.md)
