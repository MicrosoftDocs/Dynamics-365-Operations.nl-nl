--- 
title: Een vrijgegeven product maken voor een enkel bedrijf
description: "Deze procedure geeft aan hoe één vrijgegeven product kan worden gemaakt in de context van één juridische eenheid."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 042eafc29e377e0ad6fb8dc1499daf8eb105b7ed
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-released-product-for-a-single-company"></a>Een vrijgegeven product maken voor een enkel bedrijf

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure geeft aan hoe één vrijgegeven product kan worden gemaakt in de context van één juridische eenheid. Nadat het vrijgegeven product is gemaakt, is het onmiddellijk beschikbaar in alleen deze eenheid. U kunt deze procedure uitvoeren in demobedrijf USMF. Deze taak wordt gewoonlijk uitgevoerd door een productontwerper.


## <a name="create-a-released-product"></a>Een vrijgegeven product maken
1. Ga naar Vrijgegeven producten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Productnummer.
    * Als een productnummer niet automatisch in het Productnummerveld is ingevoerd, voert u een uniek productnummer in. Deze stap is alleen vereist als er geen nummerreeks voor productnummers is ingesteld.  
4. Typ een waarde in het veld Productnaam.
    * Voor de productnaam wordt standaard de zoeknaam gebruikt. Indien nodig, kunt u ervoor kiezen om de zoeknaam te wijzigen.  
5. Klik in het veld Artikelmodelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De artikelmodelgroepen bevatten instellingen waarmee wordt bepaald hoe artikelen worden beheerd en verwerkt bij artikelontvangsten en -uitgiften. De instellingen bepalen ook hoe het verbruik van artikelen wordt berekend.  
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Artikelengroepen worden gebruikt voor het beheren van de voorraad door de voorraadartikelen op basis van de kenmerken van het artikel in groepen te verdelen. Als u bijvoorbeeld wilt beheren hoe informatie in hoofdrekeningen wordt geboekt, kunt u een reeks verschillende artikelgroepen maken die zijn gekoppeld aan specifieke hoofdrekeningen. Hiermee kunt u de voorraadwaarde van artikelen in verschillende stadia bijhouden.  
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik in het veld Opslagdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De opslagdimensies helpen u bij het beheer over de opslag en het verwijderen van artikelen in de voorraad. Zo kan bijvoorbeeld een opslagdimensie Locatie en Magazijn zijn.  
12. Zoek en selecteer de gewenste record in de lijst.
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Klik in het veld Traceringsdimensiegroep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De traceringsdimensiegroep bepaalt welke traceringsdimensies u kunt toevoegen aan een product. Het batchnummer en serienummer worden bijvoorbeeld gebruikt om voorraadartikelen te traceren.  
15. Zoek en selecteer de gewenste record in de lijst.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
17. Klik in het veld Voorraadeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De voorraadeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het in de voorraad is opgeslagen.  
18. Zoek en selecteer de gewenste record in de lijst.
19. Klik in de lijst op de koppeling in de geselecteerde rij.
20. Klik in het veld Inkoopeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De inkoopeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het van een leverancier wordt gekocht.  
21. Zoek en selecteer de gewenste record in de lijst.
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Klik in het veld Verkoopeenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De verkoopeenheid bepaalt hoe het product wordt gekwantificeerd wanneer het naar een klant wordt verkocht.  
24. Zoek en selecteer de gewenste record in de lijst.
25. Klik in de lijst op de koppeling in de geselecteerde rij.
26. Klik in het veld Stuklijsteenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De stuklijsteenheid bepaalt hoe het product wordt gekwantificeerd als het wordt opgenomen in een stuklijst.  
27. Zoek en selecteer de gewenste record in de lijst.
28. Klik in de lijst op de koppeling in de geselecteerde rij.
29. Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De btw-groep voor artikel in de btw-groep voor btw-berekening op verkoop bepaalt hoe de btw wordt berekend voor elk artikel.  
30. Zoek en selecteer de gewenste record in de lijst.
31. Klik in de lijst op de koppeling in de geselecteerde rij.
32. Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De btw-groep voor artikel in de btw-groep voor btw-berekening op inkoop bepaalt hoe de btw op inkoop wordt berekend voor elk artikel.  
33. Zoek en selecteer de gewenste record in de lijst.
34. Klik in de lijst op de koppeling in de geselecteerde rij.
35. Klik op OK.

## <a name="add-product-characteristics"></a>Productkenmerken toevoegen
1. Vouw de sectie Voorraad beheren uit of samen.
2. Voer een getal in het veld Nettogewicht in.
3. Voer een getal in het veld Tarragewicht in.
4. Voer een getal in het veld Brutodiepte in.
5. Voer een getal in het veld Brutobreedte in.
6. Voer een getal in het veld Brutohoogte in.
7. Voer een getal in het veld Volume in.

## <a name="add-financial-dimensions"></a>Financiële dimensies toevoegen
1. Vouw de sectie Financiële dimensies uit of samen.
2. Klik in het veld Bedrijfseenheid op de vervolgkeuzeknop om de zoekopdracht te openen.
3. Zoek en selecteer het gewenste record in de lijst.
4. Klik in de lijst op de koppeling in de geselecteerde rij.
5. Klik in het veld Kostenplaats op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Zoek en selecteer het gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Klik in het veld Afdeling op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer het gewenste record in de lijst.
10. Klik in de lijst op de koppeling in de geselecteerde rij.
11. Klik in het veld Artikelgroep op de vervolgkeuzeknop om de zoekopdracht te openen.
12. Zoek en selecteer het gewenste record in de lijst.
13. Klik in de lijst op de koppeling in de geselecteerde rij.


