---
title: ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de documentbeheerbestanden in ER-uitvoer.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfcc03fa7470d4f2fa45ef012e30acef0712bf99
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681848"
---
# <a name="er-use-document-management-files-in-format-outputs-part-3---create-format"></a>ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (deel 3 - Indeling maken)

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indeling voor elektronische rapportage (ER) kan maken met de Documentbeheerbestanden (bijlagen) in ER-uitvoer. Deze stappen kunnen in elk bedrijf worden uitgevoerd.

Als u deze stappen wilt uitvoeren, voert u eerst de stappen uit in de procedure "ER Documentbeheerbestanden gebruiken in uitvoer van indelingen (Deel 2: Gegevensmodel uitbreiden)".

Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="create-a-format-to-process-invoices"></a>Maak een indeling om facturen te verwerken
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Vouw in de structuur Klantfactuurmodel uit.
4. Selecteer in de structuur Klantfactuurmodel\Klantfactuurmodel (aangepast).
    * U maakt een indeling om elektronische berichten te genereren met informatie over de bestanden die aan een verkooporder zijn gekoppeld die samenhangt met een elektronisch verwerkte factuur.  
5. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
6. Typ Indeling gebaseerd op gegevensmodel Klantfactuurmodel (aangepast) in het veld Nieuw.
7. Typ Voorbeeldbericht elektronische factuur in het veld Naam.
    * Voorbeeldbericht elektronische factuur  
8. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
    * InvoiceCustomer  
9. Klik op Configuratie maken.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Ontwerp een indeling om bijlagen te vullen om een bericht in MIME-indeling te genereren
1. Klik op Ontwerper.
2. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
3. Selecteer "XML\Element" in de structuur.
4. Typ Factuur in het veld Naam.
    * Factuur  
5. Klik op OK.
6. Klik op Toevoegen om het dialoogvenster te openen.
7. Selecteer "XML\Attribute" in de structuur.
8. Typ SalesOrder in het veld Naam.
    * SalesOrder  
9. Klik op OK.
10. Klik op Kenmerk toevoegen.
11. Typ InvoiceNumber in het veld Naam.
    * InvoiceNumber  
12. Klik op OK.
13. Klik op Kenmerk toevoegen.
14. Typ InvoiceAmount in het veld Naam.
    * InvoiceAmount  
15. Klik op OK.
16. Klik op Toevoegen om het dialoogvenster te openen.
17. Selecteer "XML\Element" in de structuur.
18. Typ EnclosedDocs in het veld Naam.
    * EnclosedDocs  
19. Klik op OK.
20. Selecteer in de structuur Factuur\EnclosedDocs.
21. Klik op Element toevoegen.
22. Typ Document in het veld Naam.
    * Document  
23. Klik op OK.
24. Selecteer in de structuur Factuur\EnclosedDocs\Document.
25. Klik op Toevoegen om het dialoogvenster te openen.
26. Selecteer "XML\Attribute" in de structuur.
27. Typ FileName in het veld Naam.
    * FileName  
28. Klik op OK.
29. Klik op Toevoegen om het dialoogvenster te openen.
30. Selecteer "XML\Element" in de structuur.
31. Typ FileContent in het veld Naam.
    * FileContent  
32. Klik op OK.
33. Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent.
34. Klik op Toevoegen om het dialoogvenster te openen.
35. Selecteer Tekst\Base64 in de structuur.
36. Klik op OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Indelingselementen aan gegevensmodel toewijzen als gegevensbron
1. Selecteer in de structuur Factuur\SalesOrder.
2. Klik op het tabblad Toewijzing.
3. Vouw in de structuur "model" uit.
4. Selecteer in de structuur Model\Verkoopordernummer (Salesid).
5. Klik op Binden.
6. Selecteer in de structuur Factuur\InvoiceNumber.
7. Vouw in de structuur model\Base invoice(InvoiceBase) uit.
8. Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurnummer(Id).
9. Klik op Binden.
10. Selecteer in de structuur Factuur\InvoiceAmount.
11. Selecteer in de structuur model\Base invoice(InvoiceBase)\Factuurbedrag(Amount).
12. Klik op Binden.
13. Vouw in de structuur model\Factuurbijlagen uit.
14. Selecteer in de structuur model\Factuurbijlagen\Bestandsinhoud.
15. Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\Base64.
16. Klik op Binden.
17. Selecteer in de structuur model\Factuurbijlagen\Bestandsnaam.
18. Selecteer in de structuur Factuur\EnclosedDocs\Document\FileContent\FileName.
19. Klik op Binden.
20. Selecteer in de structuur model\Factuurbijlagen.
21. Selecteer in de structuur Factuur\EnclosedDocs\Document.
22. Klik op Binden.
23. Klik op Opslaan.
24. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]