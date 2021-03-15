---
title: Een rechtspersoon voorbereiden voor het consolidatieproces
description: Tijdens een consolidatie verzamelt u transacties uit meerdere reeksen rekeningen van rechtspersonen en neemt ze op in één reeks met rekeningen van rechtspersonen. In dit onderwerp wordt uitgelegd hoe u een rechtspersoon voorbereidt voor een consolidatie.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: f6fce69724945448f961769dd383d1047a5d13c4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990294"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Een rechtspersoon voorbereiden voor het consolidatieproces

[!include [banner](../includes/banner.md)]

Tijdens een consolidatie verzamelt u transacties uit meerdere reeksen rekeningen van rechtspersonen en neemt ze op in één reeks met rekeningen van rechtspersonen. In dit onderwerp wordt uitgelegd hoe u een rechtspersoon voorbereidt voor een consolidatie.

> [!NOTE]
> Het is raadzaam om Management Reporter voor Microsoft Dynamics 365 Finance te gebruiken om de financiële resultaten voor meerdere rechtspersonen te combineren in een geconsolideerde indeling. Met Management Reporter kunt u geconsolideerde financiële rapporten voor rechtspersonen maken, Excel gebruiken om consolidatiegegevens uit andere bronnen te importeren en bedragen om te zetten in het gewenste aantal aangiftevaluta's zonder dat het consolidatieproces in Dynamics 365 Finance te hoeven uitvoeren.

U kunt rapporten, zoals financiële overzichten, afdrukken vanuit de geconsolideerde rechtspersoon. U kunt de geconsolideerde rechtspersoon echter niet gebruiken voor dagelijkse transacties.

U kunt gegevens van rechtspersonen consolideren die andere databases gebruiken dan de geconsolideerde rechtspersoon. Dit consolidatieproces wordt een *importconsolidatie* genoemd. De rechtspersonen kunnen ook dezelfde database gebruiken als de geconsolideerde rechtspersoon. Dit consolidatieproces wordt een *online consolidatie* genoemd.

De geconsolideerde rechtspersoon verzamelt de resultaten en de saldi van de dochterondernemingen. Om een geconsolideerde rechtspersoon voor te bereiden op een consolidatie, neemt u de volgende stappen.

1. Ga naar **Grootboek \> Instellen \> Organisatie \> Rechtspersonen**.
2. Selecteer **Nieuw** om de rechtspersoon te maken die de geconsolideerde rechtspersoon zal zijn.
3. Schakel het selectievakje **Gebruiken voor financieel consolidatieproces** in en voer vervolgens informatie in over de geconsolideerde rechtspersoon. Voer deze informatie precies in zoals u deze wilt weergeven op financiële overzichten voor de geconsolideerde rechtspersoon.
4. Sluit de pagina.
5. Selecteer de geconsolideerde rechtspersoon in het veld in de rechterbovenhoek van de pagina en selecteer **OK**.
6. Ga naar **Grootboek \> Instellen \> Grootboek**.
7. Selecteer het rekeningschema, de fiscale kalender, de valuta voor de boekhouding, een optionele aangiftevaluta en het standaardtype wisselkoers voor de geconsolideerde rechtspersoon. 
8. Ga naar **Grootboek \> Instellen \> Valuta \> Valutawisselkoersen**.
9. Stel valutawisselkoersen in relevante perioden in voor de valuta's van de dochterondernemingen.
10. Sluit de pagina.
11. Als de geconsolideerde rechtspersoon dochterondernemingen heeft die vreemde valuta's gebruiken, neemt u de volgende stappen:

    1. Ga naar **Grootboek \> Instellen \> Boeken \> Rekeningen voor automatische transacties**.
    2. Selecteer in het veld **Boekingstype** een geschikte rekening.

        - Als de rechtspersoon buitenlandse dochtermaatschappijen heeft die financieel of operationeel afhankelijk zijn van de bovenliggende rechtspersoon, selecteert u een geschikte rekening voor het boekingstype **Verlies-en-winstrekening voor consolidatieverschillen**.
        - Als u een dochteronderneming consolideert die financieel en operationeel onafhankelijk is van de bovenliggende rechtspersoon, of een rechtspersoon met de resultaten van verschillende dochterondernemingen die financieel en operationeel onafhankelijk zijn van de bovenliggende rechtspersoon en als u vertaalmethoden gebruikt om de gegevens te consolideren, selecteert u een geschikte rekening voor het boekingstype **Saldorekening voor consolidatieverschillen**.

    3. Selecteer in het veld **Hoofdrekening** de hoofdrekeningen die moeten worden gebruikt voor aanpassingen van de herwaardering van vreemde valuta.
    4. Sluit de pagina.

    Als u vroeg in een periode de geconsolideerde rechtspersoon maakt, kunt u vreemde valutabedragen herwaarderen als gewijzigde wisselkoersen tijdens de consolidatieperiode.

De geconsolideerde rechtspersoon is nu ingesteld voor de periodieke taak **Consolideren**. U kunt zowel een importconsolidatie als een online consolidatie uitvoeren.

- Als u een importconsolidatie wilt uitvoeren, gaat u naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Importeren uit\]**.
- Als u een onlineconsolidatie wilt uitvoeren, gaat u naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Online\]**.

> [!NOTE]
> U kunt de consolidatie pas uitvoeren nadat u de dochtermaatschappijen hebt voorbereid voor consolidatie. Zie [Een dochtermaatschappij voor consolidatie instellen](set-up-subsidiary-company-for-consolidation.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]