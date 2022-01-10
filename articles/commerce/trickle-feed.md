---
title: Groepsgewijs orders voor detailhandelstransacties maken
description: Dit onderwerp beschrijft het groepsgewijs maken van orders voor winkeltransacties in Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/14/2021
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
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921240"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Groepsgewijs orders voor detailhandelstransacties maken

[!include [banner](includes/banner.md)]

In versie 10.0.5 en hoger van Microsoft Dynamics 365 Commerce raden we u aan om alle boekingsprocessen voor overzichten over te brengen naar de boekingsprocessen voor overzichten op basis van groepsgewijze boeking. Er worden aanzienlijke prestaties en zakelijke vergoedingen gekoppeld aan het gebruik van de functionaliteit voor groepsgewijs boeken van uw bedrijf. Verkooptransacties worden de hele dag verwerkt. Betalings- en kasbeheertransacties worden aan het einde van de dag verwerkt in het financieel overzicht. Functionaliteit voor groepsgewijs boeken maakt de continue verwerking van verkooporders, facturen en betalingen mogelijk. Daarom kunnen voorraad, opbrengst en betalingen bijna in realtime worden bijgewerkt en herkend.

## <a name="use-trickle-feed-based-posting"></a>Groepsgewijs boeken gebruiken

> [!IMPORTANT]
> Voordat u groepsgewijs boeken inschakelt, moet u ervoor zorgen dat er geen berekende en ongeboekte overzichten zijn. Boek alle overzichten voordat u de functie inschakelt. U kunt controleren op openstaande overzichten in de werkruimte **Financiën van winkel**.

Als u groepsgewijs boeken van detailhandelstransacties wilt inschakelen, schakelt u de functie **Detailhandeloverzichten - Groepsgewijze invoer** in de werkruimte **Functiebeheer** in. Overzichten worden onderverdeeld in twee typen: transactieoverzichten en financiële overzichten.

### <a name="transactional-statements"></a>Transactieoverzichten

Het verwerken van transactieoverzichten is bedoeld om met een hoge frequentie te worden uitgevoerd, de hele dag lang, zodat documenten worden gemaakt wanneer de transacties worden geüpload in Commerce Headquarters. Transacties worden vanuit de winkels naar Commerce Headquarters geladen wanneer u de **P-Taak** uitvoert. U moet ook de taak **Winkeltransacties valideren** uitvoeren om transacties te valideren zodat ze worden opgepikt door het transactieoverzicht.

Plan het uitvoeren van de volgende taken met hoge frequentie:

- Als u een transactieoverzicht wilt berekenen, voert u de taak **Transactieoverzichten in batch berekenen** uit (**Retail en commerce \> IT Retail en Commerce \> POS-boekingen \> Transactieoverzichten in batch berekenen**). Met deze taak worden alle niet-geboekte en gevalideerde transacties opgehaald en aan een nieuw transactieoverzicht toegevoegd.
- Als u transactieoverzichten wilt boeken in een batch, voert u de taak **Transactieoverzichten in batch boeken** uit (**Retail en commerce \> IT Retail en Commerce \> POS-boekingen \> Transactieoverzichten in batch boeken**). Met deze taak wordt het boekingsproces uitgevoerd en worden verkooporders, verkoopfacturen, betalingsjournalen, kortingsjournalen en inkomsten-/uitgaventransacties gemaakt voor niet-geboekte overzichten die geen fouten bevatten. 

### <a name="financial-statements"></a>Financiële overzichten

De verwerking van financiële overzichten is bedoeld als een proces aan het einde van de dag. Dit type verwerking van overzichten ondersteunt alleen de **afsluitingsmethode voor ploegendiensten** en er worden alleen afgesloten ploegendiensten verwerkt. Overzichten zijn beperkt tot financiële afstemming. Hiermee worden alleen de journalen gemaakt voor de verschillen tussen het getelde bedrag en het transactiebedrag voor betalingsmethoden, samen met journalen voor andere transacties voor beheer van contant geld.

Plan de begin- en eindtijden van de volgende taken in het financieel overzicht op basis van de verwachte einde van de dag:

- Als u een financieel overzicht wilt berekenen, voert u de taak **Financiële overzichten in batch berekenen** uit (**Retail en commerce \> IT Retail en Commerce \> POS-boekingen \> Financiële overzichten in batch berekenen**). Met deze taak worden alle niet-geboekte financiële transacties verzameld en aan een nieuw financieel overzicht toegevoegd.
- Als u financiële overzichten wilt boeken in een batch, voert u de taak **Financiële overzichten in batch boeken** uit (**Retail en commerce \> IT Retail en Commerce \> POS-boekingen \> Financiële overzichten in batch boeken**).

### <a name="manually-create-statements"></a>Handmatig overzichten maken

Typen transactie- en financiële overzichten kunnen ook handmatig worden gemaakt. 

1. Ga naar **Retail en commerce \> Afzetkanalen \> Winkels** en selecteer **Overzichten**. 
2. Selecteer **Nieuw** en selecteer vervolgens het type overzicht dat u wilt maken. De velden op de pagina **Overzichten** tonen gegevens die relevant zijn voor het geselecteerde overzichtstype, terwijl de acties onder **Overzichtsgroep** relevante acties laten zien.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
