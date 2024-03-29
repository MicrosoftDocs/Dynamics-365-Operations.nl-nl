---
title: EUR-00015 Registratie van het btw-id van een leverancier
description: Deze procedure laat zien hoe u btw-registratie-id's en een btw-nummer toevoegt aan een leveranciersrekening.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
ms.openlocfilehash: ce5d2a11e1576b772a91bc58d1d7ad330e8c7481
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273746"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a>EUR-00015 Registratie van het btw-id van een leverancier

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u btw-registratie-id's en een btw-nummer toevoegt aan een leveranciersrekening. Dit proces is vergelijkbaar voor rechtspersonen en klanten. 

Voordat u deze procedure kunt uitvoeren, moet u btw-id's instellen. Deze procedure is van toepassing op alle Europese landen/regio's. De procedure is gemaakt met het demobedrijf DEMF met een primair adres in Duitsland. Deze procedure is bedoeld voor een beheerder van gegevensbeheer, leveranciers of klanten. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.

1. Ga naar Leveranciers > Leveranciers > Alle leveranciers.
2. Zoek en selecteer in de lijst klant DE-01001.
3. Klik op Registratie-id's
4. Klik op Toevoegen.
5. Selecteer Btw-id.
6. Typ een waarde in het veld Registratienummer.
    * Geef een btw-id in Duitsland op voor de geselecteerde leverancier. De id moet overeenkomen met de opgegeven indeling van het registratietype.  
7. Klik op het tabblad Algemeen.
8. Voer een datum in in het veld Ingangsdatum.
9. Klik op Opslaan.
10. Klik op Nieuw.
11. Typ een waarde in het veld Naam of omschrijving.
    * Voer bijvoorbeeld ITA in.  
12. Typ of selecteer een waarde in het veld Land/regio.
    * Selecteer bijvoorbeeld ITA.  
13. Selecteer Ja in het veld Primair voor land/regio.
14. Klik op Opslaan.
15. Klik op het tabblad Overzicht.
16. Klik op Toevoegen.
17. Typ of selecteer een waarde in het veld Registratietype.
    * Selecteer bijvoorbeeld Btw-id.  
18. Typ een waarde in het veld Registratienummer.
    * Geef bijvoorbeeld een btw-id in italië op.  De id moet overeenkomen met de indeling van het registratietype.  
19. Klik op Opslaan.
20. Sluit de pagina.
21. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer bijvoorbeeld DE-01001.  
22. Klik in de lijst op de koppeling in de geselecteerde rij.
23. Vouw de sectie Factuur en levering uit.
24. Klik op Bewerken.
25. Typ of selecteer een waarde in het veld Nummer van belastingvrijstelling.
26. Klik op Opslaan.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
