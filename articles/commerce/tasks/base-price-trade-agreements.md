---
title: " Basisprijs en handelsovereenkomsten"
description: Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten.
author: josaw1
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db3a91807c0cfb51426c03eeaf7785168e6ad0de
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006050"
---
# <a name="base-price-and-trade-agreements"></a> Basisprijs en handelsovereenkomsten

[!include [banner](../includes/banner.md)]

Deze procedure doorloopt het maken van kanaalspecifieke verkoopprijshandelsovereenkomsten. Deze procedure gebruikt het demobedrijf USRT.

1. Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Prijzen- en kortingbeheer > Prijsgroepen > Alle prijsgroepen**. Prijsgroepen bepalen hoe handelsovereenkomsten aan specifieke kanalen worden toegewezen. Als u prijsgroepen gebruikt om handelsovereenkomsten aan een kanaal toe te wijzen, worden kanaalspecifieke prijzen ingeschakeld.  
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Prijsgroepen**.
4. Typ een waarde in het veld **Naam**.
5. Klik op **Opslaan**.
6. Sluit de pagina.
7. Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Kanalen > Winkels > Alle detailhandelwinkels**.
8. Selecteer 'New York' in de lijst.
9. Klik in het actievenster op **Winkel**.
10. Klik op **Prijsgroepen**.
11. Klik op **Nieuw**.
12. Klik in het veld **Prijsgroepen** op de vervolgkeuzeknop om de zoekopdracht te openen.
13. Zoek en selecteer de gewenste record in de lijst.
14. Klik op **Opslaan**.
15. Sluit de pagina.
16. Sluit de pagina.
17. Ga in het **navigatievenster** naar **Modules > Retail en Commerce > Producten en categorieën > Vrijgegeven producten per categorie**.
18. Klik in de lijst op de koppeling in de geselecteerde rij.
19. Klik op **Bewerken**.
20. Vouw het sneltabblad **Verkopen** uit.
21. Voer een getal in het veld **Prijs** in. Deze prijs wordt gebruikt als er geen toepasselijke handelsovereenkomsten worden gevonden.  
22. Klik op **Opslaan**.
23. Klik in het **actievenster** op **Verkopen**.
24. Klik op **Handelsovereenkomsten maken**.
25. Klik op **Nieuw**.
26. Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.
27. Selecteer **Commerce** in de lijst. In de demogegevens heeft de **Commerce**-journaalnaam de standaardrelatie **Prijs (verkoop)**. Dat betekent dat alle nieuw gemaakte regels standaard verkoopprijshandelsovereenkomsten gebruiken.  
28. Klik in het **actievenster** op **Regels**.
29. Selecteer 'Groep' in het veld **Type partijcode**.
30. Klik in het veld **Rekening selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.
31. Zoek en selecteer de gewenste record in de lijst. Dit voltooit de koppeling van Kanaal naar Prijsgroep naar Handelsovereenkomst.  
32. Typ een waarde in het veld **Artikelrelatie**.
33. Typ een getal in het veld **Bedrag in valuta**.
34. Schakel op het sneltabblad **Details** het selectievakje **Volgende zoeken** in of uit. Wanneer **Volgende zoeken** is ingesteld op Ja, zoekt de prijsengine door naar toepasselijke handelsovereenkomsten met een lagere verkoopprijs. Wanneer **Volgende zoeken** is ingesteld op Nee, stopt het zoeken en wordt de handelsovereenkomst gebruikt.  
35. Klik op **Boeken**.
36. Klik op **OK**.
37. Sluit de pagina.
38. Klik in het actievenster op **Verkopen**.
39. Klik op **Verkoopprijs**.

