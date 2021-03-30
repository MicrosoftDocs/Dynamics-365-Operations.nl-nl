---
title: Gegevens van de dochtermaatschappij exporteren naar bestanden
description: In dit onderwerp wordt uitgelegd hoe u de exportgegevens van Microsoft Dynamics 365 Finance voorbereidt en deze vervolgens in een geconsolideerde rechtspersoon importeert.
author: jinniew
manager: AnnBe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 33c17cc2c1dcaa57244bf0bfaa661b11b221e2f6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205494"
---
# <a name="export-subsidiary-data-to-files"></a>Gegevens van de dochtermaatschappij exporteren naar bestanden

[!include [banner](../includes/banner.md)]

U gebruikt te pagina **Exporteren** (**Systeembeheer \> Werkruimten \> Importeren/exporteren**) om gegevens van de dochtermaatschappij to te exporteren naar bestanden die vervolgens kunnen worden geïmporteerd in een geconsolideerde rechtspersoon. Meer informatie over het import- en exportproces vindt u in [Overzicht van gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Maak een rechtspersoon voor het consolidatieproces. Meer informatie over het maken van rechtspersonen vindt u in [Een rechtspersoon maken](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Meer informatie vindt u in [Een rechtspersoon voorbereiden voor gebruik in het consolidatieproces](prepare-company-for-consolidation.md) en [Een dochtermaatschappij voor consolidatie instellen](set-up-subsidiary-company-for-consolidation.md). 

2. Ga naar **Consolidaties \> Bedrijfssaldi exporteren**. Geef op de pagina **Bedrijfssaldi exporteren** op het tabblad **Criteria** de details van de consolidatie op door de volgende velden in te stellen.

    | Veld                             | Beschrijving |
    |-----------------------------------|-------|
    | Hoofdrekening                      | Geef op welke rekeningen moeten worden geconsolideerd. Als u alle rekeningen wilt meenemen, laat u dit veld leeg. |
    | Consolidatierekening gebruiken         | Als u consolidatierekeningen hebt opgegeven, stelt u deze optie in op **Ja**. |
    | Consolidatierekening selecteren in | Selecteer **Hoofdrekening** of **Consolidatierekeninggroep**. |
    | Consolidatierekeninggroep       | Selecteer een groep consolidatierekeningen voor de consolidatierekening die u hebt geselecteerd. |
    | Consolidatieperiode              | Geef datums "van" en "tot" voor de consolidatie op. |
    | Werkelijke bedragen opnemen            | Stel deze optie in op **Ja** om werkelijke bedragen op te nemen. |
    | Budgetbedragen opnemen            | Stel deze optie in op **Ja** als u budgetbedragen wilt opnemen in consolidaties. |
    | Budgetmodellen                     | Geef het budgetmodel op dat u wilt opnemen. |

3. Geef op het tabblad **Financiële dimensies** de details van de consolidatie op:

    - Geef de financiële dimensie-informatie op die moet worden overgebracht van de transacties van de dochtermaatschappijrekeningen naar de transacties in de geconsolideerde rechtspersoon.
    - Selecteer financiële dimensies in de lijst.
    - Bepaal de juiste specificatie voor elke financiële dimensie die wordt geconsolideerd. De beschikbare opties zijn **Dimensie**, **Groepdimensie**, **Bedrijfsrekeningen** en **Rekening**.

        > [!NOTE]
        > Met de optie **Groepdimensie** kunt u de dimensiewaarde definiëren die wordt gebruikt door de groep bedrijven die wordt geconsolideerd.

    - Geef de segmentvolgorde op waarin moet worden geconsolideerd.

4. Volg deze stappen op het tabblad **Rechtspersonen** om de rechtspersoon op te geven die u exporteert:

    1. Selecteer **Nieuw**.
    2. Voer in het veld **Rechtspersoon bron** de rechtspersoon in.

        Als dezelfde criteria van toepassing zijn op verschillende dochtermaatschappijen in dezelfde database, kunt u gegevens van de dochtermaatschappijen overbrengen om exportbestanden in één bewerking te scheiden:

        1. Maak een regel voor elke dochtermaatschappij waarvoor de rekeningen moeten worden geëxporteerd naar bestanden. Deze bestanden worden later geïmporteerd in de geconsolideerde rechtspersoon.
        2. Voer voor elke dochtermaatschappij de naam van de dochtermaatschappij en de naam van het exportbestand in die worden gemaakt tijdens de exporttaak.

    3. Selecteer in het veld **Rekeningtype voor omrekeningsverschillen** de optie **Winst en verlies** of **Balans**.
    4. Voer een bestandsnaam in voor het exportbestand dat wordt gemaakt.

5. Selecteer **OK** om te exporteren.

Wanneer de export is voltooid, ontvangt u een bericht waarin het aantal records wordt weergegeven dat is opgeslagen in elk bestand. U kunt de bestanden vervolgens importeren in de geconsolideerde rechtspersoon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]