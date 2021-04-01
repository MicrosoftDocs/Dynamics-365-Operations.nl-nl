---
title: Algemene journaalverwerking
description: Dit onderwerp beschrijft capaciteiten in Microsoft Dynamics 365 Finance die kunnen helpen algemene journaalverwerking eenvoudiger te maken en dat ook kan helpen waarborgen dat de juiste gegevens worden vastgelegd en dat geen inbreuk wordt gemaakt op de interne controle.
author: ShylaThompson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f9f19f0714fc160792a29261e21fe4ec8d62c4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249234"
---
# <a name="general-journal-processing"></a>Algemene journaalverwerking

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft capaciteiten die kunnen helpen algemene journaalverwerking eenvoudiger te maken en dat ook kan helpen waarborgen dat de juiste gegevens worden vastgelegd en dat geen inbreuk wordt gemaakt op de interne controle.  

## <a name="journal-names"></a>Journaalnamen

Een van de belangrijkste in te stellen gebieden is Journaalnamen. Het is verstandig om specifieke journaalnamen te definiëren voor elk doel, zoals intercompany, correctie toerekening en correctie van fouten. U kunt elke journaalnaam aanpassen om invoer van gegevens voor elk doel gemakkelijker en veiliger te maken. 

Op de pagina **Journaalnamen** kunt u de volgende elementen instellen:

-   **Goedkeuring workflow** - Om interne controle te verhogen, definieert u journaalworkflows die materiaallimieten vastleggen voor controle- en goedkeuringsstappen, op basis van criteria zoals totale debetbedrag wordt gebaseerd. U stelt workflows voor de algemene journalen in op de pagina **Grootboekworkflows**.
-   **Standaardwaarden** - Selecteer standaardwaarden voor tegenrekeningen, valuta en financiële dimensies.
-   **Journaalcontrole** - U kunt beperkingen instellen op het bedrijf en het rekeningtype, en ook de segmentwaarden. 

**Voorbeelden**

U kunt een journaalnaam alleen gebruiken voor correcties. In dit geval kunt u opgeven dat alleen het rekeningtype **Grootboek** geldig is voor alle bedrijven. 

[![Rekeningtypen voor journaalcontrole](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)

Een journaalnaam kan alleen worden gebruikt voor een specifiek segment of voor een bereik voor hoofdrekeningen. 

[![Journaalcontrolesegment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)

De optie **Automatische omkering** is beschikbare in algemene journalen. U hebt bijvoorbeeld een toerekeningscorrectie waar het werkelijke document nog niet van is verwerkt, zoals in de volgende afbeelding.
[![Omkering van algemeen journaal](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png) 

De Microsoft Excel-invoegtoepassing voor journaalboeking biedt een extra niveau van automatisering en maakt gegevensinvoer eenvoudiger. De actie **Regels openen in Excel** is beschikbaar op de pagina's **Algemeen journaal** en **Journaalboekstuk**. 

Op de pagina **Periodieke journalen** kunt u terugkerende journalen instellen om journaalverwerking te automatiseren. 

U kunt boekstuksjablonen gebruiken op elk gewenst moment. Op de pagina **Algemene journalen** vindt u de acties **Opslaan** en **Boekstuksjabloon selecteren** op de pagina **Journaalboekstuk** onder **Functies** voor de boekstukregels.

## <a name="related-setup"></a>Verwante instellingen
De volgende instellingen zijn niet specifiek voor algemene journalen, maar helpen te garanderen dat de gegevensinvoer juist en eenvoudig is.

### <a name="main-account"></a>Hoofdrekening

De instelling van de hoofdrekening biedt veel opties voor algemene journaalverwerking:

-   **DC/CR-behoefte** - Gebruik deze optie als een hoofdrekening is beperkt tot debet- of credittransacties. De instelling wordt geverifieerd wanneer een journaal is gevalideerd of geboekt.

-   **Standaardtegenrekening**
-   **Uitgesteld** - Stel een hoofdrekening uit voor gegevensinvoer over alle bedrijven of voor een bepaald bedrijf/bepaalde rechtspersoon.
-   **Handmatige invoer niet toestaan** - Voorkom dat gebruikers handmatig een waarde voor de rekening in journalen kunnen invoeren.
-   **Standaard/Valuta valideren**
-   **Overschrijvingen rechtspersoon** - Deze instelling is specifiek voor het opgegeven bedrijf of de opgegeven rechtspersoon:
    -   **Standaard/Btw valideren**
    -   **Standaarddimensie** - **Niet vast** of **Vaste waarde**. **Vaste waarde** helpt om ervoor te zorgen dat alle boekingen voor deze hoofdrekening altijd elke dimensie gebruiken die is ingesteld op **Vast**.
-   **Boekingsvalidatie**
    -   **Gebruikersvalidatie** - Deze optie bepaalt welke gebruikers naar een hoofdrekening kunnen boeken.
    -   **Validatie van boekingstype** - Deze optie bepaalt welke boekingstypen voor een hoofdrekening zijn toegestaan.

### <a name="accounting-structures-and-advanced-rules-structures"></a>Boekhoudingsstructuren en geavanceerde regelsstructuren

Boekhoudingsstructuren en geavanceerde regelsstructuren zijn uiterst belangrijk om te garanderen dat de gegevens die vereist zijn voor financiële rapportage en prestatie-opvolging worden vastgelegd tijdens de verwerking van het algemene journaal en eventuele documentatie. Met boekhoudingsstructuren en geavanceerde regelsstructuren kunt u de gegevensinvoerervaring aanpassen. U kunt ervoor zorgen dat gegevens alleen kunnen worden ingevoerd voor financiële dimensies die in elke situatie relevant zijn. Daarnaast kunt u de vereiste afdwingen dat altijd verplichte en juiste gegevens worden vastgelegd.

Zie de volgende onderwerpen voor meer informatie:
- [Uw rekeningschema plannen](plan-chart-of-accounts.md) 
- [Geavanceerde regels voor journalen maken](tasks/create-advanced-rules-journals.md)
- [Een journaalboeking maken met een sjabloon](tasks/create-journal-entry-template.md)
- [Journalen maken en valideren](tasks/create-validate-journals.md)
- [Periodieke journalen boeken](tasks/post-periodic-journals.md)
- [Grootboektoewijzingsjournaal verwerken](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a>Boeking simuleren
U kunt **Boeking simuleren** voor de meeste journalen vinden in het menu **Valideren**. Wanneer u een journaal valideert met de functie **Valideren**, wordt het journaal getest op specifieke foutvoorwaarden. Als u de functie **Boeking simuleren** gebruikt, worden dezelfde processen uitgevoerd als tijdens het boeken (zonder het journaal daadwerkelijk te boeken). Vervolgens kunt u de weergegeven boekingsberichten controleren, eventuele fouten corrigeren en het menu **Boeken** openen om het journaal te boeken. 

**Boeking simuleren** is niet beschikbaar voor batchverwerking. Er is echter code beschikbaar om boekingen in batch te simuleren en ontwikkelaars kunnen de code uitbreiden om die functionaliteit toe te voegen.  

## <a name="journal-unlock"></a>Journaal ontgrendelen
Op de journaalpagina is een knop beschikbaar om een journaal te ontgrendelen waarvan de status 'Vergrendeld door systeem' is ingesteld op Ja. Deze ontgrendeling kan worden uitgevoerd door een systeembeheerder die eventuele batchtaken heeft geanalyseerd en bevestigd dat het journaal niet meer actief wordt verwerkt door een batchtaak. Deze knop wordt ingeschakeld door de functie **Knop Journaal ontgrendelen** op de pagina **Functiebeheer** . 

## <a name="workflow-recall"></a>Werkstroom intrekken 
De mogelijkheid om een journaal in een werkstroom met de status 'Onherstelbaar' terug te roepen, wordt ingeschakeld via de knop **Workflow** in een journaal en op de pagina **Workflowhistorie**. Deze wordt ingeschakeld door de functie **De workflowstatus voor journalen opnieuw instellen** op de pagina **Functiebeheer**.

## <a name="delete-journal-lines"></a>Journaalregels verwijderen
De mogelijkheid om alle journaalregels snel te verwijderen, is in een journaal ingeschakeld onder **Functies** > **Journaalregels verwijderen**. Als u deze functie wilt inschakelen, selecteert u op de pagina **Functiebeheer** de optie **Prestatie-optimalisaties van journaal verwijderen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]