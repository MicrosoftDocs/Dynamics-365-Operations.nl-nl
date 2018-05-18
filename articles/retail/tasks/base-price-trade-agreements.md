--- 
title: " Basisprijs en handelsovereenkomsten"
description: Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.
author: josaw1
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 81c70921718e41719470c7428c05a9f7ae77354a
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="base-price-and-trade-agreements"></a> Basisprijs en handelsovereenkomsten

[!include [task guide banner](../includes/task-guide-banner.md)]

Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Detailhandel en commerce > Prijzen en kortingen > Prijsgroepen > Alle prijsgroepen.
    * Prijsgroepen bepalen hoe handelsovereenkomsten aan specifieke kanalen worden toegewezen. Als u prijsgroepen gebruikt om handelsovereenkomsten aan een kanaal toe te wijzen, worden kanaalspecifieke prijzen ingeschakeld.  
2. Klik op Nieuw.
3. Typ een waarde in het veld Prijsgroepen.
4. Typ een waarde in het veld Naam.
5. Klik op Opslaan.
6. Sluit de pagina.
7. Ga naar Detailhandel en commerce > Kanalen > Detailhandelwinkels > Alle detailhandelwinkels.
8. Selecteer 'New York' in de lijst.
9. Klik in het actievenster op Winkel.
10. Klik op Prijsgroepen.
11. Klik op Nieuw.
12. Klik in het veld Prijsgroepen op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik op Opslaan.
15. Sluit de pagina.
16. Sluit de pagina.
17. Ga naar Detailhandel en commerce > Producten en categorieën > Vrijgegeven producten per categorie.
18. Klik in de lijst op de koppeling in de geselecteerde rij.
19. Klik op Bewerken.
20. Schakel de uitbreiding van de sectie Verkopen om.
21. Voer een getal in het veld Prijs in.
    * Deze prijs wordt gebruikt als er geen toepasselijke handelsovereenkomsten worden gevonden.  
22. Klik op Opslaan.
23. Klik in het actievenster op Verkopen.
24. Klik op Handelsovereenkomsten maken.
25. Klik op Nieuw.
26. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
27. Selecteer 'Detailhandel' in de lijst.
    * In de demogegevens heeft de journaalnaam 'Detailhandel' de standaardrelatie 'Prijs (verkoop)'. Dat betekent dat alle nieuw gemaakte regels standaard verkoopprijshandelsovereenkomsten gebruiken.  
28. Klik op Regels.
29. Selecteer 'Groep' in het veld Rekening.
30. Klik in het veld Rekening selecteren op de vervolgkeuzeknop om de zoekopdracht te openen.
31. Zoek en selecteer de gewenste record in de lijst.
    * Dit voltooit de koppeling van Kanaal naar Prijsgroep naar Handelsovereenkomst.  
32. Typ een waarde in het veld Artikelrelatie.
33. Typ een getal in het veld Bedrag in valuta.
34. Schakel het selectievakje Volgende zoeken in of uit.
    * Wanneer Volgende zoeken is ingesteld op 'Ja', zoekt de prijsengine door naar toepasselijke handelsovereenkomsten met een lagere verkoopprijs. Wanneer Volgende zoeken is ingesteld op 'Nee', stopt het zoeken en wordt de handelsovereenkomst gebruikt.  
35. Klik op Boeken.
36. Klik op OK.
37. Sluit de pagina.
38. Klik in het actievenster op Verkopen.
39. Klik op Verkoopprijs.


