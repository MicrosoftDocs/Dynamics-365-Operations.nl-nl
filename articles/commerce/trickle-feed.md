---
title: Groepsgewijs orders voor detailhandeltransacties maken
description: Dit onderwerp beschrijft het groepsgewijs maken van orders voor winkeltransacties in Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 09/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 900480c926df58cc1eaca052903384ceeadcccbdc3a0ede8a35f4b2a8ff87556
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719436"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Groepsgewijs orders voor detailhandeltransacties maken

[!include [banner](includes/banner.md)]

In Dynamics 365 Retail versie 10.0.4 en eerder is het boeken van een overzicht een bewerking die aan het einde van de dag plaatsvindt. Alle transacties worden aan het einde van de dag geboekt. Grote transacties moeten vervolgens in een beperkt tijdvenster worden verwerkt, met soms als gevolg dat er fouten optreden bij het laden, vergrendelen en boeken van overzichten. Bovendien kunnen winkeliers gedurende de dag geen opbrengsten en betalingen in hun boeken toerekenen.

Met de functie voor het groepsgewijs maken van orders in Retail versie 10.0.5 kunnen transacties gedurende de hele dag worden verwerkt, en worden alleen de financiële afstemming van de kas en andere contante transacties aan het einde van de dag verwerkt. Met deze functionaliteit wordt de werklast voor het maken van verkooporders, facturen en betalingen verspreid over de hele dag. Dit leidt tot betere prestaties en de mogelijkheid om opbrengsten en betalingen in de boeken bijna in realtime toe te rekenen. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Groepsgewijs boeken gebruiken
  
1. Als u groepsgewijs boeken van detailhandeltransacties wilt inschakelen, schakelt u de functie **Detailhandeloverzichten - Groepsgewijze invoer** in met behulp van Functiebeheer.

    > [!IMPORTANT]
    > Voordat u deze functie inschakelt, moet u ervoor zorgen dat er geen overzichten wachten om te worden geboekt.

2. Het huidige overzichtsdocument wordt opgesplitst in twee typen: transactieoverzicht en financieel overzicht.

      - In het transactieoverzicht worden alle niet-geboekte en gevalideerde transacties opgenomen. Vervolgens worden verkooporders, verkoopfacturen, betalings- en kortingsjournalen en inkomsten-/uitgaventransacties gemaakt op basis van de door u geconfigureerde frequentie. U moet dit proces configureren met een hoge frequentie, zodat documenten worden gemaakt wanneer de transacties in Headquarters worden geüpload via de P-taak. Aangezien met het transactieoverzicht al verkooporders en verkoopfacturen worden gemaakt, is het niet echt nodig om de batchtaak **Voorraad boeken** te configureren. U kunt deze echter nog wel gebruiken om te voldoen aan de specifieke vereisten van uw bedrijf.  
      
     - Het financiële overzicht is ontworpen om aan het einde van de dag te worden gemaakt en ondersteunt alleen de afsluitingsmethode **Ploeg**. Dit overzicht wordt alleen gebruikt voor financiële afstemming en maakt alleen de journalen voor de verschillen tussen het getelde bedrag en het transactiebedrag voor de verschillende betalingsmethoden, samen met journalen voor andere contante transacties.   

3. Als u het transactieoverzicht wilt berekenen, gaat u naar **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Transactieoverzichten in batch berekenen**. Als u het transactieoverzicht in batch wilt boeken, gaat u naar **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Transactieoverzichten in batch boeken**.

4. Als u het financiële overzicht wilt berekenen, gaat u naar **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Financiële overzichten in batch berekenen**. Als u de financiële overzicht in batch wilt boeken, gaat u naar **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Financiële overzichten in batch boeken**.

> [!NOTE]
> De menuopdrachten **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Overzichten in batch berekenen** en **Retail en Commerce > IT Retail en Commerce > POS-boekingen > Overzichten in batch boeken** worden vervangen door deze nieuwe functie.

U kunt de typen van transactie- en financiële overzichten ook handmatig maken. Ga naar **Retail en Commerce > Afzetkanalen > Winkels** en klik op **Overzichten**. Klik op **Nieuw** en selecteer het type overzicht dat u wilt maken. De velden op de pagina **Overzichten** en de acties onder **Overzichtsgroep** op de pagina laten de relevante gegevens en acties zien op basis van het geselecteerde overzichtstype.


[!INCLUDE[footer-include](../includes/footer-banner.md)]