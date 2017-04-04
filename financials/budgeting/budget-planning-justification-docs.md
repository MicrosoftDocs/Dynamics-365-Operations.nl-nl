---
title: documenten uitvullen
description: Redendocumenten voorzien in een verhaal daarom wordt gevraagd een budget om te verklaren waarom een specifiek budget nodig is.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>documenten uitvullen

Redendocumenten voorzien in een verhaal daarom wordt gevraagd een budget om te verklaren waarom een specifiek budget nodig is. 

Een sjabloon voor het plannen van budget is gemaakt door de budgetmanager in Microsoft Word en toegewezen aan het huidige budgetplanningsproces. Budget eigenaren open vervolgens de sjabloon en hebben gegevens automatisch in Word wordt ingevuld op basis van hun budgetaanvraag. Vervolgens kunnen ze extra tekst of gegevens voor opslaan en hun persoonlijke redenen document koppelen aan hun budgetplan toevoegen.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Instellen van Microsoft Dynamics Office-invoegtoepassing voor Microsoft Word

1.  Open een nieuw Microsoft Word-document.
2.  Klik op **invoegen** in het lint en op **winkel**.
3.  Zoeken naar Microsoft Dynamics Office-invoegtoepassing en klik op **Add**.
4.  Klik in Word in het rechterdeelvenster op **servergegevens toevoegen**.
5.  Typ of plak de URL van de server en klik op **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>De sjabloon redenen definiëren in Microsoft Word

1.  Klik op **ontwerp** in de Microsoft Dynamics Office toevoegen nadat u zich hebt aangemeld.
2.  Koptekstgegevens, gebruiken de **velden toevoegen** knop.
3.  Selecteer de gegevensbron voor de entiteit van budgetPlanJustification en op **volgende**. **opmerking:** deze entiteit is vereist voor elk document uitvullen. Andere entiteiten kunnen worden gebruikt, maar als deze entiteit niet opgenomen wordt, mislukt de upload terug naar Microsoft Dynamics 365 voor bewerkingen.
4.  De budgetPlanName, budgetPlanPreparer, ResponsibilityCenter en documentNumber labels en waarden in het Word-document toevoegen. **opmerking:** kunt u uw eigen aangepaste etiketten in plaats van de standaardlabels indien nodig.
5.  Klik op **doen** voor het voltooien van de koptekstsectie.
6.  Niveau regeldetails van budgetbedragen van het plan, klikt u op **tabel toevoegen**.
7.  Opnieuw, selecteert u de gegevensbron voor de entiteit van budgetPlanJustification en op **volgende**.
8.  Velden voor EffectiveDate, ScenarioName, AccountDisplayValue en AccountingCurrencyExpenseAmount toevoegen. **opmerking:** als opmerkingen beschikbaar om toe te voegen in afzonderlijke budgetplanregels zijn, die kunnen worden toegevoegd aan de tabel hier.
9.  Voeg eventuele extra aanwijzingen te geven voor de eindgebruiker en nodig opmaak of stijlen aan het document.
10. Sla het document op uw lokale computer en sluit het bestand voordat u doorgaat.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Het budgetplanningsproces instellen voor gebruik van de sjabloon uitvullen

1.  In Microsoft Dynamics 365 voor bewerkingen, gaat u naar **budgettering**&gt;**Setup**&gt;**budgetplanning**&gt;**uitvullen documentsjablonen**.
2.  Klik op **New** en blader naar het nieuwe Microsoft Word-document.
3.  Een sjabloon weergegeven naam en omschrijving invoeren. Click **OK**.
4.  Ga naar **budgettering**&gt;**Setup**&gt;**budget****planning**&gt;**budgetteren planningsproces**.
5.  Selecteer het proces waarin de redensjabloon moet worden gebruikt en klik op **bewerken**.
6.  In de **uitvullen documentsjabloon**, selecteert u de betreffende sjabloon en opslaan.

##### <a name="edit-and-save-personalized-justification-documents"></a>Bewerken en opslaan van persoonlijke redendocumenten

1.  In Dynamics 365 voor bewerkingen, een nieuw budgetplan maken of open een bestaand budgetplan.
2.  In de **uitvullen** vervolgkeuzelijst, selecteer **maken van nieuwe redenen**.
3.  Selecteer na het invullen van de details voor het uploaden van het aangepaste document in de **uitvullen** vervolgkeuzelijst.



