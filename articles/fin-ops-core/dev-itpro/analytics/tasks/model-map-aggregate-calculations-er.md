---
title: Modeltoewijzingsconfiguraties gebruiken voor samengevoegde berekeningen op databaseniveau gebruiken
description: In dit onderwerp wordt beschreven hoe u een nieuwe ER-modeltoewijzingsconfiguratie (elektronische rapportage) kunt ontwerpen en de ingebouwde ER-functies voor efficiënte statistische berekeningen kunt toepassen.
author: NickSelin
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f48596c30127976d915811ffa8412dcc9b2593
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745370"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Modeltoewijzingsconfiguraties gebruiken voor samengevoegde berekeningen op databaseniveau gebruiken

[!include [banner](../../includes/banner.md)]

Deze procedure bevat informatie voor het ontwerpen van een nieuwe ER-modeltoewijzingsconfiguratie (elektronische aangifte) en past de ingebouwde ER-functies toe voor efficiënte statistische berekeningen. In deze procedure maakt u een configuratie voor het voorbeeldbedrijf Litware, Inc. 

Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar. Deze stappen kunnen worden voltooid met elke dataset.

 Voordat u deze stappen uitvoert, voert u de stappen uit in de procedure ER verbetert de efficiency van aggregatieberekeningen door ze uit te voeren op databaseniveau (Deel 1: Configuraties voorbereiden).

1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
2. Vouw in de structuur 'Intrastat-model' uit.
3. Selecteer in de structuur 'Intrastat-model\Intrastat-voorbeeldtoewijzing'.
4. Klik op Ontwerper.
5. Klik op Ontwerper.
6. Selecteer in de structuur 'Dynamics 365 for Operations\Tabelrecords'.
7. Klik op Basis toevoegen.
    * Voeg een nieuwe gegevensbron toe die de records weergeeft die u wilt groeperen.  
8. Typ "Transacties" in het veld Naam.
    * Transacties  
9. Typ 'Intrastat' in het veld Tabel.
    * Intrastat  
10. Klik op OK.
11. Selecteer in de structuur Functies\Groeperen op.
    * Dit gegevensbrontype wordt gebruikt om in runtime een nieuwe gegevensbron te introduceren voor het groeperen van records en het berekenen van de vereiste aggregaties.  
12. Klik op Basis toevoegen.
13. Typ 'TransactionsGroups' in het veld Naam.
    * Transactiegroepen  
14. Klik op Groeperen op bewerken
15. Selecteer "Transactions" in de structuur.
    * Selecteer de toegevoegde gegevensbron van het type Recordlijst die de records aangeeft die u wilt groeperen.  
16. Klik op Veld toevoegen aan.
17. Klik op Wat groeperen.
18. Vouw "Transactions" uit in de structuur.
19. Selecteer in de structuur 'Transacties\Richting'.
20. Klik op Veld toevoegen aan.
21. Klik op Gegroepeerde velden.
    * Selecteer het veld om het groeperingsniveau op te geven. Op basis van deze selectie stuurt de gegevensbron tijdens runtime zoveel transactiegroepen terug als er richtingcodes zijn waaraan wordt voldaan in de Intrastat-tabel.  
22. Selecteer in de structuur 'Transacties\Factuurbedrag(AmountMST)'.
    * Selecteer het veld om de bron voor de aggregatieberekening op te geven.  
23. Klik op Veld toevoegen aan.
24. Klik op Aggregatievelden.
25. Markeer in de lijst de geselecteerde rij.
26. Selecteer 'Totaal' in het veld Methode.
    * Selecteer het aggregatietype.  
27. Typ 'SumOfAmountMST' in het veld Naam
    * Geef de naam op van deze aggregatie in de geconfigureerde gegevensbron.  
28. Klik op Opslaan.
    * Houd er rekening mee dat het veld Uitvoering in aangeeft dat deze groepering in runtime wordt uitgevoerd in de SQL-database.  
29. Sluit de pagina.
30. Klik op OK.
31. Vouw in de structuur 'Totalen' uit.
32. Vouw in de structuur 'TransactionsGroups' uit.
33. Vouw in de structuur 'TransactionsGroups\aggregated' uit.
34. Selecteer in de structuur 'TransactionsGroups\aggregated\SumOfAmountMST'.
35. Selecteer in de structuur 'Totalen\Totale factuurwaarde(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.
36. Klik op Binden.
    * Op basis van deze instelling berekent deze gegevensbron de som van de waarden van het veld AmountMST voor elke transactiegroep. Deze aggregatieberekening is beschikbaar als het item TransactionsGroups.aggregated.TotalAmount.  
37. Vouw in de structuur 'TransactionsGroups' uit.
38. Selecteer in de structuur 'TransactionsGroups'.
39. Klik op Bewerken.
40. Klik op Groeperen op bewerken
41. Vouw "Transactions" uit in de structuur.
42. Selecteer in de structuur 'Transacties\Factuurbedrag(AmountMST)'.
43. Klik op Veld toevoegen aan.
44. Klik op Aggregatievelden.
45. Markeer in de lijst de geselecteerde rij.
46. Selecteer 'Max' in het veld Methode.
47. Typ in het veld Naam 'MaxOfAmountMST'.
48. Klik op Opslaan.
    * De uitvoering van de GROUPBY-gegevensbronnen kan dan met een aantal beperkingen worden vertaald naar het niveau van de SQL-database. Vertaling is mogelijk voor gegevensbronnen van het type Recordlijst of voor gegevensbronnen die als een expressie worden weergegeven met de FILTER-functie. Dit kan ook worden uitgevoerd wanneer slechts één aggregatie wordt geconfigureerd voor één veld met groeperingsrecords.  
    * Houd er rekening mee dat hoewel er meer dan één aggregatie is geconfigureerd voor het veld AmountMST, het veld Uitvoering in nog steeds aangeeft dat deze groepering in runtime wordt uitgevoerd in de SQL-database. Dit komt doordat slechts één aggregatie is gekoppeld aan het gegevensmodelitem en dat deze wordt gebruikt om in runtime gegevens op te halen uit deze gegevensbron.  
49. Sluit de pagina.
50. Klik op OK.
51. Vouw in de structuur 'TransactionsGroups' uit.
52. Vouw in de structuur 'TransactionsGroups\aggregated' uit.
53. Selecteer in de structuur 'TransactionsGroups\aggregated\MaxOfAmountMST'.
54. Selecteer in de structuur 'Totalen\Totale statistische waarde(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.
55. Klik op Binden.
56. Vouw in de structuur 'TransactionsGroups' uit.
57. Selecteer in de structuur 'TransactionsGroups'.
58. Klik op Bewerken.
59. Klik op Groeperen op bewerken
    * Houd er rekening mee dat het veld Uitvoering in aangeeft dat deze groepering in runtime in het geheugen wordt uitgevoerd omdat beide aggregaties van hetzelfde veld zijn gekoppeld aan de gegevensmodelitems.   
60. Selecteer of deselecteer alle rijen in de lijst.
61. Klik op Verwijderen.
62. Klik op Ja.
63. Klik op Verwijderen.
64. Klik op Ja.
65. Klik op Veld toevoegen aan.
66. Klik op Wat groeperen.
67. Vouw in de structuur 'Basisproductrecord(Intrastat)' uit.
68. Klik op Opslaan.
    * Het veld Uitvoering in geeft aan dat deze groepering in runtime in het geheugen wordt uitgevoerd, hoewel er geen aggregaties zijn gedefinieerd en de geselecteerde gegevensbron van het type Tabelrecords naar dezelfde Intrastat-tabel verwijst. Dit komt doordat de gegevensbron een aantal berekende velden bevat die nog niet kunnen worden omgezet naar het niveau van de SQL-database.  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]