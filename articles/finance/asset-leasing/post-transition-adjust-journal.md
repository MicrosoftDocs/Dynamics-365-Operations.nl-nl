---
title: Journaalboeking voor transitiecorrectie boeken in Activa leasen
description: In dit onderwerp wordt de functionaliteit beschreven waarmee u een leaseportefeuille kunt overzetten naar de nieuwe boekhoudstandaarden voor leases, Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51ae41e22507d77f32b8b0f4685cce797fd19cff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969548"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Journaalboeking voor transitiecorrectie boeken in Activa leasen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de functionaliteit beschreven waarmee u een lease portfolio kunt overzetten naar de nieuwe boekhoudstandaarden voor leases: Accounting Standards Codification Topic 842 (ASC 842), de standaard voor algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (US GAAP) en International Financial Reporting Standard 16 (IFRS 16).

Zie [Leaseboeken instellen](set-up-lease-books.md) voor informatie over het overzetten van een boek naar de nieuwe standaarden.

Wanneer u een journaalboeking voor transitiecorrectie maakt, wordt er een journaalboeking gegenereerd. Deze boeking weerspiegelt het effect op de balans van het vastleggen van de lease volgens de nieuwe standaarden op die datum. De betreffende activumrekening wordt gedebiteerd voor de boekwaarde op die datum en de passivarekening wordt gecrediteerd. Het verschil wordt gedebiteerd of gecrediteerd op ingehouden inkomsten.

Voer de volgende stappen uit om een transitiecorrectie te boeken conform de nieuwe boekhoudstandaarden.

1. Selecteer de lease op de pagina **Lease-overzicht** en selecteer vervolgens **Boeken**.
2. Selecteer **Betalingsschema** in het boek.
3. Selecteer **Bevestigen** in het dialoogvenster **Betalingsschema**. Sluit vervolgens het dialoogvenster.
4. Selecteer **Transitiecorrectie**.

    > [!NOTE]
    > Een transitiecorrectie kan alleen worden gemaakt voor leaseboeken die zijn toegewezen aan een boek waarin het veld **Transitieboek** beschikbaar is. Als de waarde in het veld **Begin van lease** later valt dan de transitiedatum, wordt de waarde in het veld **Transitiecorrectie** niet bijgewerkt.

5. Selecteer **Activaleasejournalen** om de boeking het journaal weer te geven.
6. Selecteer het nieuwe journaal en selecteer vervolgens **Boeken**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]