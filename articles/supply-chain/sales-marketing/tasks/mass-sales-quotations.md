---
title: Verkoopoffertes massaal maken
description: Deze procedure toont hoe u efficiënt offertes maakt met een reeks producten of services die naar meerdere klanten moeten worden verzonden.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6cbeadb29c58f8ca77721c8f867836d8830803f2b89b82a544be4d2a03db750f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756818"
---
# <a name="mass-create-sales-quotations"></a>Verkoopoffertes massaal maken

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u efficiënt offertes maakt met een reeks producten of services die naar meerdere klanten moeten worden verzonden. Dit groepsgewijs maken van offertes is gebaseerd op offertesjablonen. U kunt deze procedure uitvoeren met uw eigen gegevens of in het demogegevensbedrijf USMF.


## <a name="create-a-quotation-template"></a>Een offertesjabloon maken
1. Ga naar Verkoop en marketing > Instellen > Offertes > Sjabloongroepen.
2. Klik op Nieuw.
3. Typ een id van uw keuze in het veld Groep-id.
4. Typ een waarde in het veld Omschrijving.
5. Klik op Opslaan.
6. Sluit de pagina.
7. Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.
8. Klik op Nieuw.
9. Selecteer in het veld Rekeningtype de optie 'Klant'.
10. Typ of selecteer een waarde in het veld Klantrekening.
11. Klik op OK.
    * Een offerte kan alleen een sjabloon worden als u op de offerteheader instellingsstappen uitvoert. U moet dit doen voordat u regels aan de offerte toevoegt.   
12. Klik in het actievenster op Opties.
13. Klik op Weergave wijzigen.
14. Klik op Weergave headers.
15. Vouw de sectie Instellingen uit.
16. Typ of selecteer een waarde in het veld Groep-id.
17. Typ een waarde in het veld Sjabloonnaam.
18. Selecteer Ja in het veld Actief.
    * U kunt alleen actieve sjablonen gebruiken wanneer u een sjabloon toepast op een nieuwe verkoopofferte.  
19. Klik in het actievenster op Opties.
20. Klik op Weergave wijzigen.
21. Klik op Regelweergave.
22. Typ of selecteer een waarde in het veld Artikel.
23. Typ een waarde in het veld Artikel.
24. Sluit de pagina.
25. Voer in het veld Kortingspercentage een getal in.
26. Klik op Regel toevoegen.
27. Typ of selecteer een waarde in het veld Artikel.
28. Typ een waarde in het veld Artikel.
29. Sluit de pagina.
30. Typ in het veld Eenheidsprijs een nieuwe prijs of wijzig de huidige.
31. Klik op Regel toevoegen.
32. Typ of selecteer een waarde in het veld Artikel.
33. Typ een waarde in het veld Artikel.
34. Sluit de pagina.
35. Voer in het veld Hoeveelheid een getal in.
36. Typ een nummer in het veld Korting.
37. Klik op Opslaan.

## <a name="apply-the-template-to-create-a-single-quotation"></a>De sjabloon toepassen om één offerte te maken
1. Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.
    * De offerte die u zojuist hebt gemaakt is als sjabloon gemarkeerd.  
2. Klik op Nieuw.
3. Selecteer in het veld Rekeningtype de optie 'Klant'.
4. Typ of selecteer een waarde in het veld Klantrekening.
5. Vouw de sectie Sjabloon uit.
6. Typ of selecteer een waarde in het veld Groep-id.
7. Typ of selecteer een waarde in het veld Sjabloonnaam.
8. Selecteer 'Op basis van sjabloonwaarden' in het veld Berekeningsmethode.
9. Klik op OK.
    * De nieuwe offerte is nu gemaakt, gebaseerd op de gegevens en de voorwaarden van de sjabloon.  
10. Sluit de pagina.
11. Sluit de pagina.

## <a name="apply-the-template-to-mass-create-quotations"></a>De sjabloon toepassen om meerdere offertes te maken
1. Ga naar Verkoop en marketing > Verkoopoffertes > Bijwerking offerte > Massaal offertes maken.
2. Selecteer in het veld Rekeningtype de optie 'Klant'.
3. Typ of selecteer een waarde in het veld Groep-id.
4. Typ of selecteer een waarde in het veld Sjabloonnaam.
5. Selecteer 'Op basis van sjabloonwaarden' in het veld Berekeningsmethode.
6. Breid de sectie Op te nemen records uit.
7. Klik op Filter.
8. Stel in het veld Criteria het filter in om een bereik van klanten te dekken die u bij het groepsgewijs maken van deze offerte wilt opnemen. Gebruik de volgende indeling: 'Klant1. KlantN'.
    * U kunt bijvoorbeeld het filter instellen: US-001..US-004  
9. Klik op OK.
10. Klik op OK.
11. Ga naar Verkoop en marketing > Verkoopoffertes > Alle offertes.
    * Controleer of er offertes zijn gemaakt voor alle klanten die in de routine voor groepsgewijs bijwerken zijn opgegeven, op basis van de geselecteerde sjabloon.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]