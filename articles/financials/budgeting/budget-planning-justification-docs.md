---
title: Verantwoordingsdocumenten voor budgetplanning
description: Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2e711b14b202d477bd3f4bda09977fd33979fc94
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-justification-documents"></a>Verantwoordingsdocumenten voor budgetplanning

[!include[banner](../includes/banner.md)]


Verantwoordingsdocumenten bieden een beschrijving voor degenen die een budget aanvragen en willen uitleggen waarom een specifiek budget nodig is. 

Een budgetplansjabloon wordt gemaakt door de budgetmanager in Microsoft Word en toegewezen aan het huidige budgetplanningsproces. Budgeteigenaren kunnen de sjabloon vervolgens openen en gegevens automatisch in Word laten invullen op basis van hun budgetaanvraag. Vervolgens kunnen ze extra tekst of gegevens toevoegen voordat hun gepersonaliseerde verantwoordingsdocument wordt opgeslagen en gekoppeld aan hun budgetplan.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office-invoegtoepassing instellen voor Microsoft Word

1.  Open een nieuw Microsoft Word-document.
2.  Klik op **Invoegen** in het lint en klik vervolgens op **Opslag**.
3.  Zoek naar Microsoft Dynamics Office-invoegtoepassing en klik op **Toevoegen**.
4.  Klik in Word in het rechterdeelvenster op **Servergegevens toevoegen**.
5.  Typ of plak de URL van de server en klik op **OK**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>De sjabloon Reden definiëren in Microsoft Word

1.  Klik op **Ontwerp** in de Microsoft Dynamics Office-invoegtoepassing nadat u zich hebt aangemeld.
2.  Gebruik voor koptekstgegevens de knop **Velden toevoegen**.
3.  Selecteer de gegevensbron voor de entiteit BudgetPlanJustification en klik op **Volgende**. **Opmerking:** deze entiteit is vereist voor elk verantwoordingsdocument. Andere entiteiten kunnen worden gebruikt, maar weer uploaden naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition is niet mogelijk als deze entiteit niet is opgenomen.
4.  Voeg de labels en waarden BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter en DocumentNumber in het Word-document toe. **Opmerking:** u kunt desgewenst uw eigen aangepaste labels gebruiken in plaats van de standaardlabels.
5.  Klik op **Gereed** om de koptekstsectie te voltooien.
6.  Klik voor regelniveaudetails van budgetplanbedragen op **Tabel toevoegen**.
7.  Selecteer de gegevensbron voor de entiteit van BudgetPlanJustification opnieuw en klik op **Volgende**.
8.  Voeg velden voor EffectiveDate, ScenarioName, AccountDisplayValue en AccountingCurrencyExpenseAmount toe. **Opmerking:** als er opmerkingen beschikbaar zijn om toe te voegen in afzonderlijke budgetplanregels, kunnen deze hier aan de tabel worden toegevoegd.
9.  Voeg eventuele aanvullende instructies voor de eindgebruiker toe en pas indien nodig opmaak of stijlen op het document toe.
10. Sla het document op uw lokale computer op en sluit het bestand voordat u doorgaat.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Het budgetplanningsproces instellen voor gebruik van de sjabloon Reden

1.  Ga in Finance and Operations naar **Budgettering** &gt; **Instellen** &gt; **Budgetplanning** &gt; **Verantwoordingsdocumentsjablonen**.
2.  Klik op **Nieuw** en blader naar het nieuwe Microsoft Word-document.
3.  Voer een naam en beschrijving voor de sjabloonweergave in. Klik op **OK**.
4.  Ga naar **Budgettering** &gt; **Instellen** &gt; **Budget****planning** &gt; **Budgetplanningsproces**.
5.  Selecteer het proces waarin de redensjabloon moet worden gebruikt en klik op **Bewerken**.
6.  Selecteer in het veld **Verantwoordingsdocumentsjabloon** de juiste sjabloon en sla deze op.

##### <a name="edit-and-save-personalized-justification-documents"></a>Persoonlijke redendocumenten bewerken en opslaan

1.  Maak in Finance and Operations een nieuw budgetplan of open een bestaand budgetplan.
2.  Selecteer in het vervolgkeuzemenu **Reden** **Nieuwe verantwoording maken**.
3.  Geef na het invullen van de details aan dat u het aangepaste document wilt uploaden in het vervolgkeuzemenu **Reden**.





