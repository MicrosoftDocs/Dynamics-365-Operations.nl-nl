--- 
title: Een nieuwe handelsovereenkomst maken
description: Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen.
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1178c7a5db129801f83afa8b4caf9357ccf76b71
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-new-trade-agreement"></a>Een nieuwe handelsovereenkomst maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Als u uw eigen gegevens gebruikt, moet u voordat u deze taakbegeleiding start ervoor zorgen dat er een handelsovereenkomstjournaal bestaat met de naam Standaard, waarvan de relatie is ingesteld op 'Prijs (verkoop)'.


## <a name="create-and-post-a-new-trade-agreement-journal"></a>Een nieuw handelsovereenkomstjournaal maken en boeken
1. Ga naar Verkoop en marketing > Prijzen en kortingen > Handelsovereenkomstjournalen.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Regels.
7. Selecteer 'Tabel' in het veld Rekeningcode.
    * In dit voorbeeld werkt u de prijs voor een specifieke klant bij, wat betekent dat u mogelijk Tabel moet kiezen. Als u de catalogusprijs van het product zou bijwerken, zou u Alle selecteren, zodat de nieuwe prijs voor alle klanten geldt. Als u onderscheid zou maken tussen verschillende prijzen uit verschillende klantsegmenten, zou u Groep selecteren. Als u Groep wilt selecteren, moet u klantprijsgroepen hebben ingesteld.  
8. Klik in het veld Rekening selecteren op de vervolgkeuzeknop om de zoekopdracht te openen.
9. Zoek en selecteer de gewenste record in de lijst.
10. Selecteer 'Tabel' in het veld Artikelcode.
    * Wanneer u een handelsovereenkomst van het type "Prijs (verkoop)" invoert, moet u alleen 'Tabel' selecteren in het veld Artikelcode. Dit komt doordat een prijs een absolute waarde is en niet voor alle producten of groep producten hetzelfde kan zijn.  
11. Klik in het veld Artikelrelatie op de vervolgkeuzeknop om de zoekopdracht te openen.
12. Selecteer in de lijst het product dat u in de overeenkomst wilt opnemen.
    * Maak een notitie van het product dat u hebt geselecteerd.  
13. Klik in de lijst op de koppeling in de geselecteerde rij.
14. Voer in het veld Van een minimumhoeveelheid in.
    * Als de klant een minimumhoeveelheid moet bestellen voordat deze voor de nieuwe prijs in aanmerking komt, moet u die hoeveelheid hier opgeven.  
    * Voer een waarde in het veld Aan in om de maximale hoeveelheid op te geven waarboven de prijs van de overeenkomst niet geldig is. Als u prijzen en kortingen aanbiedt op basis van meerdere hoeveelheidscategorieën, geeft u elke hoeveelheidsbracket op als een minimum- en een maximumwaarde in het veld 'Van' en het veld 'Tot'.  
15. Voer in het veld Bedrag in valuta een prijs in.
16. Voer in het veld Datum een datum in waarop deze overeenkomst geldig is.
17. Klik op Opslaan.
18. Klik op Valideren.
19. Klik op Geselecteerde regels valideren.
20. Klik op OK.
21. Klik op Boeken.
22. Klik op OK.

## <a name="view-trade-agreements-for-a-product"></a>Handelsovereenkomsten voor een product weergeven
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Zoek en selecteer in de lijst het product waarvan u de prijs zojuist hebt bijgewerkt.
3. Klik in het actievenster op Verkopen.
4. Klik op Handelsovereenkomsten weergeven.
    * Controleer de gegevens van de prijshandelsovereenkomst die u zojuist hebt gemaakt.    
5. Sluit de pagina.


