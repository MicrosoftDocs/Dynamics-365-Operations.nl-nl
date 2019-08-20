---
title: Een bestelopdracht maken die een offerteaanvraag gebruikt
description: In deze taakbegeleiding wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d80f84c148ff26bf008a97b06098bfd18c9062d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844148"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Een bestelopdracht maken die een offerteaanvraag gebruikt

[!include [task guide banner](../../includes/task-guide-banner.md)]

In deze taakbegeleiding wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces. Het voorbeeld dat in deze taakbegeleiding wordt weergegeven kan worden gebruikt in het demobedrijf USMF, en u moet als beheerder zijn aangemeld om alle stappen te kunnen voltooien. De taken in deze taakbegeleiding worden doorgaans uitgevoerd door inkoopprofessionals.


## <a name="create-a-requisition"></a>Een bestelopdracht maken
1. Ga naar Inkoop en sourcing > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Voer in het veld Aangevraagd een datum in.
5. Voer in het veld Boekingsdatum een datum in.
6. Klik op OK.
7. Typ of selecteer een waarde in het veld Reden.
8. Klik op Regel toevoegen.
9. Selecteer in het veld Inkoopcategorie een categorie in de structuur en klik vervolgens op OK.
10. Typ een waarde in het veld Productnaam.
11. Voer in het veld Hoeveelheid een getal in.
12. Typ of selecteer een waarde in het veld Eenheid.
13. Klik op Opslaan.
14. Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.
15. Klik op Aanbieden.
16. Sluit de pagina.
17. Klik op Aanbieden.

## <a name="reassign-a-workflow-task"></a>Een workflowtaak opnieuw toewijzen
    * De volgende taak is het maken van een offerteaanvraag om biedingen van leveranciers voor het product te ontvangen. In USMF-demogegevens wordt de bestelopdrachtworkflow ingesteld met een regel zodat als een leverancier niet wordt geselecteerd of de eenheidsprijs 0 is voor een regel, een taak wordt toegewezen aan een specifieke medewerker om een offerteaanvraag te maken. Als u wilt doorgaan met deze taakbegeleiding, moet u die taak opnieuw toewijzen aan een andere gebruiker (uzelf). U kunt dit alleen doen als u bent aangemeld als beheerder.  
1. Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.
2. Klik op Historie weergeven.
3. Vernieuw de pagina.
4. Vouw de sectie Details tracering uit.
5. Selecteer in de structuur de regel die begint met "Workflow voor regelartikelen die is geactiveerd op".
6. Klik op Workflowdetails weergeven.
7. Vouw de sectie Werkitems uit.
8. Klik op Opnieuw toewijzen.
9. Selecteer in het veld Gebruiker de optie Beheer.
10. Klik op Opnieuw toewijzen.
11. Sluit de pagina.
12. Sluit de pagina.

## <a name="create-an-rfq"></a>Een offerteaanvraag maken
1. Vernieuw de pagina.
2. Klik op Offerteaanvraag.
3. Selecteer USMF in het veld Kopende rechtspersoon.
    * U moet dezelfde rechtspersoon selecteren als op de aanvraagregel staat vermeld.  
4. Markeer in de lijst de geselecteerde rij.
    * Als u meerdere regels in uw opdracht tot inkoop had, selecteert u alle regels die aan de offerteaanvraag wilt toevoegen.  
5. Klik op OK.
6. Vernieuw de pagina.
7. Open het feitenvak en vouw vervolgens de sectie Gerelateerde documenten uit.
    * Mogelijk hebt u al een feitenvak geopend. Zoek het pictogram dat een pijl bevat, rechts van de wisselknoppen Regels/Koptekst. Als de pijl naar recht wijst, is het feitenvak al geopend. Als de pijl naar links wijst, klikt u erop om het feitenvak te openen.  
8. Klik op de koppeling in het veld Offerteaanvraag om de offerteaanvraag te openen die zojuist is gemaakt.
9. Klik op Koptekst.
10. Klik op Toevoegen.
11. Typ of selecteer een waarde in het veld Leveranciersrekening.
12. Klik op Toevoegen.
13. Typ of selecteer een waarde in het veld Leveranciersrekening.
14. Klik op Verzenden.
15. Klik op OK.
16. Klik op Antwoord invoeren.
17. Klik in het actievenster op Beantwoorden.
18. Klik op Gegevens kopiëren naar antwoord.
    * Hiermee worden gegevens, zoals de hoeveelheid en datums, van de offerteaanvraag naar het antwoord gekopieerd.  
19. Voer in het veld Eenheidsprijs een getal in.
    * Dit is de prijs die u van de leverancier hebt ontvangen. U kunt ook extra informatie van de leverancier invoeren.  
20. Klik op Accepteren.
21. Klik op OK.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Controleren of leverancier en prijs zijn overgebracht naar de bestelopdracht
1. Sluit de pagina.
2. Klik op Regels.
3. Klik op Verwante informatie.
4. Klik op Opdracht tot inkoop.
5. Selecteer de regel die is overgebracht naar de offerteaanvraag.
    * Controleer of de prijs en de leverancier zijn gekopieerd naar de bestelopdracht.  
6. Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.
7. Klik op Voltooien.
8. Sluit de pagina.
9. Klik op Voltooien.

