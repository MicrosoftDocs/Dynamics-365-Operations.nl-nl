--- 
title: Expressies ontwerpen om methoden voor toepassingsklassen aan te roepen (ER)
description: Deze handleiding bevat informatie over het opnieuw gebruiken van de bestaande toepassingslogica in ER-configuraties (elektronische rapportage) door vereiste methoden van toepassingsklassen aan te roepen in ER-expressies.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 631fa7bae808856efb8b95700fd2a85e6d5f8725
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---
# <a name="design-expressions-to-call-application-class-methods-er"></a>Expressies ontwerpen om methoden voor toepassingsklassen aan te roepen (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze handleiding bevat informatie over het opnieuw gebruiken van de bestaande toepassingslogica in ER-configuraties (elektronische rapportage) door vereiste methoden van toepassingsklassen aan te roepen in ER-expressies. Waarden van argumenten voor het aanroepen van klassen kunnen tijdens de uitvoering dynamisch worden gedefinieerd: bijvoorbeeld op basis van gegevens in het parseerdocument om de juistheid te waarborgen. In deze taakbegeleider maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Deze procedure is gemaakt voor gebruikers met de toegewezen rol van Systeembeheerder of Elektronische aangifteontwikkelaar. 

Deze stappen kunnen worden voltooid met elke dataset. U moet ook het volgende bestand downloaden en lokaal opslaan: (https://go.microsoft.com/fwlink/?linkid=862266): SampleIncomingMessage.txt.

Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "ER Een configuratieprovider maken en deze als actief markeren" voltooien.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en is gemarkeerd als actief. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" uitvoeren.   
    * Laten we ervan uitgaan dat u een proces ontwerpt voor het parseren van inkomende bankafschriften voor het bijwerken van toepassingsgegevens. U ontvangt de inkomende bankafschriften als TXT-bestanden die IBAN-codes bevatten. Als onderdeel van het importproces van het bankafschrift moet u de juistheid van deze IBAN-codes valideren met behulp van de logica die al beschikbaar is in Dynamics 365 for Finance and Operations.   

## <a name="import-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie importeren
1. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de Microsoft-providertegel.  
2. Klik op Opslagplaatsen.
3. Klik op Filters weergeven.
4. Voeg het filterveld ‘Typenaam’ toe. In het veld Naam voert u de waarde 'resources' in, selecteert u de filteroperator 'bevat' en klikt u vervolgens op Toepassen.
5. Klik op Openen.
6. Selecteer Betalingsmodel in de structuur.
    * Als de knop Importeren in het sneltabblad Versies niet is ingeschakeld, hebt u versie 1 al geïmporteerd van de ER-configuratie 'Betalingsmodel'. U kunt de overige stappen in deze subtaak overslaan.   
7. Klik op Importeren.
8. Klik op Ja.
9. Sluit de pagina.
10. Sluit de pagina.

## <a name="add-a-new-er-format-configuration"></a>Een nieuwe ER-indelingsconfiguratie toevoegen
1. Klik op Rapportconfiguraties.
    * Voeg een nieuwe ER-indeling toe om inkomende bankafschriften in TXT-indeling te parseren.  
2. Selecteer Betalingsmodel in de structuur.
3. Klik op Configuratie maken om het menu van het dialoogvenster te openen.
4. Voer in het veld Nieuw veld "Indeling gebaseerd op gegevensmodel PaymentModel" in.
5. Typ in het veld Naam 'Importindeling bankafschrift (voorbeeld)'.
    * Importindeling (voorbeeld) voor bankrekeningafschrift  
6. Selecteer in het veld Ondersteunt gegevensimport de waarde Ja.
7. Klik op Configuratie maken.

## <a name="design-the-er-format-configuration---format"></a>De configuratie voor de ER-indeling ontwerpen - indeling
1. Klik op Ontwerper.
    * De ontworpen opmaak vertegenwoordigt de verwachte structuur van het externe bestand in TXT-indeling.  
2. Klik op Basis toevoegen om het menu van het dialoogvenster te openen.
3. Selecteer in de structuur 'Tekst\Reeks'.
4. Typ Basis in het veld Naam.
    * Hoofdmap  
5. Selecteer in het veld Speciale tekens 'Nieuwe regel - Windows (CR LF)'.
    * De optie 'Nieuwe regel - Windows (CR LF)' is geselecteerd in het veld 'Speciale tekens'. Op basis van deze instelling wordt elke regel in het parseerbestand beschouwd als een afzonderlijke record.  
6. Klik op OK.
7. Klik op Toevoegen om het dialoogvenster te openen.
8. Selecteer in de structuur 'Tekst\Reeks'.
9. Typ 'Rijen' in het veld Naam.
    * Rijen  
10. Selecteer in het veld Multipliciteit 'Éen veel'.
    * De optie 'Een veel' is geselecteerd in het veld 'Multipliciteit'. Op basis van deze instelling wordt verwacht dat ten minste één regel wordt weergegeven in het parseerbestand.  
11. Klik op OK.
12. Selecteer in de structuur 'Root\Rows'.
13. Klik op Reeks toevoegen.
14. Typ 'Velden' in het veld Naam.
    * Velden  
15. Selecteer in het veld Multipliciteit 'Precies één'.
16. Klik op OK.
17. Selecteer in de structuur 'Root\Rows\Fields'.
18. Klik op Toevoegen om het dialoogvenster te openen.
19. Selecteer "Text\String" in de structuur.
20. Typ "IBAN" in het veld Naam.
    * IBAN  
21. Klik op OK.
    * Volgens de configuratie bevat elke regel in het parseerbestand alleen de IBAN-code.  
22. Klik op Opslaan.

## <a name="design-the-er-format-configuration--mapping-to-data-model"></a>De configuratie voor de ER-indeling - toewijzen aan gegevensmodel
1. Klik op 'Indeling aan model toewijzen'.
2. Klik op Nieuw.
3. Typ in het veld Definitie: 'BankToCustomerDebitCreditNotificationInitiation'.
    * BankToCustomerDebitCreditNotificationInitiation  
4. ResolveChanges de definitie.
5. Typ 'Toewijzing aan gegevensmodel' in het veld Naam.
    * Toewijzen aan gegevensmodel  
6. Klik op Opslaan.
7. Klik op Ontwerper.
8. Selecteer in de structuur 'Dynamics 365 for Operations\Class'.
9. Klik op Basis toevoegen.
    * Een nieuwe gegevensbron om de bestaande toepassingslogica aan te roepen voor validatie van IBAN-codes.  
10. Typ 'check_codes' in het veld Naam.
    * check_codes  
11. Typ 'ISO7064' in het veld Klasse.
    * ISO7064  
12. Klik op OK.
13. Vouw in de structuur 'indeling' uit.
14. Vouw in de structuur 'indeling\Root: Sequence(Root)' uit.
15. Selecteer in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)'.
16. Klik op Binden.
17. Vouw in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)' uit.
18. Vouw in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)' uit.
19. Selecteer in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.
20. Vouw in de structuur 'Betalingen = format.Root.Rows' uit.
21. Vouw in de structuur 'Betalingen = format.Root.Rows\Creditor Account(CreditorAccount)' uit.
22. Vouw in de structuur 'Betalingen = format.Root.Rows\Creditor Account(CreditorAccount)Identification' uit.
23. Selecteer in de structuur 'Betalingen = format.Root.Rows\Creditor Account(CreditorAccount)\Identification\IBAN'.
24. Klik op Binden.
25. Klik op het tabblad Validaties.
26. Klik op Nieuw.
    * Voeg een nieuwe validatieregel toe waarin een fout wordt weergegeven voor elke regel in het parseerbestand met een ongeldige IBAN-code.  
27. Klik op Voorwaarde bewerken.
28. Vouw 'check_codes' uit in de structuur.
29. Selecteer 'check_codes\verifyMOD1271_36' in de structuur.
30. Klik op Gegevensbron toevoegen.
31. Typ in het veld Formule 'check_codes.verifyMOD1271_36('.
    * check_codes.verifyMOD1271_36(  
32. Vouw in de structuur 'indeling' uit.
33. Vouw in de structuur 'indeling\Root: Sequence(Root)' uit.
34. Vouw in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)' uit.
35. Vouw in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)' uit.
36. Selecteer in de structuur 'indeling\Root: Sequence(Root)\Rows: Sequence 1..* (Rows)\Fields: Sequence 1..1 (Fields)\IBAN: String(IBAN)'.
37. Klik op Gegevensbron toevoegen.
38. Typ in het veld Formule 'check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)'.
    * check_codes.verifyMOD1271_36(format.Root.Rows.Fields.IBAN)  
39. Klik op Opslaan.
40. Sluit de pagina.
    * De validatievoorwaarde is geconfigureerd om FALSE terug te sturen voor een eventuele ongeldige IBAN-code door het aanroepen van de bestaande methode 'verifyMOD1271_36' van toepassingklasse 'ISO7064'. Houd er rekening mee dat de waarde van de IBAN-code dynamisch wordt gedefinieerd tijdens de uitvoering als het argument van de aanroepende methode op basis van de inhoud van het TXT-parseerbestand.   
41. Klik op Bericht bewerken.
42. Typ in het veld Formule 'CONCATENATE("Ongeldige IBAN-code gevonden:  ", format.Root.Rows.Fields.IBAN)'.
    * CONCATENATE("Ongeldige IBAN-code gevonden:  ", format.Root.Rows.Fields.IBAN)  
43. Klik op Opslaan.
44. Sluit de pagina.
45. Klik op Opslaan.
46. Sluit de pagina.

## <a name="run-the-format-mapping"></a>De toewijzing van de bestandsindeling uitvoeren
Voer voor testdoeleinden de toewijzing van de indeling uit met behulp van het SampleIncomingMessage.txt-bestand dat u hebt gedownload. De gegenereerde uitvoer omvat gegevens die worden geïmporteerd vanuit het geselecteerde TXT-bestand en ingevuld in het aangepaste gegevensmodel tijdens de daadwerkelijke import.   
1. Klik op Uitvoeren.
    * Klik op Bladeren en navigeer naar het bestand SampleIncomingMessage.txt, dat u eerder hebt gedownload.  
2. Klik op OK.
    * Bekijk de uitvoer in XML-indeling, die de gegevens vertegenwoordigt die zijn geïmporteerd vanuit het geselecteerde bestand en overgezet naar het gegevensmodel. Slechts 3 regels van het geïmporteerde TXT-bestand zijn verwerkt. De ongeldige IBAN-code op regel 4 is overgeslagen en een foutbericht wordt weergegeven in het infologboek.  


