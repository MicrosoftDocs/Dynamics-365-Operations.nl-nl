---
title: Transacties overboeken naar Intrastat
description: Deze procedure begeleidt u bij het instellen van Intrastat-parameters en overboeken van transacties naar Intrastat.
author: AdamTrukawka
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form:
- EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines
- Intrastat, SysQueryForm, DeliveryReason, DeliveryTerms, DestinationCode
ms.openlocfilehash: 5bcb20423b9187df99c0c3078175f4a7d85d78a3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283748"
---
# <a name="transfer-transactions-to-the-intrastat"></a>Transacties overboeken naar Intrastat

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u bij het instellen van Intrastat-parameters en overboeken van transacties naar Intrastat. Deze procedure is gemaakt met het demobedrijf DEMF.


## <a name="create-new-and-update-existing-commodity-code"></a>Nieuwe basisproductcodes maken en bestaande basisproductcodes bijwerken
1. Ga in het navigatievenster naar **Modules > Productgegevensbeheer > Instellingen > Categorieën en kenmerken > Categoriehiërarchieën**.
2. Zoek of selecteer in de lijst de record **Intrastat-basisproductcodes**.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Selecteer een record in de structuur. Selecteer bijvoorbeeld **Intrastat\Luidspreker**.  
5. Klik op **Bewerken**.
6. Vouw het sneltabblad **Buitenlandse handel** uit.
7. Typ of selecteer een waarde in het veld **Extra eenheden**. Kies bijvoorbeeld **stuks**.  
8. Selecteer **Ja** in het veld **Gewicht niet van toepassing**.
9. Selecteer **Intrastat** in de structuur.
10. Klik op **Nieuw categorieknooppunt**.
11. Voer in het veld **Naam** de naam van het basisproduct in. Typ bijvoorbeeld **Ander basisproduct**.  
12. Voer in het veld **Code** de basisproductcode in. Typ bijvoorbeeld **995 00 00**.  
13. Typ een waarde in het veld Beschrijvende naam. Typ bijvoorbeeld **Overige**.  
14. Klik op **Opslaan**.
15. Sluit de pagina.

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a>Basisproductcodes toewijzen aan producthiërarchie en vrijgegeven product
1. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Naam** met de waarde **verkoop**.
2. Klik in de lijst op de koppeling in de geselecteerde rij.
3. Vouw een **categorieknooppunt** uit in de structuur. Vouw bijvoorbeeld **Verkoophiërarchie\Home audio** uit.  
4. Selecteer de **categorie om aan de basisproductcode toe te wijzen** in de structuur. Selecteer bijvoorbeeld **Verkoophiërarchie\Home audio\Luidsprekers.  
5. Vouw het sneltabblad **Basisproductcodes** uit.
6. Klik op **Toevoegen**.
7. Selecteer **Intrastat** in het veld **Hiërarchie selecteren**.
8. Zoek en selecteer de basisproductcode in de lijst. Selecteer bijvoorbeeld **Luidspreker 920 20 34**.  
9. Klik op de rechterpijl om code te selecteren.
10. Klik op **OK**.
11. Ga in het navigatievenster naar **Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
12. Kies in de lijst het vrijgegeven product dat u aan de basisproductcode toewijst. Kies bijvoorbeeld **D0001**.  
13. Klik op **Bewerken**.
14. Vouw het sneltabblad **Buitenlandse handel** uit.
15. Voer in het veld **Basisproduct** de basisproductcode in. Selecteer bijvoorbeeld de waarde **Luidspreker 920 20 34**.    
16. Voer een getal in het veld **Percentage van toeslagen** in. Voer bijvoorbeeld **3** in.  
17. Typ of selecteer in het veld **Land/regio** een land of regio van herkomst. Selecteer bijvoorbeeld **AUT**.  
18. Vouw het sneltabblad **Voorraad beheren** uit.
19. Voer in het veld **Nettogewicht** een gewicht in kg in. Voer bijvoorbeeld **2,5** in.  
20. Klik op **Opslaan**.

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a>Intrastat-transactiecodes en parameters voor buitenlandse handel instellen
1. Ga in het navigatiedeelvenster naar **Modules > Btw > Instellingen > Buitenlandse handel > Transactiecodes**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Transactiecode**. Voer bijvoorbeeld **21** in voor de transactiecode die is gebruikt als retour.  
4. Typ in het veld **Naam** de naam van de transactiecode. Voer bijvoorbeeld **Retour** in.  
5. Selecteer een optie in het veld **Statistisch bedrag**. Selecteer bijvoorbeeld **Leeg** waarmee wordt aangegeven dat de statistische waarde die voor transacties met transactiecode **21** moet worden gerapporteerd, altijd nul is.  
6. Ga in het navigatiedeelvenster naar **Modules > Btw > Instellingen > Buitenlandse handel > Parameters buitenlandse handel**.
7. Typ of selecteer een waarde in het veld **Transactiecode**. Selecteer bijvoorbeeld **11**.  
8. Typ of selecteer een waarde in het veld **Creditnota**. Met deze waarde wordt ook de fysieke retour geïdentificeerd. De creditnota voor de fysieke retour wordt in het Intrastat-journaal in tegengestelde richting overgeboekt. De retour van aankomst wordt bijvoorbeeld overgeboekt als verzending.   Anders wordt de creditnota als een correctie beschouwd en wordt deze in dezelfde richting en met het tegengesteld teken overgeboekt. De correctie van aankomst wordt overgeboekt als een aankomst met negatief bedrag en de actieve markering wordt ingesteld op **Correctie**.  
9. Vouw het sneltabblad **Overboeking** uit.
10. Selecteer **Ja** in het veld **Artikelen met basisproductcode**. Selecteer deze optie om alleen de transacties met een toegewezen basisproductcode over te boeken. Transacties zonder een basisproductcode worden niet overgeboekt naar Intrastat.  
11. Selecteer een optie in het veld **Overboeken bij overeenkomst met criterium voor**. Selecteer bijvoorbeeld **Een van de geselecteerde elementen**.  
12. Vouw de sectie **Hiërarchie van basisproductcodes** uit.
13. Klik op het tabblad **Land-/regio-eigenschappen**.
14. Klik op **Nieuw**.
15. Typ of selecteer een waarde in het **veld Land/regio**. Selecteer bijvoorbeeld de waarde **FRA**.  
16. Voer in het veld **Intrastat-code** de ISO-code voor het land in.  Typ bijvoorbeeld **FR**.  
17. Selecteer in het veld **Land-/regiotype** de waarde **EU**.
18. Klik op het tabblad Nummerreeksen.

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a>Leveringsmethoden en regels instellen voor opname van toeslagen in Intrastat
1. Ga in het navigatiedeelvenster naar **Modules > Verkoop en marketing > Instellingen > Distributie > Leveringsmethoden**.
2. Zoek en selecteer de gewenste record in de lijst. Selecteer bijvoorbeeld **20 Air**.  
3. Vouw het sneltabblad **Buitenlandse handel** uit.
4. Klik op **Bewerken**.
5. Typ of selecteer een waarde in het veld **Transport**. Selecteer bijvoorbeeld **02**.  
6. Ga in het navigatiedeelvenster naar **Modules > Klanten > Instelling van toeslagen > Toeslagencode**.
7. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Toeslagcode met de waarde **vracht**.
8. Vouw het sneltabblad **Buitenlandse handel** uit.
9. Klik op **Bewerken**.
10. Selecteer **Ja** in het veld **IIntrastat-factuurwaarde**. Het bedrag wordt overgeboekt naar het veld **Factuurtoeslagen** en wordt samengevat met het bedrag dat in het veld Factuurbedrag is overgeboekt. Selecteer **Ja** in het veld **Statistische Intrastat-waarde** als het bedrag van wijzigingen naar het veld **Statistische toeslagen** moet worden overgeboekt en samengevat met het veld **Statistisch bedrag**.  

## <a name="sell-products-for-eu-customers"></a>Producten verkopen voor klanten in de EU
1. Ga in het navigatiedeelvenster naar **Modules > Klanten > Orders > Alle verkooporders**.
2. Klik op **Nieuw**.
3. Selecteer een EU-klant in het veld **Klantrekening**. Selecteer bijvoorbeeld **DE-012 Litware Retail**.  
4. Vouw het sneltabblad **Levering** uit.
5. Typ of selecteer een waarde in het veld **Leveringsmethode**. Selecteer bijvoorbeeld **20 Air**.  
6. Klik op **OK**.
7. Selecteer e eerste rij van verkooporderregels.
8. Typ of selecteer een waarde in het veld **Artikelnummer**. Selecteer bijvoorbeeld **D001**.  
9. Vouw het sneltabblad **Regeldetails** uit.
10. Klik op het tabblad **Buitenlandse handel**. Het transport wordt automatisch ingevuld op basis van de gekozen leveringsmethode.  
11. Typ of selecteer een waarde in het veld **Haven**.
12. Klik op **Financiële items**. Op basis van de instellingen wordt dit bedrag opgenomen in **Intrastat-factuurwaarde**.  
13. Klik op **Toeslagen onderhouden**.
14. Typ of selecteer een waarde in het veld **Toeslagcode**. Selecteer bijvoorbeeld **VRACHT**.  
15. Schakel het selectievakje **Behouden** in.
16. Voer een getal in het veld **Waarde van toeslagen** in. Voer bijvoorbeeld **10** in.  
17. Klik op **Opslaan**.
18. Sluit de pagina.
19. Klik in het actievenster op **Factuur**.
20. Klik op **Factuur**.
21. Vouw de sectie **Parameters** uit.
22. Selecteer in het veld **Hoeveelheid** de optie **Alle**.
23. Vouw het sneltabblad **Instellingen** uit.
24. Voer een datum in het veld **Factuurdatum** in. Voer bijvoorbeeld **2015-01-31** in.  
25. Klik op **OK**.
26. Klik op **OK**.
27. Sluit de pagina.
28. Klik op **Nieuw**.
29. Selecteer een EU-klant in het veld **Klantrekening**. Selecteer bijvoorbeeld **DE-013 Trey Wholesales**.
30. Klik op **OK**.
31. Typ of selecteer een waarde in het veld **Artikelnummer**. Selecteer bijvoorbeeld **D0001**.  
32. Klik op **Opslaan**.
33. Klik op **Factuur**.
34. Voer een datum in het veld **Factuurdatum** in. Typ of selecteer bijvoorbeeld de datum **31-01-2015**.  
35. Klik op **OK**.
36. Klik op **OK**.

## <a name="transfer-transactions-to-the-intrastat"></a>Transacties overboeken naar Intrastat
1. Ga in het navigatiedeelvenster naar **Modules > Btw > Aangiften > Buitenlandse handel > Intrastat**.
2. Klik op **Overboeken**.
3. Selecteer **Ja** in het veld **Klantfactuur**.
4. Klik op **Filter**.
5. Markeer in de lijst de rij met **Datum**.
6. Typ een waarde in het veld **Criteria**. Voer bijvoorbeeld het filter voor de periode januari 2015 in (de exacte waarde is afhankelijk van uw datumnotatie): 1-1-2015..31-1-2015  
7. Klik op **OK**.
8. Klik op **OK**.
9. Zoek en selecteer de overgeboekte record in de lijst.
10. Klik op het tabblad **Algemeen**.
    
Controleer de overgeboekte gegevens, waaronder land/regio van bestemming/verzending, land van oorsprong, gewicht, hoeveelheid, hoeveelheid in extra eenheden, basisproduct, transactiecode, factuurbedragen en statistische bedragen. U kunt gegevens indien nodig wijzigen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
