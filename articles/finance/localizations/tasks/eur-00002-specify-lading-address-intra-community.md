---
title: EUR-00002 Een vrachtadres opgeven voor een intracommunautaire transactie
description: Deze procedure laat zien hoe u een vrachtadres opgeeft voor een intracommunautaire handelstransactie.
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
ms.search.form:
- PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, TransportationDocument, LogisticsPostalAddress, SysLookupMultiSelectGrid
- VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, Intrastat, SysQueryForm
ms.openlocfilehash: 2094d24f256647ee3193f7e069e33bf4d99c1b70
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280596"
---
# <a name="eur-00002-specifying-a-lading-address-for-an-intra-community-transaction"></a>EUR-00002 Een vrachtadres opgeven voor een intracommunautaire transactie

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een vrachtadres opgeeft voor een intracommunautaire handelstransactie. Bijvoorbeeld een Duits bedrijf bestelt artikelen bij een leverancier met een adres in Duitsland. Deze leverancier heeft een magazijn in Italië en verzendt de artikelen vandaaruit. Deze levering moet in Intrastat worden gerapporteerd. Hetzelfde gedrag geldt voor klantretouren.
Deze procedure is van toepassing op alle Europese landen/regio's. De taak werd gemaakt met het demobedrijf DEMF met een primair adres in Duitsland. Voordat u deze procedure kunt uitvoeren, moet u Intrastat-rapporten configureren. Deze procedure is alleen bedoeld voor accountants. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.

1. Ga naar Leveranciers > Inkooporders > Alle inkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde
    * Selecteer bijvoorbeeld DE-001. Deze leverancier heeft een Duits adres.  
4. Klik op OK.
5. Markeer in de lijst de geselecteerde rij.
6. Typ of selecteer een waarde D0001 in het veld Artikelnummer.
7. Klik op Opslaan.
8. Klik in het actievenster op Ontvangen.
9. Klik op Transportgegevens.
10. Typ in het veld Laaddatum en -tijd de datum en een tijd.
11. Klik op Een nieuw adres toevoegen.
12. Klik op Nieuw en maak een nieuw adres met als doel Vracht.
13. Typ Italiaans in het veld Naam of omschrijving.
14. Selecteer Vracht als de waarde.
    * Merk op dat het adresdoel Vracht moet zijn.  
15. Typ of selecteer een waarde ITA in het veld Land/regio.
16. Klik op Opslaan.
17. Sluit de pagina.
18. Klik op Opslaan.
    * Controleer of het vrachtadres juist is.  
19. Sluit de pagina.
20. Klik in het actievenster op Inkoop.
21. Klik op Bevestigen.
22. Klik in het actievenster op Factuur.
23. Klik op Factuur.
24. Typ een waarde in het veld Nummer.
25. Voer een datum in het veld Factuurdatum in.
26. Klik op Standaard vanaf: Hoeveelheid productontvangstbon om het dialoogvenster voor beëindigen te openen.
27. Selecteer Bestelde hoeveelheid in het veld Standaardhoeveelheid voor regels.
28. Klik op OK.
29. Klik op Transportgegevens.
    * Controleer of de goederen uit Italië zijn verzonden. Bewerk indien nodig de vrachtdetails.  
30. Sluit de pagina.
31. Klik op Boeken.
32. Sluit de pagina.
33. Ga naar Belasting > Aangiften > Buitenlandse handel > Intrastat.
34. Klik op Overbrengen.
35. Selecteer Ja in het veld Leveranciersfactuur.
36. Klik op OK.
37. Klik op het tabblad Algemeen.
    * Zoek een nieuwe regel en controleer of de afzender de goederen uit Italië heeft verzonden.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
