---
title: Certificaatnummers en -datums voor TDS-transacties bijwerken
description: In dit onderwerp wordt uitgelegd hoe u de nummers en datums van het certificaat voor terugvordering kunt bijwerken die zijn geregistreerd voor leverancier-, klant- en grootboekrekeningen voor TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023144"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a>Certificaatnummers en -datums voor TDS-transacties bijwerken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de nummers en datums van het certificaat voor terugvordering kunt bijwerken die zijn geregistreerd voor leverancier-, klant- en grootboekrekeningen voor TDS (belasting ingehouden op bron). U kunt de certificaten voor TDS-transacties weergeven op de pagina **Certificaten voor terugvordering**. U kunt de certificaten bijwerken met de pagina **Certificaten bijwerken**.

Volg deze stappen om certificaatnummers en -datums voor TDS-transacties bij te werken.

1. Ga naar **Belasting \> Aangiften \> Bronbelasting \> Certificaat bijwerken**.

    [![Pagina Certificaat bijwerken](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)

2. Selecteer **TDS** op de pagina **Certificaat bijwerken** in de sectie **Selecteren** in het veld **Belastingtype**.
3. Selecteer in het veld **Certificaatnummer** het TDS-certificaatnummer van de klant of leverancier.

    > [!NOTE]
    > Het veld **Certificaatnummer** bevat alleen TDS-certificaatnummers waar het selectievakje **Afgesloten** voor is gewist op de pagina **Certificaten voor terugvordering**.

    In het veld **Certificaatdatum** wordt de datum van het certificaat weergegeven. In het veld **Rekeningtype** wordt het type rekening vermeld waar het TDS-certificaatnummer voor wordt ontvangen, en in het veld **Naam** wordt de naam van de rekening vermeld.

5. Voer in in de velden **Begindatum** en **Einddatum** de begin- en einddatum van de periode in waarvoor u de TDS-transacties wilt weergeven.
6. Selecteer **Gegevens weergeven** om de TDS-transacties weer te geven die tijdens de geselecteerde periode zijn geboekt.

    Op het tabblad **Overzicht** bevat het raster in het bovenste deelvenster de volgende informatie over elke TDS-transactie die voor de leverancier of klant is geboekt tijdens de geselecteerde periode:

    - **Boekstuk**: het boekstuknummer van de TDS-transactie.
    - **Datum**: de vervaldatum van de TDS-transactie.
    - **Bedrag**: het factuurbedrag waarover de TDS is berekend.
    - **Belastingbedrag**: het TDS-belastingbedrag dat voor de transactie is berekend.

7. Als u specifieke TDS-transacties van het bovenste raster naar het onderste raster wilt verplaatsen, selecteert u de transacties en selecteert u **Opnemen**. U kunt ook **Alle opnemen** selecteren om alle TDS-transacties van het bovenste raster naar het onderste raster te verplaatsen.

    Als u specifieke TDS-transacties of alle TDS-transacties van het onderste raster naar het bovenste raster wilt verplaatsen, gebruikt u de knop **Uitsluiten** of **Alle uitsluiten**.

8. Selecteer **Bijwerken** om de velden **Certificaatnummer** en **Certificaatdatum** voor TDS-transacties bij te werken in het onderste raster.
10. Ga naar **Belasting \> Indirecte belasting \> Bronbelasting \> Certificaat voor terugvordering** en selecteer **Opvraag** om de bijgewerkte transactieregels weer te geven met de nieuwe certificaatnummers op de pagina **Certificaattransacties**.

    [![Certificaattransacties](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)
