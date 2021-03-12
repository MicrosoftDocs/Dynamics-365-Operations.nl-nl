---
title: Gegevens van de dochtermaatschappij importeren vanuit bestanden
description: In dit onderwerp wordt uitgelegd hoe u gegevens van externe systemen voorbereidt zodat u deze in Microsoft Dynamics 365 Finance kunt importeren.
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 7ced1b970aefa20a27ab16e005dff8fabace78d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988816"
---
# <a name="import-subsidiary-data-from-files"></a>Gegevens van de dochtermaatschappij importeren vanuit bestanden

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u gegevens van externe systemen voorbereidt zodat u deze in Microsoft Dynamics 365 Finance kunt importeren. Met de pagina **Consolidatie met import** (**Consolidaties \> Consolidatie met import**) kunt u de overdracht van gegevens van dochtermaatschappijen vanuit externe systemen voorbereiden.

1. Maak een dochtermaatschappij voor de consolidatie. Meer informatie over het maken van rechtspersonen vindt u in [Een rechtspersoon maken](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Meer informatie vindt u in [Een rechtspersoon voorbereiden voor gebruik in het consolidatieproces](prepare-company-for-consolidation.md) en [Een dochtermaatschappij voor consolidatie instellen](set-up-subsidiary-company-for-consolidation.md).

2. Bereid een bestand voor met de gegevens die u wilt importeren. Meer informatie over het importproces vindt u in [Overzicht van gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).
3. Exporteer de gegevens naar een bestand volgens de stappen in de procedure 'Proces voor importeren/exporteren van gegevens' in [Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md). Met deze procedure kunt u gegevens consolideren vanuit een ander exemplaar van Dynamics 365 Finance of vanuit Dynamics 365 Business Central. Als u gegevens importeert vanuit externe systemen, moeten de gegevens de indeling hebben die is beschreven in [Gegevens van dochtermaatschappijen exporteren naar bestanden](export-subsidiary-data-to-file.md).
4. Ga naar **Consolidaties \> Consolidatie online**. Geef op de pagina **Consolidatie met import** op het tabblad **Criteria** de details van het rapport en/of de import op door de volgende velden in te stellen.

    | Veld                                 | Waarde voor het rapport | Waarde voor de import |
    |---------------------------------------|----------------------|----------------------|
    | Beschrijving                           | Niet van toepassing | Voer een beschrijving in om de import te identificeren. |
    | Hoofdrekening                          | Definieer het bereik van rekeningen dat het rapport moet bevatten. Als u geen bereik definieert, worden alle rekeningen opgenomen. | Definieer het bereik van rekeningen dat de import moet bevatten. Als u geen bereik definieert, worden alle rekeningen opgenomen. |
    | Consolidatieperiode                  | Definieer het datumbereik dat moet worden geconsolideerd. | Definieer het datumbereik dat moet worden geconsolideerd. |
    | Werkelijke bedragen opnemen                | Stel deze optie in op **Ja** om werkelijke gegevens op te nemen. | Stel deze optie in op **Ja** om werkelijke gegevens op te nemen. |
    | Budgetbedragen opnemen                | Stel deze optie in op **Ja** als u budgetbedragen wilt opnemen in consolidaties. | Stel deze optie in op **Ja** als u budgetbedragen wilt opnemen in consolidaties. |
    | Saldi opnieuw opbouwen tijdens consolidatieproces | Stel deze optie in op **Ja** als het herstelproces het saldo en de nieuwe records volledig moet leegmaken en het saldo opnieuw moet opbouwen vanaf het begin van de tijd. | Stel deze optie in op **Ja** als het herstelproces het saldo en de nieuwe records volledig moet leegmaken en het saldo opnieuw moet opbouwen vanaf het begin van de tijd. |
    | Budgetmodellen                         | Niet van toepassing | Als u budgetbedragen wilt importeren, voert u de budgetmodellen in die u wilt consolideren. |
    | Koerstype budget                      | Niet van toepassing | Voer het type budgetwisselkoers in. |

6. Als u verschillende boekhoudvaluta's hebt, gebruikt u de velden op het tabblad **Valutaomzetting** om de omzetting te configureren die tijdens de consolidatie wordt uitgevoerd.

    | Veld                      | Beschrijving |
    |----------------------------|-------------|
    | Bronbedrijf        | Selecteer de rechtspersoon van waaruit u importeert. |
    | Bronvaluta | Deze standaardvaluta is de valuta die is gekoppeld aan de bronrechtspersoon die u hebt geselecteerd in het veld **Bronrechtspersoon**. |
    | Van rekening en Naar rekening       | Definieer het bereik van rekeningen dat u wilt importeren uit de bronrechtspersoon. |
    | Wisselkoerstype         | Selecteer het type van de wisselkoers. Wisselkoerstypen worden toegewezen wanneer u een hoofdrekening maakt. Zie [Een hoofdrekening maken](tasks/create-main-account.md) voor meer informatie. |
    | Wisselkoers toepassen van   | Voer een datum in om de wisselkoers toe te passen die op die datum gold. U kunt ook de waarde invoeren die als wisselkoers moet worden gebruikt. |
    | Wisselkoers              | De standaardwaarde hangt af van het type wisselkoers dat u selecteerde voor het veld **Wisselkoerstype**. Als u een door de gebruiker gedefinieerde wisselkoers hebt ingevoerd, kunt u een wisselkoers definiëren. |

7. Stel de optie **Uitvoeren in achtergrond** in op **Ja** zodat het importproces in de achtergrond kan worden uitgevoerd.
8. Stel de optie **Batchverwerking** in op **Ja** om de consolidatie te laten uitvoeren als batchtaak op een specifiek tijdstip. Selecteer **OK** als u de consolidatie onmiddellijk wilt uitvoeren. 

De transacties en saldi die zijn opgegeven voor de consolidatie in de dochtermaatschappijen worden toegevoegd aan de desbetreffende rekeningen van het geconsolideerde bedrijf.
