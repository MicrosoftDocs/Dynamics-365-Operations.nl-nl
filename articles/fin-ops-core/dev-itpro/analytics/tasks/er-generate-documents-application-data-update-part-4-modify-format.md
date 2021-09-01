---
title: Indelingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten
description: Dit onderwerp laat zien hoe u rapportageconfiguraties ontwerpt voor het genereren van elektronische documenten en bijwerken van toepassingsgevens.
author: NickSelin
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 312a49fc524cc7359d2c1815597214656df11c018034da384d30bfb9d9efee4b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752406"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Indelingen wijzigen voor het genereren van documenten die toepassingsgegevens bevatten

[!include [banner](../../includes/banner.md)]

Als u de stappen in deze procedure wilt voltooien, moet u eerst de procedure 'ER Documenten genereren met update van toepassingsgegevens (deel 3: model en toewijzing wijzigen)' voltooien.

De stappen in deze procedure leggen uit hoe u ER-configuraties ontwerpt om een elektronisch document te genereren en toepassingsgegevens bij te werken. In deze procedure wijzigt u de ER-configuraties om ze niet alleen te gebruiken om elektronische documenten te genereren, maar ook om toepassingsgegevens bij te werken. Deze procedure is gemaakt voor gebruikers met de toegewezen rol van systeembeheerder of elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met de DEMF-gegevensset.


## <a name="modify-format-to-collect-details-of-reporting"></a>Indeling wijzigen om details over rapportage te verzamelen
1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Intrastat (model)' uit.
3. Selecteer in de structuur 'Intrastat (model)\Intrastat (indeling)'.
4. Klik op Ontwerper.
5. Vouw in de structuur 'Bestand' uit.
6. Vouw in de structuur 'Bestand\Declaratie' uit.
7. Selecteer in de structuur 'Bestand\Declaratie\Gegevens'.
8. Selecteer in het veld Multipliciteit 'Éen veel'.
    * Dit indelingselement configureren om details te archiveren van het Intrastat-rapportageproces. Dit object vertegenwoordigt de koptekstrecord van het archief.  
9. Vouw in de structuur 'Bestand\Declaratie\Gegevens' uit.
10. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item'.
11. Selecteer in het veld Multipliciteit 'Nul veel'.
    * Dit indelingselement configureren om details te archiveren van het Intrastat-rapportageproces. Dit object vertegenwoordigt de lijst met gearchiveerde regels.  
12. Vouw in de structuur 'Bestand\Declaratie\Gegevens\Item' uit.
13. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim1'.
14. Selecteer Ja in het veld Uitgesloten.
    * U archiveert deze gegevens niet, dus u kunt dit indelingselement uitsluiten van de gegevensbron van Intrastat-rapportagedetails.  
15. Vouw in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim1' uit.
16. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim1\eigenschap'.
17. Selecteer Ja in het veld Uitgesloten.
18. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim1\datum'.
19. Selecteer Ja in het veld Uitgesloten.
20. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim2'.
21. Selecteer Ja in het veld Uitgesloten.
22. Vouw in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim2' uit.
23. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim2\eigenschap'.
24. Selecteer Ja in het veld Uitgesloten.
25. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim2\code'.
26. Selecteer Ja in het veld Uitgesloten.
27. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim3'.
    * Meerdere elementen kunnen dezelfde naam hebben. Bijvoorbeeld Dim. U kunt deze niet expliciet herkennen wanneer u deze indeling als een gegevensbron gebruikt voor het archiveren van Intrastat-rapportagedetails, dus u moet de alternatieve namen definiëren voor deze indelingselementen.   
28. Typ "Amount" in het veld Naam.
    * Bedrag  
29. Selecteer in het veld Multipliciteit 'Precies één'.
30. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item\Dim4'.
31. Typ "Item" in het veld Naam.
    * Artikel  
32. Selecteer in het veld Multipliciteit 'Precies één'.
    * Naast de ontwerpindelingselementen moeten de volgende Intrastat-rapportagedetails worden gearchiveerd: unieke record-id van elk gerapporteerd basisproduct en de naam van het gegenereerde bestand. Omdat deze gegevens niet worden ingevuld in het Intrastat-rapport, moet u de indeling die is gerelateerd aan deze detailelementen als gegevensbronitems toevoegen.  
33. Selecteer in de structuur 'Bestand\Declaratie\Gegevens'.
34. Klik op Toevoegen om het dialoogvenster te openen.
35. Selecteer 'Gegevensbron\Item' in de structuur.
36. Typ Bestandsnaam in het veld Naam.
    * Bestandsnaam  
37. Selecteer "String" in het veld Gegevenstype.
38. Klik op OK.
39. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item'.
40. Klik op Item toevoegen.
41. Typ 'Basisproductrecord-id' in het veld Naam.
    * Basisproductrecord-id  
42. Selecteer 'Int64' in het veld Gegevenstype.
43. Klik op OK.
44. Klik op het tabblad Toewijzing.
45. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Bestandsnaam'.
46. Klik op Binden.
47. Vouw in de structuur "model" uit.
48. Vouw in de structuur 'model\Transacties' uit.
49. Selecteer in de structuur 'Bestand\Declaratie\Gegevens\Item = model.Transacties\Basisproductrecord-id'.
50. Selecteer in de structuur 'model\Transacties\Basisproductrecord-id'.
51. Klik op Binden.
52. Klik op Opslaan.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Indeling wijzigen om details over rapportage te onthouden

1. Klik op 'Indeling aan model toewijzen'.
2. Klik op Nieuw.
3. Typ of selecteer in het veld Definitie het basisitem 'Voor update van toepassingsgegevens'.
    * Voor bijwerken van toepassingsgegevens.
4. Typ 'Toewijzing aan updategegevens' in het veld Naam.
    * Toewijzing aan updategegevens  
5. Klik op Opslaan.
    * Deze toewijzing definieert hoe de details van het Intrastat-rapport worden verzameld in het gegevensmodel, waarvan de structuur wordt opgegeven door het geselecteerde basisitem 'voor update van toepassingsgegevens'. Deze gegevens, de modeltoewijzing met hetzelfde basisitem 'Voor update van toepassingsgegevens' en de richting 'Naar bestemming' wordt gebruikt voor de update van de toepassingsgegevens. De update van de toepassingsgegevens begint meteen nadat het uitgaande Intrastat-rapport is gegenereerd. De update van de toepassingsgegevens kan worden overgeslagen tijdens runtime, maar het gegevensmodel moet leeg zijn (een lege recordlijst moet bevatten).
6. Klik op Ontwerper.
    * De indeling van het uitgaande Intrastat-rapport wordt standaard toegevoegd als gegevensbron voor deze modeltoewijzing.  
    * Bind elementen van het opgegeven rapport (gepresenteerd als gegevensbron) aan elementen van het gegevensmodel, dat wordt gefilterd op basis van het basisitem van het geselecteerde model.  
7. Vouw in de structuur 'Archiefkoptekst' uit.
8. Vouw in de structuur 'Archiefkoptekst\Archiefregels' uit.
9. Vouw in de structuur 'indeling' uit.
10. Vouw in de structuur ' indeling\Declaratie: XML-element(Declaratie)' uit.
11. Vouw in de structuur 'indeling\Declaratie: XML-element(Declaratie)\Gegevens: XML-element 1..* (Gegevens)' uit.
12. Vouw in de structuur 'indeling\Declaratie: XML-element(Declaratie)\Gegevens: XML-element 1..* (Gegevens)\Item: XML-element 0..* (Item)' uit.
13. Vouw in de structuur 'indeling\Declaratie: XML-element(Declaratie)\Gegevens: XML-element 1..* (Gegevens)\Item: XML-element 0..* (Item)\Dim3: XML-element 1..1 (Bedrag)' uit.
14. Vouw in de structuur 'indeling\Declaratie: XML-element(Declaratie)\Gegevens: XML-element 1..* (Gegevens)\Item: XML-element 0..* (Item)\Dim4: XML-element 1..1 (Item)' uit.
15. Selecteer 'Archiefkoptekst\Aantal regels' in de structuur.
16. Klik op Bewerken.
17. Selecteer in de structuur 'Lijst\COUNT'.
18. Klik op Functie toevoegen.
19. Vouw in de structuur 'indeling' uit.
20. Vouw in de structuur ' indeling\Declaratie: XML-element(Declaratie)' uit.
21. Vouw in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)` uit.
22. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
23. Klik op Gegevensbron toevoegen.
24. Voer in het formuleveld 'COUNT(indeling.Declaratie.Gegevens.Item)'.
    * COUNT(indeling.Declaratie.Gegevens.Item)  
25. Klik op Opslaan.
26. Sluit de pagina.
27. Selecteer 'Archiefkoptekst\Bestandsnaam' in de structuur.
28. Selecteer in de structuur 'indeling\Declaratie: XML-element(Declaratie)\Gegevens: XML-element 1..* (Gegevens)\Bestandsnaam: itemtekenreeks(Bestandsnaam)'.
29. Klik op Binden.
30. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)`.
31. Selecteer 'Archiefkoptekst\Archiefregels\Itemnummer' in de structuur.
32. Klik op Binden.
33. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)`.
34. Selecteer in de structuur 'Archiefkoptekst\Archiefregels\Bedrag'.
35. Klik op Binden.
36. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)`.
37. Selecteer 'Archiefkoptekst\Archiefregels\Basisproductrecord-id' in de structuur.
38. Klik op Binden.
39. Selecteer 'Archiefkoptekst\Archiefregels' in de structuur.
40. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
41. Klik op Binden.
42. Selecteer in de structuur 'Archiefkoptekst'.
43. Selecteer in de structuur `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
44. Klik op Binden.
45. Klik op Opslaan.
46. Sluit de pagina.
47. Sluit de pagina.
48. Sluit de pagina.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]