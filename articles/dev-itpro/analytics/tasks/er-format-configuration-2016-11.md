--- 
title: 'ER: Een indelingsconfiguratie maken (november 2016)'
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER).
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: nl-nl
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a>ER: Een indelingsconfiguratie maken (november 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een indelingsconfiguratie kan maken voor elektronische rapportage (ER). Deze indelingsconfiguratie definieert de indeling van elektronische documenten die wordt gebruikt voor het verwerken van betalingen. In dit voorbeeld maakt u een indelingsconfiguratie voor het voorbeeldbedrijf, Litware, Inc. Als u deze stappen wilt uitvoeren, moet u de stappen in de procedure Model toewijzen aan geselecteerde gegevensbronnen eerst uitvoeren.


## <a name="create-a-new-format-configuration"></a>Een nieuwe indelingsconfiguratie maken
1. Ga naar **Organisatiebeheer > Werkruimten > Elektronische rapportage**.
2. Klik op **Rapportconfiguraties**.
3. Selecteer **Betalingen (vereenvoudigd model)** in de structuur.
4. Klik op **Configuratie maken** om het dialoogvenster voor beëindigen te openen.

 > [!NOTE]
 > Als **Configuratie maken** niet wordt weergegeven, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage**. 
 
5. Voer in het veld **Nieuw** **Indeling gebaseerd op gegevensmodel PaymentModel** in.
6. Typ **BACS (UK fictief)** in het veld **Naam**.
7. Typ **BACS-indeling voor leveranciersbetalingen (UK fictief)** in het veld **Beschrijving**.
    * De actieve configuratieprovider wordt hier automatisch ingevoerd. Deze provider kan deze configuratie onderhouden. Andere providers kunnen deze configuratie wel gebruiken, maar niet onderhouden.  
    * Er kan een specifieke indeling voor elektronische documenten worden gedefinieerd. Laat dit veld leeg als u een indeling wilt selecteren bij de uitvoering.  
8. Typ of selecteer een waarde in het veld **Definitie gegevensmodel**.
9. Klik op **Configuratie maken**. Er is een nieuwe configuratie gemaakt. De conceptversie kan worden gebruikt om de ontwerpindeling op te slaan voor het beheren van elektronische documenten.  

 > [!NOTE]
 > Als **Configuratie maken** niet wordt weergegeven, moet u de ontwerpmodus inschakelen op de pagina **Parameters van elektronische rapportage**.


## <a name="design-the-format-of-an-electronic-document"></a>De indeling van een elektronisch document ontwerpen
1. Klik op **Ontwerper**.
2. Klik op **Basis toevoegen** om het dialoogvenster voor beëindiging te openen.
3. Selecteer **Common\File** in de structuur.
4. Typ **XML** in het veld **Naam**.
5. Typ **UTF-8** in het veld **Codering**.
6. Klik tot slot op **OK**.
7. Klik op **Toevoegen**.
8. Selecteer **XML\Element** in de structuur.
9. Typ **Message** in het veld **Naam**.
10. Klik tot slot op **OK**.
11. Selecteer **Xml\Message** in de structuur.
12. Klik op **Element toevoegen**.
13. Typ **ProcessingDate** in het veld **Naam**.
14. Klik tot slot op **OK**.
15. Klik op **Element toevoegen**.
16. Typ **MessageId** in het veld Naam.
17. Klik tot slot op **OK**.
18. Klik op **Element toevoegen**.
19. Typ **Payments** in het veld **Naam**.
20. Klik tot slot op **OK**.
21. Selecteer **Xml\Message\Payments** in de structuur.
22. Klik op **Element toevoegen**.
23. Typ **Item** in het veld **Naam**.
24. Klik tot slot op **OK**.
25. Selecteer **Xml\Message\Payments\Item** in de structuur.
26. Klik op **Toevoegen**.
27. Selecteer **XML\Attribute** in de structuur.
28. Typ **Id** in het veld Naam.
29. Klik tot slot op **OK**.
30. Klik op **Toevoegen**.
31. Selecteer **XML\Element** in de structuur.
32. Typ **Vendor** in het veld Naam.
33. Klik tot slot op **OK**.
34. Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.
35. Klik op **Element toevoegen**.
36. Typ **Name** in het veld Naam.
37. Klik tot slot op **OK**.
38. Klik op **Element toevoegen**.
39. Typ **Bank** in het veld **Naam**.
40. Klik tot slot op **OK**.
41. Selecteer **Xml\Message\Payments\Item\Vendor\Bank** in de structuur.
42. Klik op **Element toevoegen**.
43. Typ **RoutingNumber** in het veld **Naam**.
44. Klik tot slot op **OK**.
45. Klik op **Element toevoegen**.
46. Typ **AccountNumber** in het veld **Naam**.
47. Klik tot slot op **OK**.
48. Selecteer **Xml\Message\Payments\Item\Vendor** in de structuur.
49. Klik op **Kopiëren**.
50. Selecteer **Xml\Message\Payments\Item** in de structuur.
51. Klik op **Plakken**.
52. Typ **Payer** in het veld **Naam**.
53. Selecteer **Xml\Message\Payments\Item** in de structuur.
54. Klik op **Element toevoegen**.
55. Typ **Currency** in het veld **Naam**.
56. Klik tot slot op **OK**.
57. Klik op **Element toevoegen**.
58. Typ **Description** in het veld **Naam**.
59. Klik tot slot op **OK**.
60. Klik op **Element toevoegen**.
61. Typ **TransDate** in het veld Naam.
62. Klik tot slot op **OK**.
63. Klik op **Element toevoegen**.
64. Typ **Amount** in het veld Naam.
65. Klik tot slot op **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Indelingsonderdelen voorbereiden voor toewijzing aan gegevensmodelelementen
1. Selecteer **Xml\Message\ProcessingDate** in de structuur.
2. Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
3. Selecteer **Text\DateTime** in de structuur.
4. Typ **jjjj-MM-dd** in het veld **Notatie**.
5. Klik tot slot op **OK**.
6. Selecteer **Xml\Message\Payments\Item\TransDate** in de structuur.
7. Klik op **Datum/tijd toevoegen**.
8. Typ **jjjj-MM-dd** in het veld **Notatie**.
9. Selecteer in het veld van het type **Datum/tijd** de waarde **Datum**.
10. Klik tot slot op **OK**.
11. Selecteer **Xml\Message\MessageId** in de structuur.
12. Klik op **Toevoegen** om het dialoogvenster voor beëindigen te openen.
13. Selecteer **Text\String** in de structuur.
14. Klik tot slot op **OK**.
15. Selecteer **Xml\Message\Payments\Item\Vendor\Name** in de structuur.
16. Klik op **Tekenreeks toevoegen**.
17. Klik tot slot op **OK**.
18. Selecteer **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** in de structuur.
19. Klik op **Tekenreeks toevoegen**.
20. Klik tot slot op **OK**.
21. Selecteer **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** in de structuur.
22. Klik op **Tekenreeks toevoegen**.
23. Klik tot slot op **OK**.
24. Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Name**.
25. Klik op **Tekenreeks toevoegen**.
26. Klik tot slot op **OK**.
27. Selecteer in de structuur **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.
28. Klik op **Tekenreeks toevoegen**.
29. Klik tot slot op **OK**.
30. Selecteer **Xml\Message\Payments\Item\Payer\Bank\AccountNumber** in de structuur.
31. Klik op **Tekenreeks toevoegen**.
32. Klik tot slot op **OK**.
33. Selecteer **Xml\Message\Payments\Item\Currency** in de structuur.
34. Klik op **Tekenreeks toevoegen**.
35. Klik tot slot op **OK**.
36. Selecteer **Xml\Message\Payments\Item\Description** in de structuur.
37. Klik op **Tekenreeks toevoegen**.
38. Klik tot slot op **OK**.
39. Selecteer **Xml\Message\Payments\Item\Amount** in de structuur.
40. Klik op **Tekenreeks toevoegen**.
41. Klik tot slot op **OK**.
42. Klik op **Opslaan**.
43. Sluit de pagina.


