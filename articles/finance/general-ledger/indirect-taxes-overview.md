---
title: Btw-overzicht
description: In dit onderwerp vindt u een overzicht van het btw-systeem. Daarnaast worden de verschillende elementen van de btw-instellingen uitgelegd en wordt aangegeven hoe deze samenwerken.
author: ShylaThompson
manager: AnnBe
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxPeriod, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 13111
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16a67ef625fdde0755e96c959be1fb2989ca53b6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770661"
---
# <a name="sales-tax-overview"></a>Btw-overzicht

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u een overzicht van het btw-systeem. Daarnaast worden de verschillende elementen van de btw-instellingen uitgelegd en wordt aangegeven hoe deze samenwerken.

<a name="overview"></a>Overzicht
--------

Het btw-raamwerk ondersteunt veel typen indirecte belastingen zoals btw, belasting toegevoegde waarde (btw), belasting voor goederen en services (GST), kosten op basis van eenheden en bronbelasting. Deze belastingen worden berekend en gedocumenteerd tijdens transacties voor inkoop en verkoop. Periodiek moeten deze belastingen worden aangegeven bij en betaald aan de belastingdienst. 

In het volgende diagram worden de verschillende rechtspersonen in de btw-structuur en hun onderlinge relaties beschreven.

[![Diagram met overzicht van entiteiten voor btw-instellingen](./media/taxoverview1-300x209.jpg)](./media/taxoverview1.jpg) 

Voor elk type btw waarvoor een bedrijf zich moet verantwoorden, moet een btw-code worden gedefinieerd. In een btw-code worden de btw-tarieven en berekeningsregels voor de btw opgeslagen. 

Elke btw-code moet aan een btw-vereffeningsperiode zijn gekoppeld. Btw-vereffeningsperioden definiëren de intervallen waarmee btw moet worden aangegeven en betaald aan de btw-dienst. Elke btw-vereffeningsperiode moet worden toegewezen aan een btw-dienst. Een btw-dienst vertegenwoordigt de rechtspersoon waaraan btw wordt aangegeven en betaald. Tevens definieert deze de indeling voor de btw-aangifte. De btw-dienst kan aan leveranciersrekeningen worden gekoppeld. Zie [Btw-vereffeningsperioden instellen](tasks/set-up-sales-tax-settlement-periods.md) voor meer informatie.

Elke btw-code moet ook aan een grootboekboekingsgroep zijn gekoppeld. Met een grootboekboekingsgroep worden de hoofdrekeningen gedefinieerd waarnaar bedragen voor de btw-codes worden geboekt. 

Optionele btw-aangiftecodes kunnen ook worden gedefinieerd. Deze kunnen worden toegewezen aan btw-codes voor de verschillende bedragtypen die worden berekend voor de btw-code. Het rapport **Btw-betaling per code** biedt de totalen per btw-aangiftecode voor een bepaalde btw-vereffeningsperiode en interval. 

Aan elke transactie waarvoor btw moet worden berekend en geboekt, moeten een btw-groep en btw-groep voor artikelen zijn gekoppeld. Btw-groepen zijn gekoppeld aan de partij (bijvoorbeeld een klant of leverancier) van de transactie, terwijl de btw-groepen voor artikelen aan de bron (bijvoorbeeld een artikel of aanschaffingscategorie) van de transactie zijn gekoppeld. Btw-groepen bevatten een lijst met btw-codes. De btw-codes die zowel in de btw-groep als in de btw-groep voor artikelen zijn opgenomen voor een transactie zijn de btw-codes die van toepassing zijn op die transactie. 

In de volgende tabel worden de rechtspersonen en de volgorde voor het instellen van belastingen beschreven.

| Instellingsactiviteit                                                  | Vereist/optioneel en omschrijving                                                                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hoofdrekeningen maken.                                           | Vereist. Voordat u de btw-functie in kunt stellen, moeten de hoofdrekeningen worden gemaakt die het bedrijf gebruikt om belastingen te betalen en te registreren.                                                                                                                                                                             |
| Groepen boekingen in grootboek instellen voor btw.                     | Vereist. Grootboekboekingsgroepen definiëren de hoofdrekeningen voor het registreren en het betalen van btw.   Zie [Groepen boekingen in grootboek instellen voor btw](tasks/set-up-ledger-posting-groups-sales-tax.md) voor meer informatie.                                                                                 |
| Btw-diensten instellen.                                   | Vereist. Btw-diensten zijn de rechtspersonen waarbij btw moet worden aangegeven en waaraan deze moet worden betaald.    Zie [Btw-diensten instellen](tasks/set-up-sales-tax-authorities.md) voor meer informatie.                                                                                                                                          |
| Een btw-vereffeningsperiode instellen.                            | Vereist. Btw-vereffeningsperioden bevatten informatie over wanneer en hoe vaak de btw moet worden aangegeven en betaald. Ze zijn gerelateerd aan een btw-dienst.                                                                                                                                                       |
| Btw-aangiftecodes instellen.                               | Optioneel. Btw-aangiftecodes kunnen aan btw-codes worden toegewezen om bedragen voor meerdere btw-codes aan te geven onder één btw-aangiftecode. Zie [Btw-aangiftecodes instellen](tasks/set-up-sales-tax-reporting-codes.md) voor meer informatie.                                         |
| Stel btw-codes in.                                         | Vereist. In btw-codes worden de btw-tarieven en berekeningsregels voor elke btw opgeslagen. Btw-codes zijn gekoppeld aan een btw-vereffeningsperiode en een grootboekboekingsgroep. Zie [Btw-codes instellen](tasks/set-up-sales-tax-codes.md) voor meer informatie.                                |
| Btw-groepen instellen.                                        | Vereist. Btw-groepen bevatten een lijst met btw-codes die gelden voor de partij (klant of leverancier) van een transactie. Voor elke transactie bepaalt het snijpunt van btw-codes in de btw-groep en de btw-groep voor artikelen welke btw-codes van toepassing zijn op die transactie.                  |
| Btw-groepen voor artikelen instellen.                                   | Vereist. Btw-groepen voor artikelen bevatten een lijst met btw-codes die voor de bron (product, service, enzovoort) van een transactie gelden. Voor elke transactie bepaalt het snijpunt van btw-codes in de btw-groep en de btw-groep voor artikelen welke btw-codes van toepassing zijn op die transactie. Zie [Btw-groepen en artikel-btw-groepen instellen](tasks/set-up-sales-tax-groups-item-sales-tax-groups.md) voor meer informatie. |
| Btw-parameters instellen op de pagina's voor toepassingsparameters. | Vereist. Verschillende gebieden, zoals Grootboek, Klanten en Leveranciers, moeten parameters voor een correcte berekening van indirecte belastingen instellen. Hoewel de meeste van deze parameters standaardwaarden hebben, moeten ze worden aangepast aan de vereisten van elk bedrijf.                                          |

## <a name="sales-tax-on-transactions"></a>Btw op transacties
Voor elke transactie (verkoop-/inkoopdocumentregels, journalen, enzovoort) moet u een btw-groep en een btw-groep voor artikelen invoeren om btw te berekenen. Standaardgroepen worden opgegeven in hoofdgegevens (bijvoorbeeld de categorie klant, leverancier, artikel en aanschaffing), maar u kunt de groepen voor een transactie desgewenst handmatig wijzigen. Beide groepen bevatten een lijst met btw-codes en het snijpunt van de twee lijsten met btw-codes bepaalt de lijst met relevante btw-codes voor de transactie. 

Voor elke transactie kunt u de berekende btw opzoeken door de pagina **Btw-transactie** te openen. U kunt de btw voor een documentregel of voor het hele document opzoeken. Voor bepaalde documenten (bijvoorbeeld leveranciersfacturen en algemene journalen) kunt u de berekende btw aanpassen als het oorspronkelijke document afwijkende bedragen bevat.

## <a name="sales-tax-settlement-and-reporting"></a>Btw-vereffening en -aangifte
Btw moet regelmatig (maandelijks, per kwartaal, enzovoort) worden aangegeven bij en betaald aan btw-diensten. U kunt belastingrekeningen voor het interval vereffenen en de saldi boeken naar de btw-vereffeningsrekening, zoals opgegeven in de grootboekboekingsgroepen. U hebt toegang tot deze functionaliteit op de pagina **Btw vereffenen en boeken**. U moet de btw-vereffeningsperiode opgeven waarvoor btw moet worden vereffend. 

Nadat de btw is betaald, moet het saldo op de btw-vereffeningsrekening worden verrekend met de bankrekening. Als de btw-dienst die is opgegeven voor de btw-vereffeningsperiode aan een leveranciersrekening is gekoppeld, wordt het btw-saldo geboekt als openstaande leveranciersfactuur en kan deze in het normale betalingsvoorstel worden opgenomen.

## <a name="conditional-sales-tax"></a>Voorwaardelijke btw
Voorwaardelijke BTW is BTW die proportioneel aan het werkelijke bedrag dat wordt betaald op een factuur wordt betaald. Daarentegen wordt standaard BTW berekend bij de facturering van tijd. Voorwaardelijke BTW moet worden betaald aan de belastingdienst wanneer de betaling is geboekt, niet wanneer de factuur is geboekt. Wanneer de factuur wordt geboekt, moet de transactie worden gerapporteerd op het rapport BTW-boek. De transactie moet echter niet worden opgenomen in het rapport BTW-betaling. 

Als u het selectievakje Voorwaardelijke btw inschakelt in het formulier Grootboekparameters, kan er pas btw worden afgetrokken als u de factuur hebt betaald. Dit is in sommige landen/regio's een juridische vereiste.

> [!NOTE]
> Als u het selectievakje Voorwaardelijke btw inschakelt, moet u btw-codes en btw-groepen instellen en moet u ter ondersteuning van de functionaliteit boekingsgroepen in het grootboek maken. |

###  <a name="example"></a>Voorbeeld

U betaalt elke maand BTW. Op 15 juni maakt u een klantinvoice van 10.000 met een btw-bedrag.
-   Het btw-percentage is 25% of 25,00.
-   Factuur moet niet later dan 30 juli betaald worden.

Gewoonlijk zou u 2.500 aan de belastingdienst moeten betalen wanneer de factuur wordt geboekt in juni, zelfs als u geen betaling hebt ontvangen van de klant. 

Echter, als u een voorwaardelijke BTW gebruikt, hoeft u pas met de belastingdienst te vereffenen wanneer u de betaling van de klant op 30 juli ontvangt.

### <a name="postdated-check"></a>Gepostdateerde cheque

Als u gepostdateerde cheques gebruikt als betalingsmethode, vindt geen afstemming met de bankrekening plaats wanneer de betaling wordt uitgevoerd. In sommige landen wordt de btw een 'gerealiseerde' schuld als de betaling wordt vereffend, wat betekent dat de gepostdateerde cheque is vereffend. U kunt deze optie inschakelen door **De voorwaardelijke belasting realiseren wanneer gepostdateerde cheques worden geïnd** in **Contanten en bankbeheer > Instellingen > Parameters voor Contanten en bankbeheer > Gepostdateerde cheques**.

Zie [Bronbelasting instellen](tasks/set-up-withholding-tax.md) voor meer informatie.
