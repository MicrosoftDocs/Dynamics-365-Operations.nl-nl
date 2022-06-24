---
title: Wave-stapcodes
description: Dit artikel biedt een overzicht van wave-stapcodes en hoe deze worden gebruikt.
author: Mirzaab
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4d25f1211db949b38232f945f69f197d5eda9a11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900472"
---
# <a name="wave-step-codes"></a>Wave-stapcodes

[!include [banner](../includes/banner.md)]

Wave-stapcodes zijn codes die gebruikers kunnen instellen en gebruiken om specifieke instanties van wave-methoden aan een bijbehorende sjabloon te koppelen. De sjablonen bevatten sjablonen voor aanvulling, containers, afdrukken van etiketten, belasting bouwen en sorteren.

Wanneer er geen wave-stapcodes worden gebruikt, moeten gebruikers vrije tekst invoeren om naar een bepaalde sjabloon te verwijzen vanuit het wave-methode-exemplaar. Vrije tekst is gevoelig voor fouten, omdat gebruikers ervoor moeten zorgen dat de tekst met de wave-stap die zij toevoegen voor een specifieke wave-stapmethode in een wave-sjabloon exact overeenkomt met de tekst van de wave-stap in de doelsjabloon.

Wave-stapcodes voor een specifiek wave-staptype worden ingesteld op een afzonderlijke pagina. Voor elke wave-stapmethode-instantie in een wave-sjabloon waarvoor een wave-stapcode moet worden gebruikt, moet de wave-stapcode worden geselecteerd in een vervolgkeuzelijst. De selectie in een vervolgkeuzelijst vervangt vrije tekstinvoer en vermindert het risico en de impact van de menselijke fout. Met instellingscodes wordt een wave-stapmethode in een wave-sjabloon gekoppeld aan een doelsjabloon voor de methode.

> [!NOTE]
> Het gebruik van de functie voor wave-stapcodes is optioneel. Het is organisatiebreed ingeschakeld voor alle rechtspersonen.

## <a name="setup-demo"></a>Demo instellen 

Voor deze demo moeten demogegevens worden geïnstalleerd en moet u het **USMF**-voorbeeld-gegevensbedrijf gebruiken.

### <a name="enable-wave-step-codes"></a>Wave-stapcodes inschakelen

Voer de volgende stappen uit om de functie wave-stapcodes in te schakelen.

1. Ga naar **Functiebeheer**.
2. Schakel de functie **Organisatiebrede wave-stapcode inschakelen** in.

Alle bestaande vrije teksten uit de wave-stap in alle rechtspersonen worden bijgewerkt naar de nieuwe structuur. Nadat deze upgrade voor alle rechtspersonen is voltooid, wordt de functie ingeschakeld. Als de functie niet kan worden ingeschakeld voor een of meer rechtspersonen, wordt de functie voor geen enkele rechtspersoon ingeschakeld.

Tijdens het inschakelen worden validaties uitgevoerd tijdens de gegevensupgrade. Als de upgrade mislukt, wordt een foutbericht weergegeven. Een upgrade kan mislukken vanwege de volgende conflicten:

- Er zijn dubbele wave-stapteksten beschikbaar.
- Aanpassingen bestaan.
- Een wave-stapvrije tekst die is gekoppeld aan een instantie van de wave-stapmethode komt niet overeen met het verwachte sjabloontype.

Nadat u de conflicten die tijdens de validaties zijn geïdentificeerd hebt opgelost, kunt u de functie opnieuw proberen uit te voeren.

Wanneer de functie is ingeschakeld, wordt de pagina met **wave-stapcodes** (**Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes**) weer beschikbaar. Op deze pagina worden de wave-stapcodes weergegeven die zijn bijgewerkt toen de functie voor organisatiebrede wave-stapcodes werd ingeschakeld.

### <a name="create-new-wave-step-codes"></a>Nieuwe wave-stapcodes maken

U kunt de pagina **Wave-stapcodes** gebruiken om Wave-stapcodes te maken en te verwijderen.

Elke nieuwe wave-stapcode en de bijbehorende ID moeten uniek zijn binnen alle wave-staptypen en moeten worden gedefinieerd voor een specifiek wave-staptype.

### <a name="apply-wave-step-codes"></a>Wave-stapcodes toepassen

Nadat u de juiste wave-stapcodes hebt gedefinieerd, kunnen deze worden toegepast op de wave-procesmethoden.

Ga naar de gewenste doelsjabloon om wave-stapcodes toe te passen. Dit zijn de doelsjablonen waaraan de wave-stapcodes zijn toegewezen om naar toe te wijzen:

- **Aanvullingssjablonen:** Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen
- **Sjablonen voor lading samenstellen:** Magazijnbeheer \> Instellingen \> Lading \> Sjablonen voor lading samenstellen
- **Sorteersjablonen:** Magazijnbeheer \> Instellingen \> Verpakking \> Uitgaande Sorteersjablonen
- **Sjablonen voor containervorming:** Magazijnbeheer \> Instellingen \> Containers \> Sjablonen voor containerbouw
- **Sjablonen om etiketten af te drukken:** Magazijnbeheer \> Instellingen \> Documentroutering \> Wave-labelsjablonen

De sjablonen in deze lijst worden toegepast wanneer er wordt verwezen vanuit een wave-procesmethode die is geselecteerd in een wave-sjabloon. Wanneer de wave-stapcode van een wave-procesmethode in een wave-sjabloon overeenkomt met de wave-stapcode in een van de sjabloontypen, wordt de sjabloon toegepast.

### <a name="sample-scenario"></a>Voorbeeldscenario

Met de volgende procedure kunt u garanderen dat de aanvullingssjabloon die u hebt gemaakt voor de wave- sjabloon wordt toegepast.

1. Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-stapcodes** en maak een wave-stapcode for het type **Aanvulling**.
2. Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen** en maak een aanvullingssjabloon.
3. Selecteer in het aanvullingssjabloon de wave-stapcode die u voor het type **Aanvulling** hebt gemaakt.
4. Ga naar **Magazijnbeheer \> Instellingen \> Waves \> Wave-sjablonen** en selecteer de wave-sjabloon die u wilt gebruiken.
5. Selecteer in de sjabloon op het sneltabblad **Methoden** de methode **Aanvulling**.
6. Selecteer in het veld **Wave-stapcode** de wave-stapcode die u voor de aanvullingssjabloon hebt gemaakt.

U voert deze stappen uit voor elke rechtspersoon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]