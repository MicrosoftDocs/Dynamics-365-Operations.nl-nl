---
title: Leveranciers voor specifieke producten goedkeuren
description: Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425389"
---
# <a name="approve-vendors-for-specific-products"></a>Leveranciers voor specifieke producten goedkeuren

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u leveranciers voor specifieke producten goedkeurt. Zo kunt u bepalen welke leveranciers kunnen worden gebruikt wanneer het product aan een inkooporder wordt toegevoegd. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Deze taak wordt meestal uitgevoerd door een inkoopmanager.

1. Ga in het navigatievenster > **Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Vouw het sneltabblad **Inkoop** uit. Als er een primaire leverancier in het veld **Leverancier** wordt weergegeven, moet u deze leverancier als een goedgekeurde leverancier toevoegen in de volgende stappen. Maak een notitie van het leveranciersnummer, als er een wordt weergegeven.  
5. Klik in het actievenster op **Inkoop**.
6. Klik op **Instellen**.
7. Klik op **Toevoegen**.
8. Typ of selecteer een waarde in het veld Leverancier. Selecteer de goedgekeurde leverancier. Ten minste een van de regels moet de primaire leverancier zijn als de productrecord er een bevatte. Als u eerder een notitie van het leveranciersnummer hebt gemaakt, selecteert u het hier.  
9. Voer in het veld **Vervaldatum** een datum in. Kies een datum een paar maanden vooruit.  
10. Klik op **Toevoegen**.
11. Typ of selecteer een waarde in het veld **Leverancier**.
12. Voer in het veld **Vervaldatum** een datum in. Kies een datum die afwijkt van de vorige vervaldatum.  
13. Sluit de pagina.
14. Klik in het actievenster op **Goedgekeurde leveranciers**.
15. Voer in het veld **Vervaldatum** een datum in. Deze datum fungeert als filter zodat u kunt zien wie de goedgekeurde leveranciers zijn, tot een bepaalde datum.  
16. Sluit de pagina.
17. Klik in het actievenster op **Geldigheidsperiode**.
18. Voer in het veld **Leveranciers weergeven die vervallen op** een datum in. U kunt deze pagina gebruiken om leveranciers te identificeren van wie de goedkeuringsstatus na een bepaalde datum vervalt.  
19. Sluit de pagina.
20. Klik op **Bewerken**.
21. Selecteer een optie in het veld **Controlemethode goedgekeurde leveranciers**. Met dit veld kunt u het beleid selecteren voor wat er moet gebeuren als het product aan een inkooporderregel wordt toegevoegd waarop de leverancier geen goedgekeurde leverancier is.  
22. Klik op **Opslaan**.
23. Sluit de pagina.
24. Sluit de pagina.
25. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Relaties tussen leveranciers en artikelen > Lijst met goedgekeurde leveranciers, gesorteerd op artikel**. Deze pagina geeft u een overzicht van alle producten en de goedgekeurde leveranciers.  
26. Sluit de pagina.
27. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**. U kunt ook beginnen bij een leverancier en vervolgens naar de lijst met goedgekeurde producten voor die leveranciersrekening gaan.  
28. Zoek en selecteer de gewenste record in de lijst.
29. Klik in het actievenster op **Inkoop**.
30. Klik op **Lijst met goedgekeurde leveranciers, gesorteerd op leverancier**.
31. Sluit de pagina.
32. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]