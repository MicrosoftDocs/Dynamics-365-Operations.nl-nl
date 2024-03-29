---
title: Power BI-inhoud onkostenbeheer
description: In dit artikel wordt beschreven wat is opgenomen in het Power BI-inhoudpakket voor onkostenbeheer.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 78ae444c1c9803ed3708d71da7a359667df0252f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878308"
---
# <a name="expense-management-power-bi-content"></a>Power BI-inhoud onkostenbeheer

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven wat is opgenomen in de Power BI-inhoud voor onkostenbeheer. 

## <a name="overview"></a>Overzicht
Twee Power BI-inhoudpakketten zijn beschikbaar voor gebruik met onkostenbeheer in versie 8.1 en hoger. 
- Er is een persoonlijk dashboard ontworpen voor werknemers die onkostennota's indienen. 

  Het dashboard is erop afgestemd om belangrijke informatie te verschaffen aan personen over niet-ingediende en ingediende bedragen, alsmede historie en inzichten in onkostentransactiehistorie. Het persoonlijke dashboard is één pagina met de belangrijkste informatie voor de gebruiker.

- Er is een beheerdashboard ontworpen voo medewerkers en managers van de afdeling crediteuren. Het dashboard is erop afgestemd om rapportage voor totale onkosten van werknemers bij te houden en te rapporteren. Het dashboard biedt belangrijke metrische onkostengegevens , zoals niet-ingediende onkosten, reiskosten en gemiddelde declaratiebedragen. In het dashboard worden transactiegegevens gebruikt en het bevat samengevoegde weergaven van onkostenbeheer voor alle bedrijven. Het biedt ook een onderverdeling per werknemer met de optie om gegevens van financiële dimensies toe te voegen. De onkostenanalyse-inhoud voor beheer bevat: 
  - Een overzichtspagina met belangrijke metrische gegevens over onkostenbedragen en inzichten in concepten, in processen en voltooide onkostennota's. 
  - Een pagina met werknemersstatistieken om afzonderlijke details over een werknemer te bekijken op basis van tijd, kostentype en statistiekengroep. 
  - Een werknemersvergelijkingspagina om meerdere werknemers in de loop van de tijd te vergelijken. 

Alle bedragen worden weergegeven in de bedrijfsvaluta. Gegevens voor alle bedrijven worden weergegeven, maar indien nodig kunt u een bedrijfsfilter toevoegen. 

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
U vindt de Power BI-inhoud Admin Dashboard.pbix en Expense Personal Dashboard.pbix in de bibliotheek met gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). Zie voor meer informatie over hoe u de inhoud downloadt en in uw organisatie implementeert [Power BI-inhoud in LCS van Microsoft en uw partners](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).
De inhoud is beschikbaar via de werkruimte voor onkostenbeheer als ingesloten Power Bi-inhoud. Elke onkosteneigenaar kan toegang verkrijgen tot persoonlijke onkosten van zichzelf, terwijl alleen medewerkers en managers van de afdeling Crediteuren toegang hebben tot de beheerinhoud om onkostengegevens van alle gebruikers te bekijken.

## <a name="refreshing-the-power-bi-content"></a>De Power BI-inhoud vernieuwen
Voor de Power BI-inhoud van onkostenbeheer moet de maateenheid TrvBiExpenseMeasurement en budgetActivityMeasure worden vernieuwd via de entiteitsopslag. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Metrische gegevens die zijn opgenomen in de Power BI-inhoud
De inhoud bevat een reeks rapportpagina's. Elke pagina bestaat uit een set metrische gegevens die worden gevisualiseerd als diagrammen, tegels en tabellen. In de volgende tabel vindt u een overzicht van de visualisaties in de Power BI-inhoud.

**Analyses van persoonlijke onkosten**

| Rapportpagina | Visualisatie                             |
|-------------|-------------------------------------------|
| Mijn uitgaven | Bedrag van kilometerstand                         |
|             | Onkostennota's in behandeling                |
|             | Nr. van niet-ingediende onkosten               |
|             | Persoonlijke onkosten die moeten worden betaald              |
|             | Niet-ingediend bedrag                        |
|             | Ingediend bedrag                          |
|             | Bedrag in afwachting van vergoeding             |
|             | Onkostennota's met bedragen en status   |
|             | Ingediende maar niet-goedgekeurde onkostennota's  |
|             | Onkosten per kostentype                     |
|             | Onkosten per verkoper                      |
|             | Onkosten per verwerkte onkosten            |
|             | Onkosten per project                       |
|             | Totaal transactiebedrag in de loop van de tijd        |

**Beheeronkostenanalyses**

| Rapportpagina         | Visualisatie                           |           
|---------------------|-----------------------------------------|
| Onkostenoverzicht    | Conceptonkostenbedrag                   |
|                     | Aantal conceptonkostenregels           |
|                     | Conceptonkostenregels                     |
|                     | Beleidsschendingen onkostennota        |
|                     | Uitstaand bedrag                      |
|                     | Ingediende maar niet-goedgekeurde onkosten       |
|                     | Goedgekeurde onkosten                       |
|                     | Totaal bedrag onkosten                    |
|                     | Overzicht van onkostennota's                |
|                     | Onkosten per kostentype                   |
|                     | Onkosten per verkoper                    |
|                     | Onkosten per werknemer                   |
|                     | Onkosten versus project                     |
| Werknemersvergelijking | Onkostenbedragen                         |
|                     | Onkostenbedragen in de loop van de tijd per werknemer   |
| Werknemersstatistieken | Onkostennota´s per kostentype            |
|                     | Persoonlijke onkosten                       |
|                     | Onkostennota´s per statistiekengroep     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]