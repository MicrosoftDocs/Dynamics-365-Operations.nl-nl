--- 
title: Indeling wijzigen en uitvoeren voor gebruik van documentbeheerbestanden in uitvoerindelingen voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: e145c4c7a1f3fd88481ad32d0af05511437e21dc
ms.contentlocale: nl-nl
ms.lasthandoff: 11/02/2017

---
# <a name="modify-and-run-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Indeling wijzigen en uitvoeren voor gebruik van documentbeheerbestanden in uitvoerindelingen voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in het DEMF-bedrijf worden uitgevoerd.

Om deze stappen uit te voeren, moet u eerst de stappen in de procedure "ER Documentbeheerbestanden gebruiken in indelingsuitvoer (deel 4: indeling uitvoeren)".

Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format"></a>De indeling voor het vullen van bijlagen aanpassen zodat berichten in binaire indeling worden gegenereerd
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur Klantfactuurmodel uit.
3. Vouw in de structuur 'Customer invoice model\Customer invoice model (custom)' uit.
4. Selecteer in de structuur 'Customer invoice model\Customer invoice model (custom)\Electronic invoice sample message'.
5. Klik op Ontwerper.
    * U voert het facturenbericht in de producerende uitvoer in als een XML-bestand met UNICODE-codering.  
6. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
7. Selecteer "Common\File" in de structuur.
8. Typ "XML-bericht" in het veld Naam.
    * Xml=bericht  
9. Typ "UTF-8" in het veld Codering.
    * UTF-8  
10. Klik op OK.
    * Configureer de producerende uitvoer als gecomprimeerd bestand.  
11. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
12. Selecteer in de structuur "Common\Folder".
13. Typ in het veld Naam 'Zip output'.
    * Zip-uitvoer  
14. Klik op OK.
15. Selecteer in de structuur 'Zip output'.
    * Voeg bijlagen toe aan het producerende gecomprimeerde bestand als bestanden met oorspronkelijke namen en extensies.  
16. Klik op Toevoegen om het dialoogvenster te openen.
17. Selecteer "Common\File" in de structuur.
18. Typ in het veld Naam 'Attached file'.
    * Gekoppeld bestand  
19. Klik op OK.
20. Selecteer in de structuur 'Zip output\Attached file'.
21. Klik op Toevoegen om het dialoogvenster te openen.
22. Selecteer Tekst\Base64 in de structuur.
23. Klik op OK.

## <a name="map-new-format-elements-to-data-model"></a>Nieuwe indelingselementen toewijzen aan gegevensmodellen
1. Klik op het tabblad Toewijzing.
2. Vouw in de structuur "model" uit.
3. Vouw in de structuur model\Factuurbijlagen uit.
4. Selecteer in de structuur 'Zip output\Attached file\Base64'.
5. Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.
6. Klik op Binden.
7. Selecteer in de structuur 'Zip output\Attached file'.
8. Klik op Bestandsnaam bewerken.
9. Vouw in de structuur "model" uit.
10. Vouw in de structuur model\Factuurbijlagen uit.
11. Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.
12. Klik op Gegevensbron toevoegen.
13. Klik op Opslaan.
14. Sluit de pagina.
15. Selecteer in de structuur model\Factuurbijlagen.
16. Klik op Binden.
17. Klik op Opslaan.
18. Sluit de pagina.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Het ontworpen rapport uitvoeren voor de geselecteerde factuur
1. Klik op Uitvoeren.
2. Vouw de records uit zodat de sectie () is opgenomen.
3. Klik op Filter.
4. Selecteer de rij van het Klantfacturenjournaal en het veld Verkooporder.
5. Type in het veld Criteria in het veld met criteria voor “Verkooporder” het ordernummer 000148.
    * 000148  
6. Klik op OK.
7. Klik op OK.
    * Controleer de gegenereerde uitvoer. Naast het factuurbericht in XML-indeling is voor elke bijlage één bestand gemaakt. De bijlagebestanden worden gevuld met de gecomprimeerde uitvoer in binaire indeling.  


