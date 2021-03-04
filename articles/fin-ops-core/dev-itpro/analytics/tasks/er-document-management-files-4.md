---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de documentbeheerbestanden in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89e09d79389dc2c883c429cfee3164632e0cdc0f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681776"
---
# <a name="er-use-document-management-files-in-format-outputs-part-4---run-format"></a>ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 4 - Indeling uitvoeren)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 3: Indeling maken)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Vereiste bijlagen toevoegen voor een verkooporder van één factuur
1. Ga naar Klanten > Facturen > Openstaande klantfacturen.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld Factuur met de waarde 'CIV-000148'.
    * CIV-000148  
3. Klik om de koppeling van de geselecteerde factuur te volgen.
    * CIV-000148  
4. Klik om de koppeling in het veld Verkooporder te volgen.
    * 000148  
5. Selecteer in het veld Regels of koptekst de optie Koptekst.
    * Koptekst selecteren om aan te geven dat dit het doel voor het toevoegen van bijlagen is.  
6. Klik op Koppelen.
    * Voeg een paar bestanden als bijlagen voor deze verkooporder toe. Gebruik de bestanden van de documenttypen die worden ondersteund door Documentbeheer (met bestandextensies DOCX, DPF, XML, JPG, enzovoort.). Blader en selecteer bestanden die met de bijbehorende factuur in het ER elektronische bericht moeten worden gekoppeld en verwerkt.  
7. Klik op Nieuw.
8. Klik op Bestand.
9. Klik op Nieuw.
10. Klik op Bestand.
11. Sluit de pagina.
12. Sluit de pagina.
13. Sluit de pagina.
14. Sluit de pagina.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Het ontworpen rapport uitvoeren voor de geselecteerde factuur
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur Klantfactuurmodel uit.
3. Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.
4. Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Klik op Uitvoeren.
6. Vouw de records uit zodat de sectie () is opgenomen.
7. Klik op Filter.
8. Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.
9. Typ 000148 in het veld Criteria.
    * Typ in het criteriaveld "Verkooporder" het ordernummer 000148.  
10. Klik op OK.
11. Klik op OK.
    * Controleer de gegenereerde uitvoer. Merk op dat voor elke bijlage één XML-knooppunt is gemaakt. De inhoud van de bijlage is gevuld met de XML-uitvoer in de tekstindeling MIME (base64).  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]