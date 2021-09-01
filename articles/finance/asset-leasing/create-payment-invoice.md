---
title: Betalingsfacturen maken
description: In dit onderwerp wordt uitgelegd hoe u maandelijkse leasefacturen maakt. U kunt facturen maken voor afzonderlijke leases of u kunt een batchproces gebruiken om deze voor meerdere leases te maken.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePaymentSchedule
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 94657a1c423fafb89d2fe2c16937947e0d898771ddb30a029d0938cc17aaf7d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716664"
---
# <a name="create-payment-invoices"></a>Betalingsfacturen maken

[!include [banner](../includes/banner.md)]

U kunt maandelijkse facturen maken voor afzonderlijke leases of u kunt een batchproces gebruiken om deze voor meerdere leases te maken. Met de volgende procedure wordt aangegeven hoe u een individuele leasebetalingspost kunt maken wanneer de parameter **Betalen aan leverancier** op de pagina **Leaseboek instellen** is ingeschakeld.

1. Selecteer op de pagina **Lease-overzicht** een lease en selecteer vervolgens **Boeken \> Betalingsschema**.
2. Selecteer de betaling die moet worden uitgevoerd en selecteer **Journaal maken**. U ontvangt een bericht met de mededeling dat er een journaal is gemaakt voor de geselecteerde betaling.
3. Selecteer **Factuurjournalen** en selecteer vervolgens de factuur die moet worden betaald.
4. Bekijk op het tabblad **Regels** de journaalpost voordat u deze naar het grootboek boekt.

    > [!NOTE]
    > De leveranciersfactuurregels die worden gemaakt, gebruiken standaard het boekingsprofiel van de leverancier van de pagina **Parameters van module Leveranciers**.

5. Selecteer het juiste journaal en selecteer vervolgens de factuur die moet worden betaald.

    Voor dit voorbeeld is de parameter **Betalen aan leverancier** op het leaseboek ingeschakeld. De factuur wordt daarom in het factuurjournaal opgenomen. In de sectie **Overzicht** wordt een overzicht van de journaalpost weergegeven en de sectie **Regels** bevat details van de werkelijke journaalregels.

    > [!NOTE]
    > Als de parameter **Betalen aan leverancier** is uitgeschakeld, worden de betalingsjournaalposten weergegeven op de pagina **Activa leasen** voor het leaseboek en wordt er een post voor activa leasen gemaakt in plaats van een factuur. De leasebetalingspost wordt geboekt naar de journaalnaam die is opgegeven in het veld **Maandelijks leasejournaal**.

6. Nadat de transactie is geboekt, kunt u de transactiegegevens en de boekwaarde van de leaseverplichtingen weergeven door **Transacties verplichtingen** in het leaseboek te selecteren.

    In het betalingsschema is het selectievakje **Journaal geboekt** ingeschakeld en geeft de regel het factuurjournaalnummer weer. Nadat een betalingsjournaal en een post voor dat journaal zijn gemaakt, moet u de post terugboeken voordat u deze opnieuw kunt maken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
