---
title: Algemene journaalverwerking
description: In dit artikel beschrijft de mogelijkheden in Microsoft Dynamics 365 voor bewerkingen die kunnen bijdragen tot merk algemeen journaal verwerking eenvoudiger en die ook kunnen helpen garanderen dat de juiste gegevens worden vastgelegd en interne controle niet is geknoeid.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 50cd203025be8857de943e458fc32315e494fb7a
ms.lasthandoff: 03/31/2017


---

# <a name="general-journal-processing"></a>Algemene journaalverwerking

Dit artikelen beschrijft capaciteiten in Microsoft Dynamics AX die kunnen helpen algemene journaalverwerking eenvoudiger te maken en dat ook kan helpen waarborgen dat de juiste gegevens worden vastgelegd en dat geen inbreuk wordt gemaakt op de interne controle.  

Journaalnamen

Een van de belangrijkste gebieden instellen van is Journaalnamen. Het is verstandig om te definiëren van specifieke journaalnamen voor elk doel, zoals intercompany-, correctie van de toerekening en correctie van fouten. U kunt elke journaalnaam om invoer van gegevens voor elk doel gemakkelijk en veilig op maat maken. 

Op de pagina **Journaalnamen** kunt u de volgende elementen instellen:

-   **Goedkeuring workflow** - Om interne controle te verhogen, definieert u journaalworkflows die materiaallimieten vastleggen voor controle- en goedkeuringsstappen, op basis van criteria zoals totale debetbedrag wordt gebaseerd. Workflows voor de algemene journalen instellen op de ** grootboek workflows ** pagina.
-   **Standaardwaarden** - Selecteer standaardwaarden voor tegenrekeningen, valuta en financiële dimensies.
-   **Journaalcontrole** - U kunt beperkingen instellen op het bedrijf en het rekeningtype, en ook de segmentwaarden. 

**Voorbeelden**

U kunt een journaalnaam alleen gebruiken voor correcties. In dit geval kunt u opgeven dat alleen het rekeningtype **Grootboek** geldig is voor alle bedrijven. [![Journaal rekening controletypen](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Een journaalnaam kan alleen worden gebruikt voor een specifiek segment of voor een bereik voor hoofdrekeningen. [![Journaal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

De optie **Automatische omkering** is beschikbare in algemene journalen. U hebt bijvoorbeeld een toerekeningscorrectie waar het werkelijke document nog niet van is verwerkt, zoals in de volgende afbeelding.
[![Algemeen journaal omkeren](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

De Microsoft Excel-invoegtoepassing voor journaalpost biedt een extra beveiligingsniveau automatisering en gegevensinvoer eenvoudiger maakt. De actie **Regels openen in Excel **is beschikbaar op de pagina's **Algemeen journaal** en **Journaalboekstuk**. 

Op de pagina **Periodieke journalen** kunt u terugkerende journalen instellen om journaalverwerking te automatiseren. 

U kunt boekstuksjablonen gebruiken op elk gewenst moment. Op de **algemene journalen** pagina, de **opslaan** en **boekstuksjabloon selecteren** acties staan in de **journaalboekstuk** pagina onder **functies** voor de boekstukregels.

## <a name="related-setup"></a>Verwante instellingen
De volgende instellingen zijn niet specifiek voor algemene journalen, maar helpen te garanderen dat de gegevensinvoer juist en eenvoudig is.

### <a name="main-account"></a>Hoofdrekening

De instelling van de hoofdrekening biedt veel opties voor algemene journaalverwerking:

-   **DC/CR-behoefte** - Gebruik deze optie als een hoofdrekening is beperkt tot debet- of credittransacties. De instelling wordt geverifieerd wanneer een journaal is gevalideerd of geboekt.
-   **Standaardtegenrekening**
-   **Uitgesteld** - Stel een hoofdrekening uit voor gegevensinvoer over alle bedrijven of voor een bepaald bedrijf/bepaalde rechtspersonen.
-   **Handmatige invoer niet toestaan** - Voorkom dat gebruikers handmatig een waarde voor de rekening in journalen kunnen invoeren.
-   **Standaard/Valuta valideren**
-   **Overschrijvingen rechtspersoon** - Deze instelling is specifiek voor het opgegeven bedrijf of de opgegeven rechtspersoon:
    -   **Standaard/Btw valideren**
    -   **Standaarddimensie** - **Niet vast** of **Vaste waarde**. **Vaste waarde** helpt om ervoor te zorgen dat alle boekingen voor deze hoofdrekening altijd elke dimensie gebruiken die is ingesteld op **Vast**.
-   **Boekingsvalidatie**
    -   **Gebruikersvalidatie** - Deze optie bepaalt welke gebruikers naar een hoofdrekening kunnen boeken.
    -   **Validatie van boekingstype** - Deze optie bepaalt welke boekingstypen voor een hoofdrekening zijn toegestaan.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Boekhoudingsstructuren en geavanceerde regelsstructuren

Boekhoudingsstructuren en geavanceerde regelsstructuren zijn uiterst belangrijk voor het garanderen dat de gegevens die vereist zijn voor financiële rapportage en prestatie-opvolging worden vastgelegd tijdens de verwerking van het algemeen journaal en eventuele documentatie. Met boekhoudingsstructuren en geavanceerde regelsstructuren kunt u de gegevensinvoerervaring aanpassen. U kunt ervoor dat gegevens alleen kunnen worden ingevoerd voor financiële dimensies die in elke situatie relevant zijn, en u kunt ook de behoefte afdwingen dat altijd verplichte en juiste gegevens worden vastgelegd.

Zie voor meer informatie [Planning: rekeningschema](plan-chart-of-accounts.md). 


