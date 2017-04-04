---
title: Budgetteringsoverzicht
description: "Bijna elk bedrijf dat gebruikmaakt van Financiën functionaliteit in Microsoft Dynamics 365 voor bewerkingen moet kunnen maken van rapporten van budget vs. werkelijke waarden. Dit artikel worden de minimale configuratie die nodig is om te kunnen maken van budgetten in Dynamics 365 for Operations of vanuit een programma van derden worden geladen."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: a639e509cf6a3d2f1b850f27481d7b95546522b8
ms.openlocfilehash: b62e14f7c91692ae97bb332b38b0deeb328cc1bd
ms.lasthandoff: 03/31/2017


---

# <a name="budgeting-overview"></a>Budgetteringsoverzicht

Bijna elk bedrijf dat gebruikmaakt van Financiën functionaliteit in Microsoft Dynamics 365 voor bewerkingen moet kunnen maken van rapporten van budget vs. werkelijke waarden. Dit artikel worden de minimale configuratie die nodig is om te kunnen maken van budgetten in Dynamics 365 for Operations of vanuit een programma van derden worden geladen.

<a name="overview"></a>Overzicht
--------

Het goedgekeurde budget voor een rechtspersoon wordt beheerd in een document dat een *budgetregisterregel* wordt genoemd. De regels in een document met budget kassa posten worden ook genoemd *budgetrekening* posten, en bevatten financiële dimensiegegevens, datums en de bedragen van het goedgekeurde budget. Het document met budget kassa posten is geïntegreerd met elementaire financiële rapporten en query's die zijn waar werkelijke grootboekbedragen worden vergeleken met gebudgetteerde bedragen. 

Er zijn meerdere methoden voor het maken van budgetregistervermeldingen in Dynamics 365 voor bewerkingen:

-   Voer handmatig de documentinformatie in op de pagina **Budgetregisterposten**.
-   Gebruik de Microsoft Excel-sjabloon die u kunt openen door op de knop **Openen in Excel** te klikken op de pagina **Budgetregisterposten**.
-   Gebruik de gegevensentiteit **Budgetjournaalregels** in gegevensentiteit om budgetregisterregels te importeren. U moet rekening houden met deze methode gebruikt en in te schakelen op de **ingesteld op basis** ** verwerking ** parameter wanneer u veel budgetjournaalregels in het systeem moet importeren.
-   Als het bedrijf de budgetplanningsfunctionaliteit gebruikt om budgetgegevens voor te bereiden, kunt u het periodieke proces **Budgetregisterpost genereren** gebruiken.

De budgetjournaalregel wordt beschouwd als voltooid wanneer de budgetsaldi zijn bijgewerkt. Op de **budgetjournaalregels** pagina, klikt u op **budgetsaldi bijwerken** registreren voor een geselecteerde budget meerdere posten. Nadat u de budgetsaldi hebt bijgewerkt, verandert de status van de budgetregisterregel in. **Voltooid** Ingevulde budgetregisterregel kan niet worden heropend voor bewerkingen. Daarom moet u, als de budgetgegevens moeten worden gecorrigeerd, een nieuwe budgetjournaalregel maken in plaats van gegevens in de ingevulde budgetregisterpost te corrigeren.

## <a name="configuration"></a>Configuratie
Wanneer u budgettering configureert, start op de pagina **Budgetteringsparameters**. Op deze pagina moet u het budgetjournaal, de nummerreeks voor budgetregisterregels, en het standaardgedrag in de werkruimten definiëren.

Vervolgens, als er beleid is dat de goedkeuring van budgetregisterregels bepaalt, gebaseerd op budgettype (bijvoorbeeld overboekingen of revisies), moet u de budgetregisterregelworkflows op de pagina **Budgetteringsworkflows** maken. Als er scenario's zijn waarin overboekingen toegestaan kunnen zijn zonder workflowgoedkeuring, kunt u budgettransferregels definiëren om deze scenario's te ondersteunen. 

Op de **Budgetteringsdimensies** pagina, moet u de financiële dimensies selecteren die voor budgettering worden gebruikt, op basis van de dimensies die in het rekeningschema worden gebruikt. U kunt alle financiële dimensies of een subset selecteren voor budgettering.

Definieer een * budgetmodel * die overeenkomt met alle of enkele van de budgetten. U kunt een enkel budgetmodel voor alle budgetregisterregels gebruiken. Als alternatief kunt u aparte modellen maken die zijn gebaseerd op het budgettype, de geografische locatie of een andere manier waarop een budget kan worden geclassificeerd. 

> [!NOTE] 
> Als u budgetbeheer gebruikt, kunt u slechts één budgetmodel koppelen aan een specifieke budgetcyclus budgetcyclusduur. 

*Budgetcodes *maken die het type budgettransacties identificeren dat moet worden vastgelegd en een eventuele gerelateerde werkstroom. Budgetcodes kunnen de volgende budgettypen ondersteunen:

-   Oorspronkelijk budget
-   Overboeken
-   Revisie
-   Vordering
-   Voorvordering
-   Overgeboekt budget

Met budgetcodes kunt u een audittrail krijgen van goedgekeurde budgetwijzigingen in de loop van de budgetcyclus. Als een werkstroom gekoppeld aan een budgetcode is en werkstroomstappen moeten zijn voltooid voordat de budgetregisterregel bereikt de werkstroom wordt ingeschakeld voor alle budgetregisterregels die budgetcode gebruiken de **voltooid** fase.  

U kunt desgewenst ook definiëren *budgetoverboekingsregels*. Als u regels voor budgetoverboekingen, schakelt **regels voor budgetoverboekingen gebruiken** op de **budgetparameters** pagina. Wanneer de budgetoverboekingsregels worden gebruikt, als een gebruiker een document maakt door een budgetcode van het type **Overboeking** te gebruiken, worden de budgetsaldi niet worden bijgewerkt als de budgetoverboekingsregels wordt geschonden. U kunt bijvoorbeeld budgetoverdrachtdocumenten toestaan waar het onkostenbudget wordt overgebracht tussen de hoofdrekeningen voor de afdeling Verkoop en marketing, maar kunt verbieden dat budget van of naar die afdeling wordt overgebracht, tenzij workflowgoedkeuring is verleend voor dat type budgetrekeningpost.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Werkruimten en querypagina's gebruiken om budget vs. werkelijk bij te houden
De budgetmanager kan de huidige status van een budget controleren in de werkruimte **Grootboekbudgetten en prognoses**. De tabbladen **Onkostenbudgetoverschrijding** en **Inkomsten onder budget** biedt een snelle weergave van de financiële dimensies waarin de budgetdoelen niet worden gehaald of de drempel benaderen. U kunt het budgetdrempelpercentage en de financiële dimensiesets personaliseren die op deze tabbladen worden gebruikt door op **Mijn werkruimte configureren** te klikken. U kunt klikken op **Beheerders van eenheden** om de werknemers weer te geven die voor specifieke financiële dimensiecombinaties verantwoordelijk zijn die op deze tabbladen zijn geselecteerd. Als u bijvoorbeeld ziet dat het onkostenbudget van de afdeling Bedrijfsactiviteiten over de budgetdrempel gaat, kunt u de manager van de afdeling Bedrijfsactiviteiten gemakkelijk vinden en contacteren om het probleem te bespreken. 

> [!NOTE] 
> De **afdelingsmanager** op de **organisatie-eenheden** pagina bepaalt welke managers specifieke financiële-dimensiecombinaties ondersteunen. Klik op **Meer weergeven** onder aan het tabblad om de querypagina **Budget vs. werkelijk** te openen voor meer informatie over budgetbedragen en werkelijke bedragen. 

Op de querypagina **Werkelijk vs. budget** kunt u inzoomen op de details de budgetbedragen in vergelijking met de werkelijke bedragen. Selecteer een regel op de querypagina, en klik vervolgens op **Periodesaldi** om budgetbedragen en werkelijke bedragen te bekijken verdeeld over boekperioden. De pagina **Budgetjournaalregels** bevat detailanalyse aan de details van het budgetbedrag in budgetregisterregels. De pagina **Algemeen journaalposten** opent de grootboektransacties die zijn opgenomen in het berekende bedrag voor **Werkelijke kosten**. 

Een bedrijf dat budgetplanningsfunctionaliteit gebruikt, kan *budgetprognoses *maken en gebruiken in de werkruimte **Grootboekbudgetten en prognoses**.


