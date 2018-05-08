--- 
title: " Producten verzenden van distributiecentrum naar winkel via klantlevering"
description: Deze procedure doorloopt de stappen om een klantlevering te maken en te verwerken om producten van een ontvangende locatie naar een of meer winkels te distribueren.
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 9d9a5d4fdece1cfb573224bd54d96ccd281c0f09
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a> Producten verzenden van distributiecentrum naar winkel via klantlevering

[!include [task guide banner](../includes/task-guide-banner.md)]

Deze procedure doorloopt de stappen om een klantlevering te maken en te verwerken om producten van een ontvangende locatie naar een of meer winkels te distribueren. De gebruiker kan meerdere configuraties definiëren en het systeem laten voorstellen hoe u de producten wilt verdelen, of handmatig invoeren waar de producten naar worden gedistribueerd en hoeveel naar elke winkel wordt verdeeld. Deze procedure bevat geen instelling van gegevens die in de klantlevering kunnen worden gebruikt, zoals aanvullingsregels, organisatiehiërarchieën en winkelgewichten. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Klantlevering.
2. Klik op Nieuw.
3. Typ een waarde in het veld Omschrijving.
4. Typ of selecteer een waarde in het veld Locatie.
5. Typ of selecteer in het veld Magazijn een magazijn dat producten met voorhanden hoeveelheden heeft.
6. Klik op Toevoegen.
7. Markeer in de lijst de geselecteerde rij.
8. Typ of selecteer een product in het veld Artikelnummer.
9. Klik op Toevoegen.
10. Markeer in de lijst de geselecteerde rij.
11. Typ of selecteer een variantproduct in het veld Artikelnummer.
    * Wanneer een variantproduct wordt ingevoerd, worden voor elke variant regels gemaakt.  
12. Markeer een rij in de lijst.
13. Typ in het veld In het Geleverde hoeveelheid hoeveel van het geselecteerde product u wilt verdelen.
14. Voer in het veld Bijkomende hoeveelheid voor levering de hoeveelheid in van de producten die beschikbare te verdelen hoeveelheid hebben.
15. Voer in het veld Distributie 'Locatiegewicht' in.
    * U kunt de andere typen selecteren om andere regels voor de verdeling te gebruiken.  
16. Selecteer een waarde in het veld Aanvullingshiërarchie.
17. Selecteer Ja in het veld Assortimenten respecteren.
18. Klik op Hoeveelheden berekenen en controleer de hoeveelheden die aan de rijen in de sectie Magazijn zijn toegevoegd.
19. Klik op Order maken.
20. Klik op Ja.


