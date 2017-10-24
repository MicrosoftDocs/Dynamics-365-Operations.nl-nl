--- 
title: Model en toewijzing wijzigen voor het genereren van documenten met een update van toepassingsgegevens voor elektronische aangifte (ER)
description: 'Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure ''ER Documenten genereren met update van toepassingsgegevens (deel 2: Documenten genereren)'' voltooien.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a29e273e5ef377826c0002a9a0a956defef6aa77
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Model en toewijzing wijzigen voor het genereren van documenten met een update van toepassingsgegevens voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 2: documenten genereren)' voltooien. 

De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken. In deze procedure wijzigt u de ER-configuraties om ze te gaan gebruiken om elektronische documenten te genereren en om toepassingsgegevens bij te werken. Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de DEMF-gegevensset.


## <a name="modify-data-model"></a>Gegevensmodel wijzigen
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Selecteer in de structuur 'Intrastat (model)'.
    * U gaat uitbreiden hoe u het gegevensmodel gebruikt. U gebruikt het niet alleen als gegevensbron om het Intrastat-rapport te genereren, maar het gegevensmodel wordt gebruikt voor het verzamelen van gegevens over het Intrastat-rapportageproces. De details worden vervolgens gebruikt voor het bijwerken van toepassingsgegevens.   
3. Klik op Ontwerper.
4. Klik op Nieuw om het verwijderdialoogvenster te openen.
5. Typ in het veld "Nieuw knooppunt als een" de tekst "Modelbasis".
6. Typ 'Voor update van toepassingsgegevens' in het veld Naam.
    * Voor bijwerken van toepassingsgegevens  
7. Klik op Toevoegen.
8. Selecteer in de structuur 'Voor update van toepassingsgegevens'.
    * Dit nieuwe basisitem wordt toegevoegd om de gegevensstroom op te geven voor het verplaatsen van gegevens door het Intrastat-rapport (gebruikt als gegevensbron) naar de toepassingstabellen (de updatebestemming). Houd er rekening mee dat verschillende basisitems moeten worden gebruikt voor het ophalen van gegevens die worden geboekt naar het uitgaande document en voor het ophalen van gegevens uit het document dat wordt gebruikt om toepassingsgegevens bij te werken.   
9. Klik op Nieuw om het verwijderdialoogvenster te openen.
10. Typ 'Archiefkoptekst' in het veld Naam.
    * Archiefkoptekst  
11. Selecteer "Record list" in het veld Artikeltype.
12. Klik op Toevoegen.
    * Omdat u een record maakt voor elk Intrastat-rapport dat wordt gegenereerd, moet u er een nieuw item voor maken.  
13. Klik op Nieuw om het verwijderdialoogvenster te openen.
14. Typ Bestandsnaam in het veld Naam.
    * Bestandsnaam  
15. Selecteer "String" in het veld Artikeltype.
16. Klik op Toevoegen.
17. Klik op Nieuw om het verwijderdialoogvenster te openen.
18. Typ 'Aantal regels' in het naamveld.
    * Aantal regels  
19. Selecteer 'Geheel getal' in het veld Artikeltype.
20. Klik op Toevoegen.
    * Voeg dit item toe om het nummer voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.  
21. Klik op Nieuw om het verwijderdialoogvenster te openen.
22. Typ 'Archiefregels' in het veld Naam.
    * Archiefregels  
23. Selecteer "Record list" in het veld Artikeltype.
24. Klik op Toevoegen.
    * Voeg dit item toe om de lijst voor te stellen van Intrastat-transacties die worden gerapporteerd tijdens het huidige rapportageproces.  
25. Klik op Nieuw om het verwijderdialoogvenster te openen.
26. Typ "Amount" in het veld Naam.
    * Bedrag  
27. Selecteer "Real" in het veld Artikeltype.
28. Klik op Toevoegen.
29. Klik op Nieuw om het verwijderdialoogvenster te openen.
30. Typ 'Basisproductrecord-id' in het veld Naam.
    * Basisproductrecord-id  
31. Selecteer 'Int64' in het veld Artikeltype.
32. Klik op Toevoegen.
33. Klik op Nieuw om het verwijderdialoogvenster te openen.
34. Typ 'Artikelnummer' in het veld Naam.
    * artikelnummer  
35. Selecteer "String" in het veld Artikeltype.
36. Klik op Toevoegen.
37. Klik op Opslaan.
38. Sluit de pagina.

## <a name="modify-model-mapping"></a>Modeltoewijzing wijzigen
1. Vouw in de structuur 'Intrastat (model)' uit.
2. Selecteer in de structuur 'Intrastat (model)\Intrastat (toewijzing)'.
    * Wijzig de bestaande modeltoewijzing om deze te gaan gebruiken voor de update van toepassingsgegevens en om Intrastat-rapportagedetails te archiveren.  
3. Klik op Ontwerper.
4. Klik op Nieuw.
5. Typ 'Archief bijwerken' in het veld Naam.
    * Archief bijwerken  
6. Selecteer 'Tot bestemming' in het veld Richting.
7. Klik op Opslaan.
    * Deze nieuwe toewijzing geeft de gegevensstroom op voor het verplaatsen van gegevens (Intrastat-rapportagedetails) van het gegevensmodel naar de toepassingstabellen (de updatebestemming). Houd er rekening mee dat verschillende basisitems moeten worden gebruikt om gegevens op te halen uit de toepassing voor het rapportageproces en gebruik vervolgens de gegevens uit het gegevensmodel voor de update van de toepassingsgegevens.   
8. Klik op Ontwerper.
9. Selecteer in de structuur 'Gegevensmodel\Gegevensmodel'.
    * Voeg de vereiste gegevensbron toe. Dit is het gegevensmodel dat gegevens bevat van de gerapporteerde Intrastat-transacties die moeten worden gearchiveerd.  
10. Klik op Basis toevoegen.
11. Typ 'model' in het veld Naam.
    * model  
12. Typ of selecteer in het veld Definitie de waarde voor 'Voor gegevensupdate van toepassing'.
    * Voor bijwerken van toepassingsgegevens  
13. Klik op OK.
14. Vouw in de structuur "model" uit.
15. Selecteer "Functions\Calculated field" in de structuur.
16. Selecteer 'model\Archiefkoptekst' in de structuur.
17. Klik op Toevoegen.
    * Omdat u gerapporteerde Intrastat-transacties gaat opsommen voor archivering, moet de juiste gegevensbron worden toegevoegd.  
18. Typ 'Vaste regels' in het naamveld.
    * Vaste regels  
19. Klik op Formule bewerken.
20. Selecteer in de structuur 'Lijst\ENUMERATE'.
21. Klik op Functie toevoegen.
22. Vouw in de structuur "model" uit.
23. Vouw in de structuur 'model\Archiefkoptekst' uit.
24. Selecteer 'model\Archiefkoptekst\Archiefregels' in de structuur.
25. Klik op Gegevensbron toevoegen.
26. Voer in het formuleveld 'ENUMERATE (model.'Archiefkoptekst'.'Archiefregels')' in.
    * ENUMERATE(model. 'Archiefkoptekst'.'Archiefregels')  
27. Klik op Opslaan.
28. Sluit de pagina.
29. Klik op OK.
30. Klik op Bestemming toevoegen.
    * Voeg toepassingstabellen toe als vereiste bestemmingen die updates vereisen om details te archiveren van gerapporteerde Intrastat-transacties.  
31. Typ in het veld Naam 'Archief'.
    * Archiveren  
32. Typ in het veld Tabel 'IntrastatArchiveGeneral'.
    * IntrastatArchiveGeneral  
    * Houd de recordactie 'Invoegen', zodat u records kunt toevoegen tijdens de detailarchivering van elk Intrastat-rapportageproces.  
33. Selecteer Ja in het veld Infolog registreren.
    * Selecteer Ja om informatie te krijgen over problemen met de update van toepassingsgegevens.  
34. Selecteer Ja in het veld Validatie van actie registreren overslaan.
    * Selecteer Ja als u validatiefouten wilt onderdrukken over het lege veld 'Intrastat-archief-id'. Dit wordt gedaan nadat records zijn toegevoegd, op basis van de numerieke reeksvolgorde-instellingen die zijn geconfigureerd voor deze tabel in het parameterformulier voor buitenlandse handel.  
35. Klik op OK.
    * Bind elementen van de toegevoegde gegevensbron (het gefilterde model op basis van het geselecteerde hoofditem) met elementen uit de toegevoegde bestemming.  
36. Vouw in de structuur 'Archief' uit.
37. Vouw in de structuur 'Archief\<Relaties' uit.
38. Vouw in de structuur 'Archief\<Relaties\IntrastatArchiveDetail' uit.
39. Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Bedrag(AmountMST)'.
40. Vouw in de structuur 'model\Archiefkoptekst\Vaste regels' uit.
41. Vouw in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde' uit.
42. Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Bedrag'.
43. Klik op Binden.
44. Selecteer in de structuur 'Archief\<Relaties\Intrastat\ArchiveDetail\Basisproduct(IntrastatCommodity)'.
45. Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Basisproductrecord-id'.
46. Klik op Binden.
47. Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Artikelnummer(ItemId)'.
48. Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Waarde\Artikelnummer'.
49. Klik op Binden.
50. Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail\Regelnummer(Regelnummer)'.
51. Selecteer in de structuur 'model\Archiefkoptekst\Vaste regels\Getal'.
52. Klik op Binden.
53. Selecteer in de structuur 'Archief\<Relaties\IntrastatArchiveDetail'.
54. Selecteer 'model\Archiefkoptekst\Vaste regels' in de structuur.
55. Klik op Binden.
56. Selecteer in de structuur 'Archief\Bestandsnaam(Bestandsnaam)'.
57. Selecteer 'model\Archiefkoptekst\Bestandsnaam' in de structuur.
58. Klik op Binden.
59. Selecteer in de structuur 'Archief\Aantal regels(AantalRegels)'.
60. Selecteer 'model\Archiefkoptekst\Aantal regels' in de structuur.
61. Klik op Binden.
62. Selecteer in de structuur 'Archief'.
63. Selecteer 'model\Archiefkoptekst' in de structuur.
64. Klik op Binden.
65. Klik op Opslaan.
66. Sluit de pagina.
67. Sluit de pagina.


