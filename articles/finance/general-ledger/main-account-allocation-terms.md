---
title: Toewijzingstermijn
description: Dit onderwerp biedt informatie over het gebruik van toewijzingstermijnen voor een hoofdrekening.
author: rachel-profitt
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60b995216eed2eda740cb4cd9be79d15d46789e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248922"
---
# <a name="allocation-terms"></a>Toewijzingstermijn

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over het gebruik van toewijzingstermijnen voor een hoofdrekening. Toewijzingstermijnen worden gebruikt om bedragen over meerdere combinaties van grootboekrekeningen te verdelen. Hiermee kunt u ervoor zorgen dat uitgaven en opbrengsten in de boekhouding aan het juiste object worden doorberekend.

Elke toewijzingstermijn die u maakt op basis van een hoofdrekening, definieert het percentage van een boekstuk dat moet worden toegewezen vanuit een hoofdrekening met één bron en een combinatie van financiële dimensies. Daarnaast definieert u de doelhoofdrekening en de financiële dimensies waar het bedrag wordt toegewezen. 

Wanneer u de financiële dimensie van de bron voor de toewijzing definieert, kunt u selecteren of elke dimensie specifiek of flexibel is. Specifiek geeft aan dat de financiële dimensie voor de brontransactie moet overeenkomen met de geselecteerde dimensie. Wanneer u flexibel selecteert, geeft dit aan dat elke waarde voor de financiële dimensie kan bijdragen aan een overeenkomst.

Wanneer u de doelgrootboekrekening voor een toewijzingstermijn definieert, moet u de hoofdrekening opgeven waaraan u het bedrag toewijst. U kunt dezelfde hoofdrekening gebruiken waarnaar de brontransactie wordt geboekt, of een andere hoofdrekening. Als dezelfde hoofdrekening wordt gebruikt, wordt er een waarschuwing weergegeven wanneer de record wordt opgeslagen. Naast het opgeven van de hoofdrekening moet u ook de doeldimensies opgeven. Voor elke dimensie kunt u opgeven of u de waarde van de financiële dimensie van de bron wilt behouden of wijzigen. Als u Nee selecteert, moet u een nieuwe waarde selecteren voor de financiële dimensie. Als u Ja selecteert, wordt er geen aanvullende informatie opgegeven en blijven de oorspronkelijke financiële dimensies bij het boeken behouden.

Er is geen limiet voor het aantal toewijzingstermijnen dat u aan een hoofdrekening kunt toevoegen. De som van het percentage dat wordt toegewezen voor een toewijzingstermijn kan echter niet groter zijn dan 100. U kunt toewijzingen maken voor minder dan 100 procent als een gedeelte van het oorspronkelijke boekstukbedrag in de financiële dimensies van de bron moet blijven. Toewijzingstermijnen kunnen worden toegevoegd aan een hoofdrekening als een rechtspersoon. Als u een gedeeld rekeningschema gebruikt, moeten er toewijzingstermijnen worden gedefinieerd voor elke rechtspersoon. Als u de knop **Toewijzingstermijnen** wilt openen , moet u eerst het selectievakje **Toewijzing** inschakelen bij overschrijvingen rechtspersoon.

## <a name="allocation-term-example"></a>Voorbeeld van toewijzingstermijn
U hebt een kostenplaats gedefinieerd voor uw organisatie met de naam CORPORATE en het nummer 000. Wanneer facturen voor kosten van elektriciteit worden geboekt, worden ze gecodeerd naar deze kostenplaats CORPORATE. Uw bedrijf heeft een regel gedefinieerd dat alle elektriciteitskosten moeten worden toegewezen aan elk van de afzonderlijke kostenplaatsen. De overige financiële dimensies voor afdeling en bedrijfseenheid blijven hetzelfde.

Met dit voorbeeld wordt een nieuwe toewijzingstermijn gemaakt voor de hoofdrekening voor elektriciteitskosten. Voor elke kostenplaats wordt één rij gemaakt met het percentage dat moet worden toegewezen. De **selectiecriteria** voor de financiële dimensies van de bron voor elke rij zijn **specifiek** voor de **kostenplaats** en de waarde wordt ingesteld op 000: CORPORATE. Voor afdeling en bedrijfseenheid zijn de **selectiecriteria** **flexibel**.

Op het sneltabblad **Doelgrootboekrekening** is de hoofdrekening dezelfde onkostenrekening voor elektriciteit en wordt **Financiële dimensies van bron behouden** ingesteld op **Ja** voor **Bedrijfseenheid** en **Afdeling**. **Financiële dimensies van bron behouden** wordt ingesteld op **Nee** voor de **kostenplaats** en de geselecteerde waarde wordt elk afzonderlijk kostencentrum waaraan u toewijst. Als er drie kostenplaatsen zijn om aan toe te wijzen, worden er drie toewijzingsrecords gemaakt. Het enige verschil tussen elke toewijzingstermijn is de kostenplaats die is opgegeven op de doelgrootboekrekening.

## <a name="create-an-allocation-term-on-a-main-account"></a>Een toewijzingstermijn maken voor een hoofdrekening

1. Ga in het **Navigatievenster** naar **Modules > Grootboek > Rekeningschema > Rekeningen > Hoofdrekeningen**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Selecteer **Toevoegen** op het sneltabblad **Overschrijvingen rechtspersoon**.
4. Selecteer het **Bedrijf** en selecteer vervolgens **Toevoegen**.
5. Schakel het selectievakje **Toewijzing** in.
6. Selecteer **Toewijzingstermijnen**.
7. Selecteer **Verwerken** om de standaardrecord te wijzigen of selecteer **Nieuw** om een record toe te voegen.
8. Voer in het veld **Percentage** het percentage boekstuktransacties in dat u wilt toewijzen.
9. Selecteer op het sneltabblad **Financiële dimensie van bron** in de **selectiecriteria** voor elke financiële dimensie een optie.
    - Als u **Specifiek** selecteert, selecteert u vervolgens de waarde van de financiële dimensie in de vervolgkeuzelijst aan de rechterkant.
    - Als u **Flexibel** selecteert, is er geen aanvullende informatie nodig voor de financiële dimensie.
10. Selecteer op het sneltabblad **Doelgrootboekrekening** in het veld **Naar rekening** de hoofdrekening waaraan u het percentage van de boekstuktransactie wilt toewijzen.
11. Selecteer bij **Financiële dimensies van bron behouden** een optie voor elke financiële dimensie.
    - Als u **Nee** selecteert, selecteert u aan de rechterkant de waarde van de financiële dimensie in de vervolgkeuzelijst waaraan u de boekstuktransactie wilt toewijzen.
    - Als u **Ja** selecteert, hoeft u verder geen informatie in te vullen. Het systeem houdt de waarde op het oorspronkelijke boekstuk bij bij het boeken van de toewijzing.
12. Herhaal stap 7 tot en met 11 voor elk extra toewijzing. De som van alle toewijzingen wordt aangegeven in het veld **Totaal percentage**. Dit bedrag kan niet hoger zijn dan 100.
13. Sluit alle pagina's.

>[!NOTE] 
> U kunt desgewenst de knop **Kopiëren** gebruiken om de geselecteerde toewijzing te dupliceren.

Wanneer een toewijzingstermijn voor een hoofdrekening wordt gemaakt, boekt het systeem automatisch een nieuw boekstuk wanneer een boekstuk wordt geboekt dat overeenkomt met de financiële dimensies van de bron van de toewijzingstermijnen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]