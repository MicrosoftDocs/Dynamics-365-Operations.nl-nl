---
title: 'ER: vereiste configuraties maken voor het importeren van gegevens uit een extern bestand'
description: Dit onderwerp beschrijft het ontwerpen van configuraties elektronische rapportage om gegevens te importeren in de Microsoft Dynamics 365 Finance-app vanuit een extern bestand.
author: NickSelin
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERSolutionCreateDropDialog, EROperationDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula, Tax1099Summary, VendSettlementTax1099
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7eaa35baae8e030d8a8b7ce903554c4876c874b48cfd72d6ac278cf4c0e8a6e8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720851"
---
# <a name="er-create-required-configurations-to-import-data-from-an-external-file"></a>ER: vereiste configuraties maken voor het importeren van gegevens uit een extern bestand

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder of ER-ontwikkelaar nieuwe ER-configuraties kan maken waarmee gegevens vanuit een extern bestand in de toepassing kunnen worden geïmporteerd. In dit voorbeeld maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Voordat u deze stappen uitvoert, moet u eerst de stappen uitvoeren in de Taakbegeleiding "ER Een configuratieprovider maken en deze als actief markeren". Deze stappen kunnen worden voltooid met de USMF-gegevensset. U moet ook de volgende bestanden downloaden en lokaal opslaan: 

| Omschrijving inhoud                       | Bestandsnaam                                     |
|-------------------------------------------|-----------------------------------------------|
| Configuratie van model voor ER-gegevens - 1099 | [1099model,xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)                  |
| ER-indelingsconfiguratie - 1099    | [1099format.xml](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)                  |
| Voorbeeld van het binnenkomende document in XML-indeling                          | [1099entries.xml](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)        |
| Voorbeeld van de werkmap voor beheer van gegevens van inkomend document                          | [1099entries.xlsx](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx) |

ER biedt zakelijke gebruikers de mogelijkheid om het proces te configureren voor de import van externe gegevensbestanden in tabellen in de indeling .XML of .TXT. Allereerst moet u een abstract gegevensmodel en een configuratie voor een ER-gegevensmodel opzetten, om de gegevens te vertegenwoordigen die u wilt importeren. Vervolgens moet u de structuur definiëren van het bestand dat u wilt importeren en de methode die u gebruikt om de gegevens van het bestand over te zetten naar het abstracte gegevensmodel. De ER-indelingsconfiguratie die de toewijzing naar het door u ontworpen gegevensmodel bevat, moet voor dat abstracte gegevensmodel worden gemaakt. Vervolgens moet u de gegevensmodelconfiguratie uitbreiden met een toewijzing die beschrijft hoe de geïmporteerde gegevens permanent worden gemaakt als gegevens in het abstracte gegevensmodel en hoe ze worden gebruikt voor het bijwerken van tabellen.  Aan de gegevensmodelconfiguratie van ER moet een nieuwe modeltoewijzing worden toegevoegd, die de binding van het gegevensmodel aan de bestemmingen van de toepassing beschrijft.  

In het volgende scenario worden de mogelijkheden van ER voor gegevensimport getoond. Dit omvat leveranciertransacties die extern worden bijgehouden en vervolgens geïmporteerd, zodat ze later worden gerapporteerd in de Vereffening van leverancier voor 1099-aangiften.   

## <a name="add-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie toevoegen
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.

    Controleer of de configuratieprovider voor het voorbeeldbedrijf ‘Litware, inc.‘ beschikbaar is en als actief gemarkeerd. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.   

2. Klik op Rapportconfiguraties.

    U hoeft niet een nieuw model te maken ter ondersteuning van de gegevensimport; u laadt het bestand 1099model.xml, dat u eerder hebt gedownload. Dit bestand bevat het aangepaste gegevensmodel voor leverancierstransacties. Dit gegevensmodel is toegewezen aan de gegevensonderdelen die onderdeel zijn van de AOT-gegevensentiteit.   

3. Klik op Uitwisselen.
4. Klik op Laden uit XML-bestand.

    Klik op Bladeren en navigeer naar het bestand 1099model.xml, dat u eerder hebt gedownload.  

5. Klik op OK.
6. Selecteer in de structuur '1099 Payments model'.

## <a name="review-data-model-settings"></a>Instellingen van het gegevensmodel controleren
1. Klik op Ontwerper.

    Dit model is ontworpen om leverancierstransacties weer te geven vanuit het bedrijfsoogpunt en is onafhankelijk van de implementatie.   

2. Vouw in de structuur '1099-MISC' uit.
3. Selecteer in de structuur '1099-MISC\Transactions'.
4. Vouw in de structuur '1099-MISC\Transactions' uit.

    Het element Transacties van dit model vertegenwoordigt de afzonderlijke transacties. De onderliggende elementen worden gebruikt om voor elke transactie de vereiste gegevens op te geven, zoals de leveranciersrekening en de transactiedatum.   

5. Sluit de pagina.

## <a name="add-a-new-er-format-configuration-that-supports-data-import"></a>Een nieuwe ER-indelingsconfiguratie toevoegen die het importeren van gegevens ondersteunt
In de stappen in deze subtaak ziet u hoe u een nieuwe indelingsconfiguratie kunt maken voor het beheer van de gegevensimport vanuit externe bestanden.   
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Voer in het veld Nieuw de volgende tekst in: 'Indeling gebaseerd op gegevensmodel 1099 Payments model'.
3. Selecteer in het veld Ondersteunt gegevensimport de waarde Ja.
4. Druk op ESC om deze pagina te sluiten.

    U hoeft niet een nieuwe indeling te maken ter ondersteuning van de gegevensimport; u laadt het bestand 1099format.xml, dat u eerder hebt gedownload. Dit bestand bevat de gedefinieerde structuur van het bestand dat u wilt importeren en de toewijzing van de structuur naar het aangepaste gegevensmodel van de leverancierstransacties.   
5. Klik op Uitwisselen.
6. Klik op Laden uit XML-bestand.
    Klik op Bladeren en navigeer naar het bestand 1099format.xml, dat u eerder hebt gedownload.  
7. Klik op OK.
8. Vouw in de structuur '1099 Payments model' uit.
9. Selecteer in de structuur '1099 Payments model\Format for importing vendors' transactions'.

## <a name="review-format-settings"></a>Indelingsinstellingen controleren
1. Klik op Ontwerper.
2. Schakel de optie 'Details weergeven' in.
3. Klik op Uitvouwen/samenvouwen.
4. Klik op Uitvouwen/samenvouwen.

    De ontworpen opmaak vertegenwoordigt de verwachte structuur van het externe bestand. Dit bestand moet de XML-indeling hebben en het hoofdelement settlement. Elke leverancierstransactie wordt vertegenwoordigd door het element transaction, dat is gedefinieerd met een nul-veel multipliciteit. Dit betekent dat het aantal transacties in het inkomende bestand tussen nul en meerdere kan liggen. Geneste elementen van het element 'transaction' vertegenwoordigen de kenmerken van een enkele transactie. Houd er rekening mee dat alle kenmerken, met uitzondering van 'land', zijn gemarkeerd als verplicht, wat betekent dat deze verplicht in het importbestand moeten bestaan.   

## <a name="review-the-settings-of-the-format-mapping-to-the-data-model"></a>De instellingen van de indelingstoewijzing naar het gegevensmodel controleren
1. Klik op 'Indeling aan model toewijzen'.

    De toewijzing 'For importing vendors' transactions' bevat de regels voor gegevensoverdracht van het inkomende XML-bestand naar het geselecteerde deel van het aangepaste gegevensmodel, dat wordt gedefinieerd door de definitie 1099-MISC te selecteren.  

2. Klik op Ontwerper.
3. Schakel de optie 'Details weergeven' in.
4. Vouw in de structuur 'format: Record' uit.
5. Selecteer in de structuur 'format: Record'.

    Merk op dat de ontworpen indeling hier wordt weergegeven als een onderdeel van de gegevensbron.  

6. Vouw in de structuur `format: Record\*settlement: XML Element 1..1 (settlement): Record` uit.
7. Vouw in de structuur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list` uit.
8. Vouw in de structuur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record` uit.
9. Vouw in de structuur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\country: XML Element 0..1 (country): Record` uit.
10. Selecteer in de structuur `format: Record\*settlement: XML Element 1..1 (settlement): Record\transaction: XML Element 0..* (transaction): Record list\*vendor: XML Element 1..1 (vendor): Record`.

    Merk op dat de presentatie van verplichte en optionele indelingselementen anders is dan in het vooraf onderdeel van de gegevensbron ‘format’.  
11. Vouw in de structuur 'Transactions: Record list= format.settlement.'$enumerated'' uit.

    Houd er rekening mee dat de elementen van de indeling waarmee de structuur van het geïmporteerde bestand wordt gedefinieerd, zijn gebonden aan de elementen van het aangepaste gegevensmodel. Op basis van deze bindingen wordt de inhoud van het geïmporteerde XML-bestand tijdens de uitvoering opgeslagen in het bestaande gegevensmodel. Let op de binding van het element land. Voor elk transactie-element in het inkomende bestand waarbij dit element ontbreekt, wordt standaard de landcode 'V.S.' ingevuld in het gegevensmodel.  

12. Klik op het tabblad Validaties.

    Deze indelingstoewijzing kan door de gebruiker gedefinieerde logica bevatten voor het valideren van de nauwkeurigheid van de geïmporteerde gegevens vanuit een zakelijk oogpunt. Bijvoorbeeld wordt op basis van de instelling voor elke transactie in het importbestand dat geen gedefinieerde landcode heeft, een waarschuwingsbericht gegenereerd in het infologboek waarmee de gebruiker wordt geïnformeerd over het probleem, met het volgnummer van de transactie.  

13. Sluit de pagina.

## <a name="run-the-format-mapping-to-the-data-model"></a>De indelingstoewijzing naar het gegevensmodel uitvoeren
Voer deze toewijzingsindeling uit om te testen. Gebruik het bestand 1099entries.xml, dat u eerder hebt gedownload. U kunt dit bestand exporteren vanuit de werkmap 1099entries.xlsx, die wordt gebruikt voor het beheer van leverancierstransacties. De gegenereerde uitvoer wordt geïmporteerd vanuit het geselecteerde XML-bestand en vult het aangepaste gegevensmodel bij de daadwerkelijke import.  

1. Klik op Uitvoeren.

    Klik op Bladeren en navigeer naar het bestand 1099entries.xml, dat u eerder hebt gedownload.  

2. Klik op OK.

    Let op de waarschuwing voor een ontbrekende landcode bij een transactie in het geïmporteerde bestand.  
    
    Bekijk de uitvoer in XML-indeling, die de gegevens vertegenwoordigt die zijn geïmporteerd vanuit het geselecteerde bestand en overgezet naar het gegevensmodel.   

3. Sluit de pagina.
4. Sluit de pagina.

## <a name="review-the-settings-for-the-model-mapping-to-the-destinations"></a>De instellingen van de modeltoewijzing naar de bestemmingen controleren
1. Selecteer in de structuur '1099 Payments model'.
2. Klik op Ontwerper.
3. Klik op Model toewijzen aan gegevensbron.

    De toewijzing 'For 1099 manual transactions import' is gedefinieerd met het richtingtype Naar bestemming (To destination). Dit betekent dat deze is ingevoerd om gegevensimport te ondersteunen en het instellen van regels bevat, die definiëren hoe het geïmporteerde externe bestand en gegevens die permanent zijn gemaakt als abstracte-gegevensmodel worden gebruikt om tabellen bij te werken in de toepassing.  

4. Klik op Ontwerper.
5. Vouw in de structuur 'model: Data model 1099 Payments model' uit.
6. Vouw in de structuur 'model: Data model 1099 Payments model\Transactions: Record list' uit.

    Merk op dat het ontworpen model hier wordt weergegeven als een element van de gegevensbron. Tijdens runtime bevat het de gegevens die uit het externe bestand zijn geïmporteerd. Meerdere tabellen zijn toegevoegd als gegevensbronelementen, om ervoor te zorgen dat de geïmporteerde gegevens compatibel is met de gegevens van de huidige toepassing, zoals of de leverancierrekening voor de importtransacties beschikbaar is in het systeem, of de combinatie van het importerende land en staatcodes bestaat, enz.  

7. Selecteer in de structuur 'model: Data model 1099 Payments model\Transactions: Record list\$failed: Calculated field = IF(OR(ISEMPTY(model.Transactions.'$refs'.vendor), ISEMPTY(model.Transactions.'$refs'.vendor1099), ISEMPTY(model.Transactions.'$refs'.box1099), ISEMPTY(model.Transactions.'$refs'.country), ISEMPTY(model.Transactions.'$refs'.state), ISEMPTY(model.Transactions.'$refs'.location)), true, false): Boolean'.
8. Klik op Bewerken.
9. Klik op Formule bewerken.

    Wanneer ten minste één validatie mislukt voor één geïmporteerde transactie, wordt deze transactie gemarkeerd als mislukt met het gegevensbronkenmerk '$failed'.  

10. Sluit de pagina.
11. Klik op Annuleren.
12. Selecteer in de structuur 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated'.
13. Klik op Bestemming bewerken'.

    Deze ER-bestemming is toegevoegd om op te geven hoe de geïmporteerde gegevens de toepassingstabellen bijwerken. In dit geval is de gegevenstabel VendSettlementTax1099 geselecteerd. Omdat de recordactie Insert is geselecteerd, worden de geïmporteerde transacties ingevoegd in de tabel VendSettlementTax1099. Houd er rekening mee dat één enkele toewijzing verschillende bestemmingen kan bevatten. Dit betekent dat de geïmporteerde gegevens kunnen worden gebruikt om meerdere toepassingstabellen tegelijk bij te werken. Tabellen, weergaven en gegevensentiteiten kunnen worden gebruikt als ER-bestemmingen.   

    Als de toewijzing wordt aangeroepen vanuit een punt in de toepassing (zoals een knop of menu-item) dat speciaal is ontworpen voor deze actie, moet de ER-bestemming worden gemarkeerd als het integratiepunt. In dit voorbeeld is dit het punt ERTableDestination#VendSettlementTax1099.  

14. Klik op Annuleren.
15. Klik op 'Alles weergeven'.
16. Klik op 'Alleen toegewezen weergeven'.
17. Vouw in de structuur 'tax1099trans: Table 'VendSettlementTax1099' records= model.Validated' uit.

    Merk op dat het gegevensbronelement dat de enige gevalideerde transacties bevat, is gebonden aan de gemaakte bestemming. U kunt de geïmporteerde transacties filteren om degene over te slaan die niet compatibel zijn met de gegevens in de toepassing.  

18. Selecteer in de structuur 'failed: Table 'VendSettlementTax1099Entity' records= model.Failed'.
19. Klik op het tabblad Validaties.

    Dit model kan door de gebruiker gedefinieerde logica bevatten voor het valideren van de juistheid van de bestaande toepassingsgegevens. Bijvoorbeeld wordt op basis van de huidige instelling voor elke transactie in het importbestand met een leveranciersrekening die niet in het systeem voorkomt, een waarschuwingsbericht gegenereerd in het infologboek waarmee de gebruiker wordt geïnformeerd over het probleem, met de foutieve leveranciersrekeningcode.  

    Houd er rekening mee dat u de optie Actie na validatie kunt gebruiken voor elke validatie, om op te geven of het importproces moet worden voortgezet of gestopt, en of de reeds uitgevoerde invoegingen/updates kunnen worden behouden of moeten worden teruggedraaid.  

20. Klik op 'Alleen toegewezen weergeven'.
21. Klik op 'Alles weergeven'.
22. Sluit de pagina.

    Voer deze modeltoewijzing uit om de ontworpen indelingen en modeltoewijzingen te testen. Gebruik het bestand 1099entries.xml. De gegevens uit het geselecteerde bestand worden in het systeem geïmporteerd.  

23. Klik op Uitvoeren.

    Merk op dat het dialoogvenster geen extra vragen bevat over het indelingstoewijzen waarmee het importbestand moet worden geparseerd en de gegevens worden overgezet naar het gegevensmodel. Dit komt doordat er momenteel slechts één indeling bestaat die gebruik maakt van dit model, dat is gemarkeerd voor ondersteuning van gegevensimport.  
    
    Definieer de boekstuk-ID zodanig dat onderscheid wordt gemaakt tussen de geïmporteerde transacties en andere transacties die al handmatig zijn ingevoerd of geïmporteerd.  

24. Typ in het veld Boekstuk-ID invoeren de tekst 'IMPORT-001'.

    Blader naar het bestand '1099entries.xml'.  

25. Klik op OK.

    De lijst met gegenereerde waarschuwingen geeft informatie over onjuiste leverancierrekeningen, een onjuiste 1099-belasting-vakcode, ontbrekende landcodes, enz. Vergelijk deze lijst met waarschuwingen met de inhoud die is opgenomen in het XML-uitvoeringsbestand.  

26. Sluit de pagina.
27. Sluit de pagina.
28. Sluit de pagina.
29. Sluit de pagina.
30. Ga naar Leveranciers > Periodieke taken >1099-belasting > Vereffening van leverancier voor 1099-aangiften.

    Dit formulier geeft de cumulatieve transacties weer in de tabel Tax1099Summary, die zijn gemaakt op basis van de geïmporteerde transacties.  

31. Stel in het veld Begindatum de datum in op "2000-01-01".
32. Klik op Handmatige 1099-transacties.

    Dit formulier bevat de lijst met transacties die handmatig zijn toegevoegd en degene die we net hebben geïmporteerd.  

33. Open het kolomfilter Boekstuk.
34. Typ de filterwaarde 'IMPORT-001' in het veld 'Boekstuk' met de filteroperator 'begint met'.

## <a name="review-the-relationship-between-model-and-format-mappings"></a>De relatie tussen het model en de indelingstoewijzingen controleren
1. Sluit de pagina.
2. Sluit de pagina.
3. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
4. Klik op Rapportconfiguraties.
5. Selecteer in de structuur '1099 Payments model'.

    Stel dat u import van dezelfde gegevens wilt ondersteunen, maar dan in een. TXT-bestandsindeling.   

6. Klik op Configuratie maken. Het dialoogvenster wordt geopend. 
7. Voer in het veld Nieuw de volgende tekst in: 'Indeling gebaseerd op gegevensmodel 1099 Payments model'.
8. Typ in het veld Naam: 'Gegevens importeren uit TXT-bestand'.
9. Selecteer in het veld Ondersteunt gegevensimport de waarde Ja.
10. Klik op Configuratie maken.
11. Klik op Ontwerper.
12. Klik op 'Indeling aan model toewijzen'.
13. Klik op Nieuw.
14. Typ of selecteer een waarde in het veld Definitie.

    Selecteer de optie '1099-MISC'.  

15. Typ in het veld Naam: 'Gegevens importeren uit TXT-bestand'.
16. Typ in het veld Beschrijving: 'Gegevens importeren uit TXT-bestand'.
17. Klik op Opslaan.
18. Sluit de pagina.
19. Sluit de pagina.
20. Klik op Bewerken.

    Als u de hotfix "KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions of Dynamics 365 Finance" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) hebt geïnstalleerd, voert u de volgende stap "Turn the flag 'Default for model mapping' on" uit voor de opgegeven indelingsconfiguratie. Sla anders de volgende stap over.  

21. Selecteer in het veld Standaard voor modeltoewijzing de waarde Ja.
22. Selecteer in de structuur '1099 Payments model'.
23. Klik op Ontwerper.
24. Klik op Model toewijzen aan gegevensbron.
25. Klik op Uitvoeren.

    Als u de hotfix "KB 4012871 Support of GER model mappings in separated configurations with an ability to specify different kinds of prerequisites for deploying them on different versions" ([KB 4012871](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871)) hebt geïnstalleerd, selecteert u de gewenste modeltoewijzing in het zoekveld. Als u de hotfix nog niet hebt geïnstalleerd, gaat u door met de volgende stap, omdat de toewijzing is al geselecteerd door de definitie van de standaardindelingsconfiguratie.  
    
    Als u de hotfix KB 4012871 niet hebt geïnstalleerd, ziet u dat het dialoogvenster een extra vraag bevat voor de modeltoewijzing die wordt gebruikt om het te importeren bestand te parseren. De gegevens worden vervolgens vanuit het dialoogvenster overgezet naar het gegevensmodel. U kunt op dit moment kiezen welke toewijzingsindeling moet worden gebruikt, afhankelijk van het type bestand dat u wilt importeren.  
    
    Als u van plan bent om deze modeltoewijzing aan te roepen vanuit een punt in de toepassing, dat speciaal is ontworpen voor de actie, moeten de ER-bestemming en de indelingstoewijzing zijn gemarkeerd als onderdeel van de integratie.  

26. Klik op Annuleren.
27. Sluit de pagina.
28. Sluit de pagina.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
