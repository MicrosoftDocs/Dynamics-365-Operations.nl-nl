---
title: Budgetteringsoverzicht
description: Bijna elk bedrijf dat gebruikmaakt van de functionaliteit Financiële items in Microsoft Dynamics 365 Finance, moet rapporten kunnen maken van gebudgetteerde versus werkelijke waarden. In dit artikel wordt de minimale configuratie uitgelegd die nodig is om budgetten in Finance and Operations te kunnen maken of budgetten te kunnen laden vanuit een programma van derden.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 60113
ms.assetid: 28a9793e-d376-47af-a345-69046bad17df
ms.search.region: global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 36144474defc4849a112a180247f37796de00a27
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441974"
---
# <a name="budgeting-overview"></a>Overzicht van Budgettering

[!include [banner](../includes/banner.md)]

Bijna elk bedrijf dat gebruikmaakt van de functionaliteit Financiële items in Microsoft Dynamics 365 Finance, moet rapporten kunnen maken van gebudgetteerde versus werkelijke waarden. In dit artikel wordt de minimale configuratie uitgelegd die nodig is om budgetten in Finance and Operations te kunnen maken of budgetten te kunnen laden vanuit een programma van derden.

<a name="overview"></a>Overzicht
--------

Het goedgekeurde budget voor een rechtspersoon wordt beheerd in een document dat een *budgetregisterregel* wordt genoemd. De regels in een budgetjournaalpostdocument worden *budgetrekeningposten* genoemd, en bevatten financiële dimensiegegevens, datums en de bedragen van het goedgekeurde budget. Het document met budgetjournaalposten is geïntegreerd met elementaire financiële rapporten en querypagina´s waarin werkelijke bedragen worden vergeleken met gebudgetteerde bedragen. 

Er zijn meerdere methoden om budgetregisterposten te maken:

-   Voer handmatig de documentinformatie in op de pagina **Budgetregisterposten**.
-   Gebruik de Microsoft Excel-sjabloon die u kunt openen door op de knop **Openen in Excel** te klikken op de pagina **Budgetregisterposten**.
-   Gebruik de gegevensentiteit **Budgetjournaalregels** in gegevensentiteit om budgetregisterregels te importeren. U kunt overwegen deze methode te gebruiken en de parameter **Op sets gebaseerde** **verwerking** in te schakelen wanneer u veel budgetjournaalposten in het systeem moet importeren.
-   Als het bedrijf de budgetplanningsfunctionaliteit gebruikt om budgetgegevens voor te bereiden, kunt u het periodieke proces **Budgetregisterpost genereren** gebruiken.

De budgetjournaalpost wordt beschouwd als voltooid wanneer de budgetsaldi zijn bijgewerkt. Op de pagina **Budgetjournaalposten** klikt u op **Budgetsaldi bijwerken** voor een geselecteerde budgetjournaalpost of meerdere posten. Nadat u de budgetsaldi hebt bijgewerkt, verandert de status van de budgetregisterregel in. **Voltooid** Ingevulde budgetregisterregel kan niet worden heropend voor bewerkingen. Daarom moet u, als de budgetgegevens moeten worden gecorrigeerd, een nieuwe budgetjournaalregel maken in plaats van gegevens in de ingevulde budgetregisterpost te corrigeren.

## <a name="configuration"></a>Configuratie
Wanneer u budgettering configureert, start op de pagina **Budgetteringsparameters**. Op deze pagina moet u het budgetjournaal, de nummerreeks voor budgetregisterregels, en het standaardgedrag in de werkruimten definiëren.

Vervolgens, als er beleid is dat de goedkeuring van budgetregisterregels bepaalt, gebaseerd op budgettype (bijvoorbeeld overboekingen of revisies), moet u de budgetregisterregelworkflows op de pagina **Budgetteringsworkflows** maken. Als er scenario's zijn waarin overboekingen toegestaan kunnen zijn zonder workflowgoedkeuring, kunt u budgettransferregels definiëren om deze scenario's te ondersteunen. 

Op de **Budgetteringsdimensies** pagina, moet u de financiële dimensies selecteren die voor budgettering worden gebruikt, op basis van de dimensies die in het rekeningschema worden gebruikt. U kunt alle financiële dimensies of een subset selecteren voor budgettering.

Definieer een *budgetmodel* dat correspondeert met alle of enkele budgetten. U kunt een enkel budgetmodel voor alle budgetregisterregels gebruiken. Als alternatief kunt u aparte modellen maken die zijn gebaseerd op het budgettype, de geografische locatie of een andere manier waarop een budget kan worden geclassificeerd. 

> [!NOTE] 
> Als budgetbeheer wordt gebruikt, kunt u slechts één budgetmodel aan een specifieke budgetcyclustijd koppelen. 

*Budgetcodes* maken die het type budgettransacties identificeren dat moet worden vastgelegd en een eventuele gerelateerde werkstroom. Budgetcodes kunnen de volgende budgettypen ondersteunen:

-   Oorspronkelijk budget
-   Overboeken
-   Revisie
-   Vordering
-   Voorvordering
-   Overgeboekt budget

Met budgetcodes kunt u een audittrail krijgen van goedgekeurde budgetwijzigingen in de loop van de budgetcyclus. Als een werkstroom is gekoppeld aan een budgetcode, wordt de werkstroom ingeschakeld voor alle budgetjournaalposten die de desbetreffende budgetcode gebruiken en moeten werkstroomstappen worden uitgevoerd voordat de budgetjournaalpost de fase **Voltooid** kan bereiken.  

U kunt desgewenst ook *budgetoverboekingsregels* instellen. Als u budgetoverboekingsregels wilt gebruiken, schakelt u **Regels voor budgetoverboekingen gebruiken** op de pagina **Budgetparameters** in. Wanneer de budgetoverboekingsregels worden gebruikt, als een gebruiker een document maakt door een budgetcode van het type **Overboeking** te gebruiken, worden de budgetsaldi niet worden bijgewerkt als de budgetoverboekingsregels wordt geschonden. U kunt bijvoorbeeld budgetoverdrachtdocumenten toestaan waar het onkostenbudget wordt overgebracht tussen de hoofdrekeningen voor de afdeling Verkoop en marketing, maar kunt verbieden dat budget van of naar die afdeling wordt overgebracht, tenzij workflowgoedkeuring is verleend voor dat type budgetrekeningpost.

Functionaliteit die in Microsoft Dynamics 365 Finance versie 10.0.7 (januari 2020) werd geïntroduceerd voegde mogelijkheden en flexibiliteit toe voor budgetregistervermeldingen. Als u deze uitbreidingen wilt inschakelen, gaat u naar de werkruimte **Functiebeheer** en selecteert u de **Budgetregistervermeldingen voor alleen hoeveelheid** en/of **Budgetregistervermeldingen standaard van bedragtype**.

Met de functie **Budgetregistervermeldingen voor alleen hoeveelheid** kunt u een budgetregistervermelding met alleen hoeveelheden boeken. U kunt bijvoorbeeld een budgetregel boeken met een hoeveelheid van 32 en een prijs van nul, wat resulteert in een bedrag van nul. U kunt deze hoeveelheid vervolgens binnen de context van een financieel rapport gebruiken om een prijs per hoeveelheid te bepalen. U ziet dat er geen query's of rapporten zijn bijgewerkt als onderdeel van deze functie. Met deze functie kunt u alleen een bedrag van nul boeken.

De functie **Budgetregistervermeldingen standaard van bedragtype** maakt het mogelijk dat het standaard bedragtype binnen een budgetregistervermelding een ander bedragtype is dan onkosten. Voor de budgetregistervermeldingsregel wordt nu standaard onkosten gebruikt wanneer het hoofdrekeningtype onkosten is, wordt standaard opbrengst gebruikt als het hoofdrekeningtype onkosten is en wordt standaard onkosten gebruikt voor alle andere rekeningtypen.

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Werkruimten en querypagina's gebruiken om budget vs. werkelijk bij te houden
De budgetmanager kan de huidige status van een budget controleren in de werkruimte **Grootboekbudgetten en prognoses**. De tabbladen **Onkostenbudgetoverschrijding** en **Inkomsten onder budget** biedt een snelle weergave van de financiële dimensies waarin de budgetdoelen niet worden gehaald of de drempel benaderen. U kunt het budgetdrempelpercentage en de financiële dimensiesets personaliseren die op deze tabbladen worden gebruikt door op **Mijn werkruimte configureren** te klikken. U kunt klikken op **Beheerders van eenheden** om de werknemers weer te geven die voor specifieke financiële dimensiecombinaties verantwoordelijk zijn die op deze tabbladen zijn geselecteerd. Als u bijvoorbeeld ziet dat het onkostenbudget van de afdeling Bedrijfsactiviteiten over de budgetdrempel gaat, kunt u de manager van de afdeling Bedrijfsactiviteiten gemakkelijk vinden en contacteren om het probleem te bespreken. 

> [!NOTE] 
> Het veld **Afdelingsmanager** op de pagina **Organisatie-eenheden** bepaalt welke managers specifieke financiële dimensiecombinaties ondersteunen. Klik op **Meer weergeven** onder aan het tabblad om de querypagina **Budget vs. werkelijk** te openen voor meer informatie over budgetbedragen en werkelijke bedragen. 

Op de querypagina **Werkelijk vs. budget** kunt u inzoomen op de details de budgetbedragen in vergelijking met de werkelijke bedragen. Selecteer een regel op de querypagina, en klik vervolgens op **Periodesaldi** om budgetbedragen en werkelijke bedragen te bekijken verdeeld over boekperioden. De pagina **Budgetjournaalregels** bevat detailanalyse aan de details van het budgetbedrag in budgetregisterregels. De pagina **Algemeen journaalposten** opent de grootboektransacties die zijn opgenomen in het berekende bedrag voor **Werkelijke kosten**. 

Een bedrijf dat budgetplanningsfunctionaliteit gebruikt, kan *budgetprognoses* maken en gebruiken in de werkruimte **Grootboekbudgetten en prognoses**.



