---
title: EUR-00012 Een EU-invoercertificaat uitgeven
description: Deze procedure begeleidt u bij het inschakelen van een EU-invoercertificaat, het configureren van een klantrekening om invoercertificaten te gebruiken en het uitgeven van een certificaat.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, CustTable, SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CustEntryCertificateJour_W, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41ede621fdb36d39efc79788cd2da77aacfc282895dd84d572b99f4528456643
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768232"
---
# <a name="eur-00012-issue-an-eu-entry-certificate"></a>EUR-00012 Een EU-invoercertificaat uitgeven

[!include [banner](../../includes/banner.md)]
Deze procedure begeleidt u bij het inschakelen van een EU-invoercertificaat, het configureren van een klantrekening om invoercertificaten te gebruiken en het uitgeven van een certificaat. Deze procedure is gemaakt met het demobedrijf DEMF.


## <a name="enable-entry-certificate-management"></a>Certificaatbeheer inschakelen
1. Ga naar Klanten > Instellingen > Parameters van module Klanten.
2. Klik op het tabblad Zendingen.
3. Vouw de sectie Invoercertificaat uit.
4. Selecteer Ja in het veld Certificaatbeheer inschakelen.
5. Selecteer Ja in het veld Verstrekken van invoercertificaat inschakelen.
6. Klik op het tabblad Nummerreeksen.
7. Zoek en selecteer de rij van het invoercertificaat in de lijst.
8. Typ of selecteer een waarde in het veld Nummerreekscode.

## <a name="set-up-a-customer"></a>Een klant instellen
1. Ga naar Klanten > Klanten > Alle klanten.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Rekening met een waarde van 'DE-015'.
3. Open klantrekeninggegevens.
4. Klik op Bewerken.
5. Vouw de sectie Factuur en levering uit.
6. Selecteer Ja in het veld Invoercertificaat vereist.
7. Selecteer Ja in het veld Uitgifte van invoercertificaat.
8. Klik op Opslaan.

## <a name="create-an-eu-entry-certificate-automatically"></a>Automatisch een EU-invoercertificaat maken
1. Ga naar Klanten > Orders > Alle verkooporders.
2. Klik op Nieuw.
3. Typ of selecteer een waarde in het veld Klantrekening.
4. Klik op OK.
5. Typ of selecteer een waarde in het veld Artikelnummer.
6. Klik op Opslaan.
7. Klik in het actievenster op Verzamelen en inpakken.
8. Klik op Pakbon boeken.
9. Vouw de sectie Parameters uit.
10. Selecteer in het veld Hoeveelheid de optie 'Alle'.
11. Schakel het selectievakje Uitgifte van invoercertificaat uit.
    * Een invoercertificaat kan worden uitgegeven tijdens pakbonboeking of orderfacturering. Laat het selectievakje Uitgifte van invoercertificaat uitgeschakeld om het certificaat later uit te geven.  
12. Klik op OK.
13. Klik op OK.
14. Klik in het actievenster op Factuur.
15. Klik op Factuur.
    * Controleer of de selectievakjes Invoercertificaat vereist en Uitgifte van invoercertificaat in de sectie Overzicht zijn gemarkeerd.  U kunt ook het selectievakje Invoercertificaat afdrukken inschakelen om afdrukken van het certificaat toe te staan.  
16. Klik op OK.
17. Klik op OK.
18. Klik in het actievenster op Factuur.
19. Klik op Factuur.
20. Klik in het actievenster op Factuur.
21. Klik op Uitgegeven invoercertificaten weergeven.
22. Klik op Afdrukken.
23. Sluit de pagina.
24. Klik op Status wijzigen.
25. Selecteer een optie in het veld Nieuwe status.
26. Klik op OK.
27. Sluit de pagina.

## <a name="create-an-eu-entry-certificate-manually"></a>Handmatig een EU-invoercertificaat maken
1. Klik in het actievenster op Factuur.
2. Klik op Invoercertificaat maken.
3. Klik op OK.
4. Klik in het actievenster op Factuur.
5. Klik op Uitgegeven invoercertificaten weergeven.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]