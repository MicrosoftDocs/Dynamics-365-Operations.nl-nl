---
title: Grondstoffen maken (februari 2016)
description: Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552665"
---
# <a name="create-raw-materials-february-2016"></a>Grondstoffen maken (februari 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taak is gericht op het maken van de componenten van eindproducten en halffabricaten. Dit is de derde taak in de reeks stuklijstberekeningen. Het bedrijf van de demogegevens dat wordt gebruikt om deze taak te maken is USMF.


## <a name="create-the-first-material"></a>De eerste grondstof maken
1. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Productnummer.
    * Typ voor dit voorbeeld: 'Artikel_A'.  
4. Typ of selecteer een waarde in het veld Artikelmodelgroep.
    * Selecteer STD. STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.  
5. Typ of selecteer een waarde in het veld Artikelgroep.
    * Selecteer bijvoorbeeld 'Audio'. Dit heeft geen invloed op de kostenberekeningen.  
6. Typ of selecteer een waarde in het veld Opslagdimensiegroep.
    * Selecteer 'SiteWH'. Alleen Locatie en Magazijn wordt gebruikt voor de demo.  
7. Typ of selecteer een waarde in het veld Traceringsdimensiegroep.
    * Traceringsdimensies worden niet voor dit voorbeeld gebruikt. Selecteer 'Geen'.  
8. Klik op OK.
9. Klik in het actievenster op Voorraad beheren.
10. Klik op Standaardorderinstellingen.
11. Typ of selecteer een waarde in het veld Inkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
12. Typ of selecteer een waarde in het veld Voorraadvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
13. Typ of selecteer een waarde in het veld Verkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
14. Sluit de pagina.
15. Sluit de pagina.
16. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op Artikel_A.  
17. Vouw de sectie Kosten beheren uit.
18. Typ een waarde in het veld Kostengroep.
    * Typ voor dit voorbeeld: 'M2'  
19. Klik in het actievenster op Kosten beheren.
20. Klik op Artikelprijs.
21. Klik op Nieuw.
22. Typ of selecteer een waarde in het veld Versie.
    * Selecteer voor dit voorbeeld 10, namelijk het kostprijsberekeningstype van de standaardkostprijs.  
23. Typ of selecteer een waarde in het veld Locatie.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
24. Voer een getal in het veld Prijs in.
    * Typ voor dit voorbeeld 10.  
25. Klik op Opslaan.
26. Klik op Prijzen in behandeling activeren.
27. Sluit de pagina.
28. Sluit de pagina.

## <a name="create-the-second-material"></a>De tweede grondstof maken
1. Klik op Nieuw.
2. Typ een waarde in het veld Productnummer.
    * Typ voor dit voorbeeld: 'Artikel_B'.  
3. Typ of selecteer een waarde in het veld Artikelmodelgroep.
    * Selecteer STD. STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.  
4. Typ of selecteer een waarde in het veld Artikelgroep.
    * Selecteer bijvoorbeeld 'Audio'. Dit heeft geen invloed op de kostenberekeningen.  
5. Typ of selecteer een waarde in het veld Opslagdimensiegroep.
    * Selecteer 'SiteWH'. Alleen Locatie en Magazijn wordt gebruikt voor dit voorbeeld.  
6. Typ of selecteer een waarde in het veld Traceringsdimensiegroep.
    * Traceringsdimensies worden niet voor dit voorbeeld gebruikt. Selecteer 'Geen'.  
7. Klik op OK.
8. Klik in het actievenster op Voorraad beheren.
9. Klik op Standaardorderinstellingen.
10. Typ of selecteer een waarde in het veld Inkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
11. Typ of selecteer een waarde in het veld Voorraadvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
12. Typ of selecteer een waarde in het veld Verkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
13. Sluit de pagina.
14. Sluit de pagina.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op Artikel_B.  
16. Vouw de sectie Kosten beheren uit.
17. Typ een waarde in het veld Kostengroep.
    * Typ voor dit voorbeeld: 'M2'  
18. Klik in het actievenster op Kosten beheren.
19. Klik op Artikelprijs.
20. Klik op Nieuw.
21. Typ of selecteer een waarde in het veld Versie.
    * Selecteer voor dit voorbeeld 10. Dit is het kostprijsberekeningstype van de standaardkostprijs.  
22. Typ of selecteer een waarde in het veld Locatie.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
23. Voer een getal in het veld Prijs in.
    * Typ voor de demonstratie 10.  
24. Klik op Opslaan.
25. Klik op Prijzen in behandeling activeren.
26. Sluit de pagina.
27. Sluit de pagina.

## <a name="create-the-third-material"></a>De derde grondstof maken
1. Klik op Nieuw.
2. Typ een waarde in het veld Productnummer.
    * Typ voor de demonstratie: 'Artikel_C'.  
3. Typ of selecteer een waarde in het veld Artikelmodelgroep.
    * Selecteer STD. STD staat voor de standaardkosten. Dit is het meestgebruikte model bij het werken met kostenberekeningen.  
4. Typ of selecteer een waarde in het veld Artikelgroep.
    * Selecteer bijvoorbeeld 'Audio'. Dit heeft geen invloed op de kostenberekeningen.  
5. Typ of selecteer een waarde in het veld Opslagdimensiegroep.
    * Selecteer 'SiteWH'. Alleen Locatie en Magazijn wordt gebruikt voor de demo.  
6. Typ of selecteer een waarde in het veld Traceringsdimensiegroep.
    * Traceringsdimensies worden niet voor dit voorbeeld gebruikt. Selecteer 'Geen'.  
7. Klik op OK.
8. Klik in het actievenster op Voorraad beheren.
9. Klik op Standaardorderinstellingen.
10. Typ of selecteer een waarde in het veld Inkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
11. Typ of selecteer een waarde in het veld Voorraadvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
12. Typ of selecteer een waarde in het veld Verkoopvestiging.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
13. Sluit de pagina.
14. Sluit de pagina.
15. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op Artikel_C.  
16. Vouw de sectie Kosten beheren uit.
17. Typ een waarde in het veld Kostengroep.
    * Typ voor dit voorbeeld: 'M1'  
18. Klik in het actievenster op Kosten beheren.
19. Klik op Artikelprijs.
20. Klik op Nieuw.
21. Typ of selecteer een waarde in het veld Versie.
    * Selecteer voor dit voorbeeld 10. Dit is het kostprijsberekeningstype van de standaardkostprijs.  
22. Typ of selecteer een waarde in het veld Locatie.
    * Selecteer voor dit voorbeeld 'Locatie 1.'  
23. Voer een getal in het veld Prijs in.
    * Typ voor dit voorbeeld 10.  
24. Klik op Opslaan.
25. Klik op Prijzen in behandeling activeren.
26. Sluit de pagina.
27. Sluit de pagina.

