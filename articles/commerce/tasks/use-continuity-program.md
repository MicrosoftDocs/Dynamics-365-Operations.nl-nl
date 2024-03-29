---
title: Continuïteitsprogramma's gebruiken
description: Deze procedure laat zien hoe u een continuïteitsprogramma verkoopt en de gerelateerde verkooporders verwerkt.
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.industry: Retail
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
ms.openlocfilehash: 3736984a336b35b23b7060b2d98770912cc9ec6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267399"
---
# <a name="using-continuity-program"></a>Continuïteitsprogramma's gebruiken

[!include [banner](../includes/banner.md)]

Deze procedure laat zien hoe u een continuïteitsprogramma verkoopt en de gerelateerde verkooporders verwerkt. Om deze procedure te kunnen uitvoeren, moet de gebruiker zijn ingesteld als een callcenter-gebruiker. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Klanten > Klantenservice.
2. Type in het veld Zoektekst 'Karen' en druk de Tab-toets in.
    * Het dialoogvenster Geavanceerd zoeken moet worden geopend in een pop-upvenster. Als dit niet gebeurt, klikt u op Zoeken rechts naast dit veld.  
3. Markeer in de lijst de geselecteerde rij.
    * Er zou slechts één rij moeten zijn, die Karen Berg bevat. Selecteer de rij door te klikken op de kolom met het selectievakje helemaal links in het raster.  
4. Klik op Selecteren.
5. Klik op Nieuwe verkooporder.
    * Het is handig om nu het verkoopordernummer te noteren. U hebt dit later in deze procedure nog nodig.  
6. Type in het veld Artikelnummer '88000' en druk de Tab-toets in.
    * Dit is een continuïteitsartikel in de demogegevens van USRT.  
7. Klik op Voltooien.
8. Selecteer in het veld Betalingsmethode 'Visa'.
9. Klik op Creditcard toevoegen.
    * Voer de vereiste creditcardinformatie in op deze pagina.  
10. Klik op OK.
11. Vouw de sectie Betaling uit.
    * Om een callcenter-bestelling in te dienen, moeten voor de order ook betalingen worden ingevoerd.  
12. Klik op OK.
13. Klik op Aanbieden.
    * U bent klaar met het maken van een nieuwe continuïteitsorder. Vervolgens voert u twee batchprocessen uit waarmee de continuïteitsorders worden verwerkt.  
14. Sluit de pagina.
15. Ga naar Detailhandel en commerce > Continuïteit > Continuïteitsbetalingen verwerken.
16. Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.
17. Klik op OK.
18. Ga naar Detailhandel en commerce > Continuïteit > Onderliggende continuïteitsorders maken.
    * Dit proces maakt nieuwe verkooporders op basis van de instellingen van uw continuïteitsprogramma's.  
19. Type in het veld Continuïteitsartikel '88000' en druk de Tab-toets in.
    * Artikel '88000' is een continuïteitsartikel in de demogegevens van USRT.  
20. Typ of selecteer een waarde in het veld Verkooporder.
    * Voer het verkoopordernummer in dat u eerder in de procedure hebt genoteerd. Dit zorgt ervoor dat de verwerkingstijd voor deze procedure minimaal blijft. Het veld Verkooporder is optioneel. U kunt alle orders voor elk programma verwerken.  
21. Klik op OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
