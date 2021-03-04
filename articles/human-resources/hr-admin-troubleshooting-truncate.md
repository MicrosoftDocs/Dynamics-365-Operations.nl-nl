---
title: Tekstafbreking in de positiehiërarchie vermijden en exporteren naar Visio
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat namen van personen en posities worden afgekapt wanneer klanten de positiehiërarchie weergeven in Microsoft Dynamics 365 Human Resources. Tekstafbreking kan het moeilijk maken om een schermopname te maken of de hiërarchie af te drukken.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 02fb0098cc6f5a0b353e827653b1c8c96af2470c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417986"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Tekstafbreking in de positiehiërarchie vermijden en exporteren naar Visio

**Probleem**

Als een klant de positiehiërarchie weergeeft in Microsoft Dynamics 365 Human Resources, worden de namen van personen en posities afgebroken. Daarom kan het lastig zijn om een schermopname te maken of de hiërarchie af te drukken en te distribueren.

![Positiehiërarchie](media/position-h.png)

**Oorzaak**

Dit is zo ontworpen.

**Resolutie**

Helaas kunnen gebruikers de grootte van de tekst niet gemakkelijk wijzigen. U kunt de positiehiërarchie echter uit Human Resources exporteren en vervolgens importeren in Microsoft Visio. Hoewel het volgende artikel is geschreven voor Microsoft Dynamics AX 2012, is het proces ook van toepassing op Human Resources: [Een positiehiërarchie exporteren naar Microsoft Visio](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Volg deze stappen om te exporteren naar Visio.

1. Open in Human Resources de lijstpagina **Posities**.

    Als u meer informatie in het diagram van de structuur van organisatie wilt opnemen, voegt u velden toe aan de lijst **Posities**, zodat deze beschikbaar zijn wanneer u de wizard verderop in deze procedure gebruikt.

2. Selecteer in het actievenster de knop **Openen in Microsoft Office** en selecteer vervolgens onder **Exporteren naar Excel** de optie **Posities**. Of druk op Ctrl+T.

    ![De lijstpagina Posities exporteren naar Excel](media/org-admin.png)

3. Sla het geëxporteerde Excel-bestand op.

    ![Het dialoogvenster Exporteren naar Excel](media/export-excel.png)

4. Selecteer in Visio de optie **Visio - Nieuwe maken** en selecteer de sjablooncategorie **Zakelijk**.

    ![Nieuw diagram](media/new.png)

5. Selecteer **Wizard Organigram** en vervolgens **Maken**.

    ![Het dialoogvenster Wizard Organigram](media/orgchart-wizard.png)

6. Selecteer **Gegevens die al zijn opgeslagen in een bestand of database** en selecteer **Volgende**.

    ![Wizard Organigram 1](media/orgchart-wizard7.png)

7. Kies **Een tekst-, Org Plus- (\*.txt) of Excel-bestand** en selecteer **Volgende**.

    ![Wizard Organigram 2](media/orgchart-wizard3.png)

8. Ga naar het geëxporteerde Excel-bestand met de positiehiërarchie en selecteer **Volgende**.

    ![Wizard Organigram 3](media/orgchart-wizard2.png)

9. Stel het veld **Naam** in op **Positie**, stel het veld **Rapporteert aan** in op **Verantwoording aan positie** en selecteer vervolgens **Volgende**.

    ![Wizard Organigram 4](media/orgchart-wizard1.png)

10. Selecteer de velden die moeten worden weergegeven voor elk knooppunt en selecteer vervolgens **Volgende**.

    ![Wizard Organigram 5](media/orgchart-wizard5.png)

11. Voeg de kolom **Positie** toe aan de lijst **Shapegegevensvelden** en selecteer vervolgens **Volgende**.

    ![Wizard Organigram 6](media/orgchart-wizard6.png)

12. Afbeeldingen zijn momenteel niet beschikbaar. Selecteer daarom **Volgende** op de volgende pagina.
13. Selecteer **Ik wil dat het organigram automatisch over de pagina's wordt verdeeld**.

    ![Wizard Organigram 7](media/orgchart-wizard4.png)

14. Selecteer **Voltooien**.

    Als er posities zijn die niet in de structuur zijn opgenomen, wordt u gevraagd om deze op te nemen in het diagram.

In het diagram dat wordt gegenereerd in Visio wordt elke manager in een afzonderlijk werkblad weergegeven.

Op basis van de velden die u hebt geselecteerd voor het diagram worden voor elk knooppunt de relevante gegevens weergegeven wanneer het Visio-bestand wordt gegenereerd.

![Hiërarchiediagram](media/hierarchy.png)

**Aanvullende optie**

In Human Resources kunt u mogelijk ook het werkgebied **Mensen** gebruiken om bepaalde hiërarchiegerelateerde informatie weer te geven.


[!INCLUDE[footer-include](../includes/footer-banner.md)]