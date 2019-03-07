---
title: Voorraadniveaus in het magazijn initiëren
description: Deze procedure laat zien hoe u de voorhanden voorraad handmatig bijwerkt met behulp van een voorraadmutatiejournaal.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bfa40c19e34631edb68b8cff42e7f72eb9ce2ad
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "332283"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>Voorraadniveaus in het magazijn initiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u de voorhanden voorraad handmatig bijwerkt met behulp van een voorraadmutatiejournaal. (Het is ook mogelijk om voorhanden voorraad bij te werken door transacties in gegevensentiteiten te importeren.) U kunt deze handleiding in het demobedrijf USMF uitvoeren, waar alle vereisten zoals journaalnaam, artikelinstelling, boekingsprofielen en rekeningen beschikbaar zijn. De handleiding suggereert specifieke waarden voor het artikel en de dimensies die worden gebruikt. Als u een ander artikel kiest, moet u mogelijk waarden voor andere dimensies invoeren.

1. Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Mutatie.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer IMov.
    * Het is een goed idee om verschillende journaalnaamsjablonen te gebruiken voor verschillende bedrijfsdoeleinden.  
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Geef in het veld Tegenrekening de waarden '140200' op.
    * Dit is de tegenrekening die de standaardrekening is op de journaalregels. Het is mogelijk om de standaardwaarde te negeren om verschillende tegenrekeningen per regel toe te wijzen.  
7. Klik op OK.
8. Klik op Nieuw.
9. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
10. Selecteer artikel A0001.
11. Klik in de lijst op de koppeling in de geselecteerde rij.
12. Klik op het tabblad Voorraaddimensies.
13. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
14. Selecteer site 1.
15. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
16. Selecteer magazijn 13.
17. Klik in de lijst op de koppeling in de geselecteerde rij.
18. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
19. Selecteer locatie 13.
20. Voer in het veld Hoeveelheid een getal in.
21. Klik op Opslaan.
22. Klik op Boeken.
23. Schakel het selectievakje Alle boekingsfouten overboeken naar een nieuw journaal in of uit.
    * Als u deze optie inschakelt, worden eventuele regels die er niet in slagen te boeken, naar een nieuw journaal gekopieerd. Deze procedure gebruikt de informatie in het logboek om de problemen te corrigeren en boekt vervolgens de regels opnieuw.  
24. Klik op OK.
25. Sluit de pagina.
26. Sluit de pagina.

