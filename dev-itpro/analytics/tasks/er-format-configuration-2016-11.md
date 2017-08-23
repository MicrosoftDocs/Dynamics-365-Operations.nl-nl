--- 
title: Een indelingsconfiguratie maken voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c46b222cb12d0432609c47f89afc522e02c41ab6
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a>Een indelingsconfiguratie maken voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER). Deze indelingsconfiguratie definieert de indeling van elektronische documenten die wordt gebruikt voor het verwerken van betalingen. In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf, Litware, Inc. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure Model toewijzen aan geselecteerde gegevensbronnen eerst uitvoeren.


## <a name="create-a-new-format-configuration"></a>Een nieuwe indelingsconfiguratie maken
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Klik op Rapportconfiguraties.
3. Selecteer "Payments (simplified model)" in de structuur.
4. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
5. Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.
6. Typ "BACS (UK fictief)" in het veld Naam.
    * BACS (UK fictief)  
7. Typ "BACS-indeling voor leveranciersbetalingen (UK fictief)" in het veld Beschrijving.
    * Indeling voor BACS-leveranciersbetaling (UK fictief)  
    * De actieve configuratieprovider wordt hier automatisch ingevoerd. Deze provider kan deze configuratie onderhouden. Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.  
    * Er kan een specifieke indeling voor elektronische documenten worden gedefinieerd. Laat dit veld leeg als u een indeling wilt selecteren bij de uitvoering.  
8. Typ of selecteer een waarde in het veld Definitie gegevensmodel.
9. Klik op Configuratie maken.
    * Er is een nieuwe configuratie gemaakt. De conceptversie kan worden gebruikt om de ontwerpindeling op te slaan voor het beheren van elektronische documenten.  

## <a name="design-format-of-electronic-document"></a>Indeling van elektronisch document ontwerpen
1. Klik op Ontwerper.
2. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
3. Selecteer "Common\File" in de structuur.
4. Typ "XML" in het veld Naam.
    * XML  
5. Typ "UTF-8" in het veld Codering.
    * UTF-8  
6. Klik op OK.
7. Klik op Toevoegen om het dialoogvenster te openen.
8. Selecteer "XML\Element" in de structuur.
9. Typ "Bericht" in het veld Naam.
    * Bericht  
10. Klik op OK.
11. Selecteer in de structuur 'Xml\Message'.
12. Klik op Element toevoegen.
13. Typ "ProcessingDate" in het veld Naam.
    * ProcessingDate  
14. Klik op OK.
15. Klik op Element toevoegen.
16. Typ "MessageId" in het veld Naam.
    * MessageId  
17. Klik op OK.
18. Klik op Element toevoegen.
19. Typ "Payments" in het veld Naam.
    * Betalingen  
20. Klik op OK.
21. Selecteer in de structuur 'Xml\Message\Payments'.
22. Klik op Element toevoegen.
23. Typ "Item" in het veld Naam.
    * Artikel  
24. Klik op OK.
25. Selecteer in de structuur 'Xml\Message\Payments\Item'.
26. Klik op Toevoegen om het dialoogvenster te openen.
27. Selecteer "XML\Attribute" in de structuur.
28. Typ "Id" in het veld Naam.
    * Id  
29. Klik op OK.
30. Klik op Toevoegen om het dialoogvenster te openen.
31. Selecteer "XML\Element" in de structuur.
32. Typ "Vendor" in het veld Naam.
    * Leverancier  
33. Klik op OK.
34. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor'.
35. Klik op Element toevoegen.
36. Typ "Name" in het veld Naam.
    * Naam  
37. Klik op OK.
38. Klik op Element toevoegen.
39. Typ "Bank" in het veld Naam.
    * Bank  
40. Klik op OK.
41. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank'.
42. Klik op Element toevoegen.
43. Typ "RoutingNumber" in het veld Naam.
    * RoutingNumber  
44. Klik op OK.
45. Klik op Element toevoegen.
46. Typ "AccountNumber" in het veld Naam.
    * AccountNumber  
47. Klik op OK.
48. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor'.
49. Klik op Kopiëren.
50. Selecteer in de structuur 'Xml\Message\Payments\Item'.
51. Klik op Plakken.
52. Typ "Payer" in het veld Naam.
    * Betaler  
53. Selecteer in de structuur 'Xml\Message\Payments\Item'.
54. Klik op Element toevoegen.
55. Typ "Currency" in het veld Naam.
    * Valuta  
56. Klik op OK.
57. Klik op Element toevoegen.
58. Typ "Description" in het veld Naam.
    * Omschrijving  
59. Klik op OK.
60. Klik op Element toevoegen.
61. Typ "TransDate" in het veld Naam.
    * Transactiedatum  
62. Klik op OK.
63. Klik op Element toevoegen.
64. Typ "Amount" in het veld Naam.
    * Bedrag  
65. Klik op OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Indelingsonderdelen voorbereiden voor toewijzing aan gegevensmodelelementen
1. Selecteer in de structuur 'Xml\Message\ProcessingDate'.
2. Klik op Toevoegen om het dialoogvenster te openen.
3. Selecteer in de structuur 'Text\DateTime'.
4. Typ "yyyy-MM-dd" in het veld Notatie.
    * jjjj-MM-dd  
5. Klik op OK.
6. Selecteer in de structuur 'Xml\Message\Payments\Item\TransDate'.
7. Klik op Datum/tijd toevoegen.
8. Typ "yyyy-MM-dd" in het veld Notatie.
    * jjjj-MM-dd  
9. Selecteer in het veld van het type Datum/tijd de waarde 'Datum'.
10. Klik op OK.
11. Selecteer in de structuur 'Xml\Message\MessageId'.
12. Klik op Toevoegen om het dialoogvenster te openen.
13. Selecteer "Text\String" in de structuur.
14. Klik op OK.
15. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Name'.
16. Klik Tekenreeks toevoegen.
17. Klik op OK.
18. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.
19. Klik Tekenreeks toevoegen.
20. Klik op OK.
21. Selecteer in de structuur 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.
22. Klik Tekenreeks toevoegen.
23. Klik op OK.
24. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Name'.
25. Klik Tekenreeks toevoegen.
26. Klik op OK.
27. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.
28. Klik Tekenreeks toevoegen.
29. Klik op OK.
30. Selecteer in de structuur 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.
31. Klik Tekenreeks toevoegen.
32. Klik op OK.
33. Selecteer in de structuur 'Xml\Message\Payments\Item\Currency'.
34. Klik Tekenreeks toevoegen.
35. Klik op OK.
36. Selecteer in de structuur 'Xml\Message\Payments\Item\Description'.
37. Klik Tekenreeks toevoegen.
38. Klik op OK.
39. Selecteer in de structuur 'Xml\Message\Payments\Item\Amount'.
40. Klik Tekenreeks toevoegen.
41. Klik op OK.
42. Klik op Opslaan.
43. Sluit de pagina.


