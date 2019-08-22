---
title: ER-configuraties ontwerpen om rapporten in Word-indeling te genereren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met een rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-indeling (elektronische rapportage) kan configureren, waarmee rapporten in de vorm van Microsoft Word-bestanden worden gegenereerd.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fd138fb5fea4098a862fbecba5e8ec226ed6afa9
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850298"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a>ER-configuraties ontwerpen om rapporten in Word-indeling te genereren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met een rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een ER-indeling (elektronische rapportage) kan configureren, waarmee rapporten in de vorm van Microsoft Word-bestanden worden gegenereerd. Deze stappen kunnen in het GBSI-bedrijf worden uitgevoerd.

Voordat u deze stappen uitvoert, moet u eerst de stappen uitvoeren in de taakbegeleiding “Een ER-configuratie maken voor het genereren van rapporten in OPENXML-indeling“. U moet van tevoren ook de volgende sjablonen downloaden en lokaal opslaan voor het voorbeeldrapport:

- [Sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)
- [Gebonden sjabloon van betalingsrapport](https://go.microsoft.com/fwlink/?linkid=862266)


Deze procedure is voor een functie die is toegevoegd in Microsoft Dynamics 365 for Operations, versie 1611.


## <a name="select-the-existing-er-report-configuration"></a>De bestaande ER-rapportconfiguratie selecteren
1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider 'Litware, Inc.' als actief is gemarkeerd.  
2. Klik op Rapportconfiguraties.
    * We recyclen de bestaande ER-configuratie die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.  
3. Vouw "Betalingsmodel" uit in de structuur.
4. Selecteer Betalingsmodel\Voorbeeldwerkbladrapport in de structuur.
5. Klik op Ontwerper.

## <a name="replace-the-excel-template-with-the-word-template"></a>De Excel-sjabloon vervangen door de Word-sjabloon
    * Momenteel wordt het Excel-document gebruikt als sjabloon voor het genereren van de uitvoer in OPENXML-indeling. We importeren de sjabloon van het rapport in Word-indeling.  
1. Klik op Bijlagen.
    * Vervang de bestaande Excel-sjabloon door de Word-sjabloon die u eerder hebt gedownload, SampleVendPaymDocReport.docx. Houd er rekening mee dat deze sjabloon alleen de indeling bevat van het document dat we willen genereren als ER-uitvoer.  
2. Klik op Verwijderen.
3. Klik op Ja.
4. Klik op Nieuw.
5. Klik op Bestand.
6. Klik op Bladeren. Navigeer naar en selecteer het bestand SampleVendPaymDocReport.docx, dat u eerder hebt gedownload. Klik op OK.
    * Selecteer de sjabloon die u in de vorige stap hebt gedownload.  
7. Typ of selecteer een waarde in het veld Sjabloon.

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a>De Word-sjabloon uitbreiden met een aangepast XML-onderdeel
1. Klik op Opslaan.
    * De actie Opslaan legt niet alleen de configuratiewijzigingen vast, maar werkt ook tegelijk de gekoppelde Word-sjabloon bij. De structuur van de ontworpen indeling wordt overgezet naar het gekoppelde Word-document als een nieuw aangepast XML-onderdeel met de naam 'Report'. Let erop dat de gekoppelde Word-sjabloon niet alleen de indeling van het document bevat dat we wilt genereren als ER-uitvoer, maar ook de structuur van gegevens die ER in deze sjabloon tijdens runtime invult.  
2. Klik op Bijlagen.
    * Nu moet u de elementen van het aangepaste XML-onderdeel 'Report' binden aan de delen van het Word-document.  
    * Als u ervaring hebt met Word-documenten die zijn ontwikkeld als formulieren met inhoudsbesturingselementen die gebonden zijn aan met elementen van aangepaste XML-onderdelen: speel alle stappen van de volgende subtaak af om een dergelijk document te maken. Zie deze koppeling https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US voor nadere details. Zo niet, dan kunt u alle stappen in de volgende subtaak overslaan.  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a>Word met aangepast XML-onderdeel gegevensbindingen laten uitvoeren
    * Open dit document in Word en doe het volgende: - Ga naar het tabblad Word-ontwikkelaar (pas het lint aan als dit tabblad nog niet is ingeschakeld).  - Selecteer het deelvenster XML-toewijzing.  - Selecteer het aangepaste XML-onderdeel 'Rapport' in de zoekopdracht.  - Voer de toewijzing uit van de elementen van het geselecteerde, aangepaste XML-onderdeel aan de inhoudsbesturingselementen van het Word-document.  - Sla het bijgewerkte Word-document op een lokaal station op.  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a>De Word-sjabloon met aangepaste XML-onderdeel, dat is gebonden aan inhoudsbesturingselementen, uploaden
1. Klik op Verwijderen.
2. Klik op Ja.
    * Voeg een nieuwe sjabloon toe. Als u de stappen in de vorige subtaak hebt uitgevoerd, selecteert u het Word-document dat u hebt voorbereid en lokaal opgeslagen. Selecteer anders de MS Word-sjabloon SampleVendPaymDocReportBounded.docx, die u eerder hebt gedownload.  
3. Klik op Nieuw.
4. Klik op Bestand.
5. Klik op Bladeren. Navigeer naar en selecteer het bestand SampleVendPaymDocReportBounded.docx, dat u eerder hebt gedownload. Klik op OK.
6. Selecteer in het veld Sjabloon het document dat u in de vorige stap hebt gedownload.
7. Klik op Opslaan.
8. Sluit de pagina.

## <a name="execute-the-format-to-create-word-output"></a>De indeling uitvoeren om Word-uitvoer te maken
1. Klik in het actievenster op Configuraties.
2. Klik op Gebruikersparameters.
3. Selecteer Ja in het veld Uitvoeringsinstellingen.
4. Klik op OK.
5. Klik op Bewerken.
6. Selecteer Ja in het veld Concept uitvoeren.
7. Klik op Opslaan.
8. Sluit de pagina.
9. Sluit de pagina.
10. Ga naar Leveranciers > Betalingen > Betalingsjournaal.
11. Klik op Regels.
12. Selecteer of deselecteer alle rijen in de lijst.
13. Klik op Betalingsstatus.
14. Klik op Geen.
15. Klik op Betalingen genereren.
16. Klik op OK.
17. Klik op OK.
    * Analyseer de gegenereerde uitvoer. Merk op dat de uitvoer wordt weergegeven in Word-indeling en de details van de verwerkte betalingen bevat.  

