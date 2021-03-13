---
title: Een bestelopdracht maken die een offerteaanvraag gebruikt
description: In dit onderwerp wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05ff98b5fd95fa345d344e54d9116c73434e5de5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018891"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>Een bestelopdracht maken die een offerteaanvraag gebruikt

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt aangegeven hoe u prijs- en leveranciersgegevens kunt toevoegen aan een opdracht tot inkoop vanuit een offerteaanvraagproces. Het voorbeeld dat in deze taakbegeleiding wordt weergegeven kan worden gebruikt in het demobedrijf USMF, en u moet als beheerder zijn aangemeld om alle stappen te kunnen voltooien. De taken in deze taakbegeleiding worden doorgaans uitgevoerd door inkoopprofessionals.


## <a name="create-a-requisition"></a>Een bestelopdracht maken
1. Ga in het navigatievenster naar **Modules > Inkoopbeheer > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Naam**.
4. Voer in het veld **Gevraagde datum** een datum in.
5. Voer in het veld **Boekhoudingsdatum** een datum in.
6. Selecteer **OK**.
7. Typ of selecteer een waarde in het veld **Reden**.
8. Selecteer **Regel toevoegen**.
9. Selecteer in het veld **Inkoopcategorie** een categorie in de structuur en selecteer **OK**.
10. Typ een waarde in het veld **Productnaam**.
11. Voer een getal in het veld **Hoeveelheid** in.
12. In het veld **Eenheid** typt of selecteert u een waarde.
13. Selecteer **Opslaan**.
14. Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.
15. Selecteer **Indienen**.
16. Sluit de pagina.
17. Selecteer **Indienen**.

## <a name="reassign-a-workflow-task"></a>Een workflowtaak opnieuw toewijzen
De volgende taak is het maken van een offerteaanvraag om biedingen van leveranciers voor het product te ontvangen. In USMF-demogegevens wordt de bestelopdrachtworkflow ingesteld met een regel zodat als een leverancier niet wordt geselecteerd of de eenheidsprijs 0 is voor een regel, een taak wordt toegewezen aan een specifieke medewerker om een offerteaanvraag te maken. Als u wilt doorgaan met deze taakbegeleiding, moet u die taak opnieuw toewijzen aan een andere gebruiker (uzelf). U kunt dit alleen doen als u bent aangemeld als beheerder.  

1. Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.
2. Selecteer **Historie weergeven**.
3. Vernieuw de pagina.
4. Vouw de sectie **Details tracering** uit.
5. Selecteer in de structuur de regel die begint met "Workflow voor regel die is geactiveerd op".
6. Selecteer **Workflowdetails weergeven**.
7. Vouw de sectie **Werkitems** uit.
8. Selecteer **Opnieuw toewijzen**.
9. Selecteer in het veld **Gebruiker** de optie **Beheer**.
10. Selecteer **Opnieuw toewijzen**.
11. Sluit de twee pagina's.

## <a name="create-an-rfq"></a>Een offerteaanvraag maken

1. Vernieuw de pagina.
2. Selecteer **Offerteaanvraag**.
3. Selecteer **USMF** in het veld **Kopende rechtspersoon**. U moet dezelfde rechtspersoon selecteren als op de aanvraagregel staat vermeld.  
4. Markeer in de lijst de geselecteerde rij. Als u meerdere regels in uw opdracht tot inkoop had, selecteert u alle regels die aan de offerteaanvraag wilt toevoegen.  
5. Selecteer **OK**.
6. Vernieuw de pagina.
7. Zorg dat het feitenvak geopend is en vouw vervolgens de sectie **Gerelateerde documenten** uit.
8. Selecteer de koppeling in het veld **Offerteaanvraag** om de offerteaanvraag te openen die zojuist is gemaakt.
9. Selecteer **Koptekst**.
10. Selecteer **Toevoegen**.
11. In het veld **Leveranciersrekening** typt of selecteert u een waarde.
12. Selecteer **Toevoegen**.
13. In het veld **Leveranciersrekening** typt of selecteert u een waarde.
14. Selecteer **Verzenden**.
15. Selecteer **OK**.
16. Selecteer **Antwoord invoeren**.
17. Selecteer **Beantwoorden** in het actievenster.
18. Selecteer **Gegevens kopiëren naar antwoord**. Hiermee worden gegevens, zoals de hoeveelheid en datums, van de offerteaanvraag naar het antwoord gekopieerd.  
19. Voer een nummer in het veld **Eenheidsprijs** in. Dit is de prijs die u van de leverancier hebt ontvangen. U kunt ook extra informatie van de leverancier invoeren.  
20. Selecteer **Accepteren**.
21. Selecteer **OK**.

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>Controleren of leverancier en prijs zijn overgebracht naar de bestelopdracht
1. Sluit de pagina.
2. Selecteer **Regels**
3. Selecteer **Gerelateerde informatie**.
4. Selecteer **Opdracht tot inkoop**.
5. Selecteer de regel die is overgebracht naar de offerteaanvraag. Controleer of de prijs en de leverancier zijn gekopieerd naar de bestelopdracht.  
6. Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.
7. Selecteer Voltooien.
8. Selecteer de pagina.
9. Selecteer Voltooien.

