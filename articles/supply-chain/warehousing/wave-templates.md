---
title: Wavesjablonen
description: In dit onderwerp wordt het instellen van de criteria beschreven die bepalen of de waves handmatig of automatisch worden verwerkt, en het werk dat wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: aca03e3fda4405fa6fe2b427a47066af5bb95b644b7f5b47d22736347208a8bd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751620"
---
# <a name="wave-templates"></a>Wavesjablonen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt het instellen van de criteria beschreven die bepalen of de waves handmatig of automatisch worden verwerkt, en het werk dat wordt gegenereerd voor een magazijn wanneer een wave wordt verwerkt. U kunt de criteria bepalen door wavesjablonen en query's in te stellen die overeenstemmen met een wave met vrijgegeven regels in verkooporders, productieorders en kanbans.

## <a name="settings-for-wave-templates"></a>Instellingen voor wavesjablonen

Wanneer u een wavesjabloon instelt, bepaalt u het volgende:

- De **site** en het **magazijn** waarvoor de sjabloon werk zal maken.
- De volgorde waarin de sjablonen worden geëvalueerd. De volgorde waarin de sjablonen aan vrijgegeven regels op verkooporders, productieorders en kanbans worden gekoppeld. Wanneer een regel wordt vrijgegeven, past het systeem de eerste wavesjabloon toe waarvoor de regel aan de criteria voldoet. Hoe breder de criteria, hoe groter de kans dat een regel aan de criteria voldoet, dus u moet de sjablonen met de meest specifieke criteria boven aan de lijst plaatsen. Gebruik de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** in het actievenster om sjablonen te rangschikken in de lijst.
- De acties die door elke sjabloon worden uitgevoerd. De **wavemethoden** voeren de acties uit die door de sjabloon zijn gemaakt, zoals het maken of verdelen van werk voor elk type wavesjabloon.
- De wavekenmerken (filters) die moeten worden toegepast voor het gebruik van de wavesjabloon.

> [!NOTE]
> Indien nodig kan een ontwikkelaar extra methoden maken. U kunt de volledige lijst met methoden bekijken op de pagina **Methoden voor verwerking van waves**.

Sommige instellingen vertegenwoordigen strategische beslissingen voor waveverwerking als volgt:

- Als de sjabloon voor het verzenden van artikelen voor verkooporders en overboekingsorders wordt gebruikt of voor het verplaatsen van artikelen naar productie voor productieorders of kanbans.
- Als een wave handmatig of automatisch wordt verwerkt, als volgt:

  - **Handmatige verwerking**: de regel wordt toegevoegd aan een wave en de voorraad word gereserveerd. U moet echter klikken op **Verwerken** op de lijstpagina **Alle waves** om het orderverzamelwerk voor de order te maken.
  - **Automatische verwerking**: u kunt waveverwerking volledig of gedeeltelijk automatiseren. Als u waveverwerking volledig automatiseert, wordt een wave gemaakt die de regel van de verkooporder, de productieorder of de kanban omvat wanneer een verkooporder, een productieorder of een kanban wordt gemaakt. De artikelen worden afgetrokken van voorhanden voorraad en het orderverzamelwerk wordt gemaakt. Als u de waveverwerking automatiseert, kunt u waarden opgeven die de waveverwerking activeren. U kunt bijvoorbeeld een maximumgewicht opgeven voor zendingen die waveverwerking activeren wanneer het totale gewicht van regels in de wave de waarde bereikt.

- Als u zendingen toewijst aan een open wave. Als u bijvoorbeeld klanten belooft dat een order dat middernacht wordt geplaatst, binnen de 24 uur wordt verzonden, kunt u de wavesjabloon instellen om automatisch orderregels toe te wijzen aan een open wave tot middernacht. Op dat moment wordt de wave automatisch verwerkt.

Wanneer een wave wordt verwerkt, wordt het orderverzamelwerk dat is gemaakt, gebaseerd op de werksjabloon en de locatierichtlijn die is opgegeven voor het magazijn. De werksjabloon bepaalt hoe het orderverzamelwerk wordt gemaakt, en de locatierichtlijn bepaalt de orderverzamel- en neerzetlocaties.

## <a name="create-a-wave-template"></a>Een wavesjabloon maken

Ga als volgt te werk om een wavesjabloon in te stellen:

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Waves** \> **Wavesjablonen**.
1. Selecteer **Nieuw** om een nieuwe wavesjabloon te maken.
1. Selecteer in het veld **Wavesjabloontype** een van de volgende opties:

    - *Zending*: gebruik de wavesjabloon voor het verzenden van artikelen voor verkooporders en overboekingsorders.
    - *Productieorders*: gebruik de wavesjabloon om artikelen voor productieorders te verplaatsen.
    - *Kanban*: gebruik de wavesjabloon om artikelen voor kanbanorders te verplaatsen.

1. Voer in de velden **Naam van wavesjabloon** en **Beschrijving van wavesjabloon** een naam en een beschrijving in voor de wavesjabloon.

    > [!NOTE]
    > Als meer dan één sjabloon voor een magazijn is gemaakt, geeft het nummer in het veld **Volgorde wavesjabloon** de positie van de sjabloon weer in de volgorde waarin de sjablonen worden toegepast wanneer wordt voldaan aan de criteria van de sjabloon. Indien nodig u **Omhoog** of **Omlaag** selecteren om de volgorde van de reeks sjablonen te wijzigen.

1. Selecteer in de velden **Site** en **Magazijn** de site en het magazijn waarvoor de wavesjabloon waves en orderverzamelwerk zal maken.
1. Als u de waveverwerking wilt automatiseren, voert u indien nodig de volgende instellingen uit:

    - **Het maken van waves automatiseren**: stel dit in op *Ja* om automatisch een wave te maken wanneer een verkooporder, een productieorder of een kanban aan het magazijn wordt vrijgegeven.
    - **Toewijzen aan open waves**: stel dit in op *Ja* om automatisch regels toe te wijzen aan een open wave wanneer de regels worden vrijgegeven. Regels worden toegewezen aan waves op basis van het queryfilter voor de wavesjabloon.
    - **Wave verwerken bij vrijgave door magazijn**: stel dit in op *Ja* om de wave automatisch te verwerken en werk te maken wanneer een regel naar het magazijn wordt vrijgegeven.
    - **Wave automatisch verwerken op drempel**: stel dit in op *Ja* om de wave automatisch te verwerken wanneer de waarden de drempels bereiken voor gewicht, verzending en regels bepaald in de veldgroep **Wavedrempels**. Deze instelling is alleen actief als *Verzending* is geselecteerd in het veld **Type wavesjabloon**.
    - **Vrijgave wave automatiseren**: stel dit in op *Ja* om de wave automatisch vrij te geven. Het orderverzamelwerk wordt gemaakt en wordt beschikbaar op mobiele apparaten.
    - **Vrijgave van aanvullingswerk automatiseren**: stel dit in op *Ja* om op vraag gebaseerd aanvullingswerk te maken en dit automatisch vrij te geven. U moet de methode van de aanvullingswave toevoegen aan de wavesjabloon en een aanvullingssjabloon maken met het type *Waveaanvraag*. Stel een aanvullingssjabloon in de pagina **Aanvullingssjablonen** in. Hiervoor moet u de aanvul methode toevoegen aan de wavesjabloon.
    - **Doorgaan met verwerken van wave als het maken van werk mislukt**: wanneer deze optie is ingeschakeld op *Ja*, wordt een lege locatie gebruikt als er geen voorraad kan worden gereserveerd op de locatie die wordt voorgesteld door de locatierichtlijn (bijvoorbeeld omdat de voorraad niet meer beschikbaar is). Als deze optie is ingesteld op *Nee*, mislukt de wave als het systeem de voorraad niet kan reserveren.

1. Stel indien nodig de veldgroep **Wavedrempels** in:
    - **Drempelwaarde voor wave**: voer het maximale gewicht in dat een wave kan bevatten.
    - **Verzenddrempel**: voer het maximum aantal zendingen in dat in een wave kan worden opgenomen.
    - **Regeldrempel**: voer het maximum aantal regels in dat in een wave kan worden opgenomen.

1. Selecteer in de veldgroep **Standaardwaarden** de wavekenmerken als extra criteria voor de wavesjabloon. Wavekenmerken zijn nuttig om extra criteria toe te wijzen, zoals een specifieke klantnaam, aan een wavesjabloon. U maakt deze kenmerken op de pagina **Wavekenmerken**. 

1. Stel **Beleid voor wavemeldingen** in op het beleid dat u wilt gebruiken voor het genereren van meldingen met betrekking tot waves die deze sjabloon gebruiken. Zie [Wave-uitvoeringsmeldingen](wave-execution-notifications.md) voor een voorbeeld van een beleid voor wavemeldingen.

1. Op het sneltabblad **Methoden** toont het deelvenster **Geselecteerde methoden** de methoden voor het geselecteerde type wavesjabloon. De wavemethoden voeren de acties uit die door de sjabloon zijn gemaakt, zoals het maken of verdelen van werk. Deze acties worden ook wel wavestappen genoemd. Wavemethoden zijn vooraf gedefinieerd voor elk type wavesjabloon. U kunt de vooraf gedefinieerde wavemethoden niet verwijderen, maar u kunt de volgorde van de methoden herordenen en extra methoden toevoegen. Als u bijvoorbeeld een wavesjabloon maakt voor verzenden, kunt u methoden toevoegen voor aanvulling en het maken van containers. Wavecontainervorming kan aan een reeks van wavemethoden worden toegevoegd om het maken van containers te definiëren voor de regels die in een wavesjabloon worden verwerkt. Ga als volgt te werk om een aanvullende methode toe te voegen:

    - Selecteer een methode in het deelvenster **Resterende methoden** en selecteer vervolgens de **pijl naar links** om de methode toe te voegen aan het deelvenster **Geselecteerde methoden**.
    - Als u de volgorde wilt wijzigen, selecteert u een methode en selecteert u vervolgens de pijlen **Omhoog** of **Omlaag**.

    > [!NOTE]
    > Wanneer u een methode toevoegt, wordt deze automatisch weergegeven op de juiste locatie in de reeks stappen.

1. Als u de query wilt instellen die overeenkomt met vrijgegeven regels met een geschikte wave, selecteert u **Query bewerken** in het actievenster.
1. Als u wilt verifiëren dat de instellingen van de wavesjabloon geldig zijn, selecteert u **Sjabloon valideren**.
