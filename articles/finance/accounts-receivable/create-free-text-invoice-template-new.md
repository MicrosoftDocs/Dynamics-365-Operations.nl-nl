---
title: Een sjabloon voor vrije-tekstfacturen maken
description: In deze procedure wordt beschreven hoe u een sjabloon voor een terugkerende vrije-tekstfactuur maakt.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8281de3cb336d9392a6a97f98e51a2a139a384c5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441829"
---
# <a name="create-a-free-text-invoice-template"></a>Een sjabloon voor vrije-tekstfacturen maken

[!include [banner](../includes/banner.md)]

Gebruik voor deze procedure het demobedrijf USMF. Deze procedure is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.

## <a name="create-a-template"></a>Een sjabloon maken

1. Ga naar Klanten > Facturen > Terugkerende facturen > Vrije-tekstfactuursjablonen.
    * Met dit formulier kunt u sjablonen voor vrije-tekstfacturen maken met factuurregels, toeslagen, een boekhoudingsverdelingsjabloon en gegevens over grootboekrekeningen.  
2. Klik op Nieuw om een nieuwe sjabloon voor een terugkerende vrije-tekstfactuur te maken.
3. Typ een waarde in het veld Sjabloonnaam.
    * "Sjabloonnaam" identificeert op unieke wijze een sjabloon voor vrije-tekstfacturen. Twee sjablonen kunnen niet dezelfde "Sjabloonnaam" hebben.  
4. Voer in het veld Beschrijving een omschrijving van de sjabloon in.
5. Vouw het tabblad Factuurregels uit.
6. Voer in het veld Beschrijving een omschrijving in voor de factuurregel.
7. Selecteer in het veld Hoofdrekening een opbrengstrekening.
    * U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.  
8. Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.  
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Selecteer in het veld Btw-groep voor artikel de btw-groep voor artikel voor de huidige factuurregel.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
12. Typ of bekijk in het veld Eenheidsprijs de prijs per eenheid voor factuurregel.
    * Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.  
13. Voeg een nieuwe regel toe aan een sjabloon voor een vrije-tekstfactuur.
14. Voer in het veld Beschrijving een omschrijving in voor de factuurregel.
15. Selecteer in het veld Hoofdrekening een opbrengstrekening.
    * U kunt de tegenrekening voor transacties van een klantkrediet voor het totaalbedrag van de factuur selecteren op de pagina Boekingsprofielen van klant.  
16. Klik in het veld Btw-groep op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De btw-groep voor de huidige factuurregel. Dit is de standaard-btw-groep voor de klantrekening.  
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik in het veld Btw-groep van artikel op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De artikel-btw-groep voor de huidige factuurregel.  
19. Klik in de lijst op de koppeling in de geselecteerde rij.
20. Het aantal eenheden voor de factuurregel invoeren of bekijken
    * Dit getal wordt vermenigvuldigd met de waarde in het veld Eenheidsprijs om het bedrag van de factuurregel te berekenen.  
21. De prijs per eenheid voor de factuurregel bekijken of invoeren. 
    * Dit bedrag wordt vermenigvuldigd met de waarde in het veld Hoeveelheid om het bedrag van de factuurregel te berekenen.  
22. Bekijk en wijzig de boekhoudingsverdelingen voor een afzonderlijke regel en eventuele onderliggende regels.
    * Boekhoudingsverdelingen bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst.  
23. Werk de boekhoudingsverdelingen voor de geselecteerde factuurregel bij.
24. Klik op Sluiten.

## <a name="save-a-free-text-invoice-as-a-template"></a>Een vrije-tekstfactuur opslaan als een sjabloon
U kunt ook een bestaande vrije-tekstfactuur als een sjabloon opslaan. Wanneer u Opslaan in sjabloon selecteert op het tabblad Factuur, moet u een naam en beschrijving voor de sjabloon opgeven. Als er al een sjabloon met deze naam bestaat, wordt dit in een melding aangegeven. U kunt nog steeds op OK klikken om deze sjabloon te vervangen. 
