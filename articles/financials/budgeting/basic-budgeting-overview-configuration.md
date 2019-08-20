---
title: Budgetteringsoverzicht
description: Bijna elk bedrijf dat gebruikmaakt van de functionaliteit Financiële items in Microsoft Dynamics 365 for Finance and Operations, moet rapporten kunnen maken van gebudgetteerde versus werkelijke waarden. In dit artikel wordt de minimale configuratie uitgelegd die nodig is om budgetten in Finance and Operation te kunnen maken of budgetten te kunnen laden vanuit een programma van derden.
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
ms.openlocfilehash: 9871d41c8e0c8f05acfd6618ca537a98ab0dd71b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834266"
---
# <a name="budgeting-overview"></a>Budgetteringsoverzicht 

[!include [banner](../includes/banner.md)]

Bijna elk bedrijf dat gebruikmaakt van de functionaliteit Financiële items in Microsoft Dynamics 365 for Finance and Operations, moet rapporten kunnen maken van gebudgetteerde versus werkelijke waarden. In dit artikel wordt de minimale configuratie uitgelegd die nodig is om budgetten in Finance and Operation te kunnen maken of budgetten te kunnen laden vanuit een programma van derden.

<a name="overview"></a>Overzicht
--------

Het goedgekeurde budget voor een rechtspersoon wordt beheerd in een document dat een *budgetregisterregel* wordt genoemd. De regels in een budgetjournaalpostdocument worden *budgetrekening*posten genoemd, en bevatten financiële dimensiegegevens, datums en de bedragen van het goedgekeurde budget. Het document met budgetjournaalposten is geïntegreerd met elementaire financiële rapporten en querypagina´s waarin werkelijke bedragen worden vergeleken met gebudgetteerde bedragen. 

Er zijn meerdere methoden om budgetjournaalposten te maken in Finance and Operations:

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

## <a name="using-workspaces-and-inquiry-pages-to-track-budget-vs-actuals"></a>Werkruimten en querypagina's gebruiken om budget vs. werkelijk bij te houden
De budgetmanager kan de huidige status van een budget controleren in de werkruimte **Grootboekbudgetten en prognoses**. De tabbladen **Onkostenbudgetoverschrijding** en **Inkomsten onder budget** biedt een snelle weergave van de financiële dimensies waarin de budgetdoelen niet worden gehaald of de drempel benaderen. U kunt het budgetdrempelpercentage en de financiële dimensiesets personaliseren die op deze tabbladen worden gebruikt door op **Mijn werkruimte configureren** te klikken. U kunt klikken op **Beheerders van eenheden** om de werknemers weer te geven die voor specifieke financiële dimensiecombinaties verantwoordelijk zijn die op deze tabbladen zijn geselecteerd. Als u bijvoorbeeld ziet dat het onkostenbudget van de afdeling Bedrijfsactiviteiten over de budgetdrempel gaat, kunt u de manager van de afdeling Bedrijfsactiviteiten gemakkelijk vinden en contacteren om het probleem te bespreken. 

> [!NOTE] 
> Het veld **Afdelingsmanager** op de pagina **Organisatie-eenheden** bepaalt welke managers specifieke financiële dimensiecombinaties ondersteunen. Klik op **Meer weergeven** onder aan het tabblad om de querypagina **Budget vs. werkelijk** te openen voor meer informatie over budgetbedragen en werkelijke bedragen. 

Op de querypagina **Werkelijk vs. budget** kunt u inzoomen op de details de budgetbedragen in vergelijking met de werkelijke bedragen. Selecteer een regel op de querypagina, en klik vervolgens op **Periodesaldi** om budgetbedragen en werkelijke bedragen te bekijken verdeeld over boekperioden. De pagina **Budgetjournaalregels** bevat detailanalyse aan de details van het budgetbedrag in budgetregisterregels. De pagina **Algemeen journaalposten** opent de grootboektransacties die zijn opgenomen in het berekende bedrag voor **Werkelijke kosten**. 

Een bedrijf dat budgetplanningsfunctionaliteit gebruikt, kan *budgetprognoses* maken en gebruiken in de werkruimte **Grootboekbudgetten en prognoses**.



