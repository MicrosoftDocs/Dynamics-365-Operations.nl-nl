---
title: Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)
description: In dit artikel wordt de kostenconfiguratie voor Gedistribueerd orderbeheer (DOM) in Dynamics 365 Commerce beschreven.
author: josaw1
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9aaff8f627adcd00be174a0b5f7bd398300cfef9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862013"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a>Kostenconfiguratie voor Gedistribueerd orderbeheer (DOM)

[!include [banner](../includes/banner.md)]

Organisaties houden rekening met meerdere kostencomponenten om de optimale locatie te bepalen voor het afhandelen van een order. Deze kostencomponenten kunnen bestaan uit verzendkosten, afhandelingskosten en verpakkingskosten. Er wordt een berekening gemaakt van de combinatie van deze kosten om de afhandelingslocatie te bepalen.

Toen de toewijzing van orders aan afhandelingslocatie voor het eerst met Gedistribueerd orderbeheer (DOM) werd geoptimaliseerd in Dynamics 365 Commerce, werd alleen rekening gehouden met de afstand. Hoewel afstand kan samenhangen met kosten, is het niet hetzelfde als kosten. Het verzenden van producten in één dag is bijvoorbeeld duurder dan verzendmethoden over dezelfde afstand die drie of zeven dagen in beslag nemen.

Met de functie voor kostenconfiguratie kunnen detailhandelaren aanvullende kostencomponenten definiëren en configureren die worden berekend en meegenomen bij het bepalen van de optimale locatie voor het afhandelen van orderregels.

Wanneer kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie alleen gebruik van deze kostendefinities om de optimale locatie te bepalen voor het afhandelen van een order. De afstandcomponent wordt niet als een kostenpost beschouwd. Als er echter geen kostencomponenten worden geconfigureerd, maakt de DOM-oplossingsfunctie wel gebruik van de afstandscomponent als kostenpost om de optimale locatie te bepalen voor het afhandelen van een order.

## <a name="set-up-cost-components"></a>Kostencomponenten instellen

Er kunnen twee belangrijke kostencomponenttypen worden gedefinieerd in het systeem: **Verzending** en **Overig**.

Maar beide kostencomponenttypen ondersteunen meerdere berekeningsbases, zoals wordt getoond in de volgende tabel.

<table>
<thead>
<tr>
<th>Kostencomponenttype</th>
<th>Berekeningsbasis</th>
</tr>
</thead>
<tbody>
<tr>
<td>Verzenden</td>
<td>
<ul>
<li>Eenvoudig</li>
<li>Gelaagd</li>
</ul>
</td>
</tr>
<tr>
<td>Overig</td>
<td>
<ul>
<li>Verkooporder</li>
<li>Verkoopregel</li>
<li>Locatie</li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a>Kostencomponenttype voor verzending

In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype **Verzending** en de berekeningsbasis voor de verzendkosten kunt instellen. Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a>Kostencomponenttype = Verzending en Berekeningsbasis = Eenvoudig

Als een combinatie van het kostencomponenttype **Verzending** en de berekeningsbasis **Eenvoudig** wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand.

U moet de volgende velden instellen voor deze combinatie:

- **Kostenfactor**: voer een unieke id voor de kostenfactor in.
- **Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.
- **Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik. Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.
- **Actief**: geef aan of de kostenfactor actief is. In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.
- **Bedrijf**: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd. Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.
- **Leveringsmethoden**: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.
- **Berekeningstype**: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode. Er worden twee berekeningstypen ondersteund:

    - **Vast**: er wordt een standaardtarief gebruikt voor de leveringsmethode. Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld **Kosten**.
    - **Per afstandseenheid**: de kosten voor de leveringsmethode worden berekend als de waarde die is opgegeven in het veld **Kosten** maal de afstand tussen het afleveradres en de locaties.

- **Kosten**: geef de waarde op die wordt gebruikt in combinatie met het veld **Berekeningstype** om de kosten voor de leveringsmethode te berekenen.

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a>Kostencomponenttype = Verzending en Berekeningsbasis = Gelaagd

Als een combinatie van het kostencomponenttype **Verzending** en de berekeningsbasis **Gelaagd** wordt gebruikt, zijn de verzendkosten voor een leveringsmethode gebaseerd op een vast tarief of afstand. In deze combinatie is de afstand echter gebaseerd op een gelaagd bereik met afstanden.

U moet de volgende velden instellen voor deze combinatie:

- **Kostenfactor**: voer een unieke id voor de kostenfactor in.
- **Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.
- **Standaardkosten**: geef de kosten op voor een leveringsmethode als de afstand tussen het afleveradres en de locatie niet binnen een van de gelaagde afstanden voor de leveringsmethode vast.
- **Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik. Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.
- **Actief**: geef aan of de kostenfactor actief is. In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.
- **Bedrijf**: geef de rechtspersoon op waarvoor de kostenfactor wordt geconfigureerd. Alle regels van de berekeningscriteria moeten gelden voor dezelfde rechtspersoon.
- **Leveringsmethoden**: geef de leveringsmethoden op waarvoor de kostenfactor wordt geconfigureerd.
- **Afstandstype**: geef op of de gelaagde afstandsdefinitie een afstand hemelsbreed is of over de weg.
- **Afstandseenheden**: geef de eenheid op waarin de gelaagde afstand wordt gemeten.
- **Afstand van**: geef het beginbereik van de gelaagde afstand op.
- **Afstand tot**: geef het eindbereik van de gelaagde afstand op.
- **Berekeningstype**: geef op hoe de kosten moeten worden berekend voor een specifieke leveringsmethode en de gelaagde afstand. Er worden twee berekeningstypen ondersteund:

    - **Vast**: er wordt een standaardtarief gebruikt voor de leveringsmethode. Als u dit berekeningstype selecteert, wordt het standaardtarief gedefinieerd in het veld **Kosten**.
    - **Per afstandseenheid**: de kosten voor de leveringsmethode en de gelaagde afstand worden berekend als de waarde die is opgegeven in het veld **Kosten** maal de afstand tussen het afleveradres en de locaties.

- **Kosten**: geef de waarde op die wordt gebruikt in combinatie met het veld **Berekeningstype** om de kosten voor de leveringsmethode te berekenen.

> [!NOTE]
> - Wanneer u gelaagde afstanden definieert, wordt door het systeem gecontroleerd of er geen ontbrekende of overlappende afstanden zijn.
> - Het afstandstype dat voor een leveringsmethode wordt gebruikt moet hetzelfde zijn voor alle gelaagde afstanden.

### <a name="other-cost-component-type"></a>Kostencomponenttype Overig

In deze sectie wordt uitgelegd hoe u de verschillende combinaties van het kostencomponenttype **Overig** en een overig kostentype voor niet-verzendkosten kunt instellen. Ook wordt uitgelegd hoe de DOM-oplossingsfunctie deze combinaties toepast.

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a>Kostencomponenttype = Overig en Overig kostentype = Verkooporder

Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Verkooporder** wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporder.

U moet de volgende velden instellen voor deze combinatie:

- **Kostenfactor**: voer een unieke id voor de kostenfactor in.
- **Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.
- **Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik. Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.
- **Actief**: geef aan of de kostenfactor actief is. In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.
- **Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporder.

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a>Kostencomponenttype = Overig en Overig kostentype = Verkoopregel

Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Verkoopregel** wordt gebruikt voor het definiëren van niet-verzendkosten op het niveau van de verkooporderregel.

U moet de volgende velden instellen voor deze combinatie:

- **Kostenfactor**: voer een unieke id voor de kostenfactor in.
- **Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.
- **Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik. Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.
- **Actief**: geef aan of de kostenfactor actief is. In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.
- **Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de verkooporderregel.

#### <a name="cost-component-type--other-and-other-cost-type--location"></a>Kostencomponenttype = Overig en Overig kostentype = Locatie

Een combinatie van het kostencomponenttype **Overig** en het overige kostentype **Locatie** wordt gebruikt voor het definiëren van niet-verzendkosten voor een groep van locaties of een individuele locatie.

U moet de volgende velden instellen voor deze combinatie:

- **Kostenfactor**: voer een unieke id voor de kostenfactor in.
- **Beschrijving**: voer de naam en de omschrijving van de kostenfactor in.
- **Begindatum** en **Einddatum**: met deze velden kunt u de kostenfator beperken tot een specifiek datumbereik. Als u deze velden leeg laat, is de kostenfactor voor een onbepaalde periode.
- **Actief**: geef aan of de kostenfactor actief is. In Gedistribueerd orderbeheer wordt alleen rekening gehouden met actieve kostenfactoren die aan het afhandelingsprofiel zijn gekoppeld.
- **Afhandelingsgroep**: geef de groep met locaties op waarvoor de niet-verzendkosten worden gedefinieerd.
- **Afhandelingslocatie**: geef de locatie op waarvoor de niet-verzendkosten worden gedefinieerd.

    > [!NOTE]
    > U kunt niet op dezelfde regel een afhandelingsgroep en een afhandelingslocatie opgeven voor op locatie gebaseerde berekeningscriteria.

- **Kosten**: geef de kostenwaarde op voor niet-verzendkosten op het niveau van de afhandelingsgroep of de afhandelingslocatie.

> [!IMPORTANT]
> Voordat deze kosten in Gedistribueerd orderbeheer (DOM) worden meegenomen, moet u de kostenfactor toevoegen aan het relevante afhandelingsprofiel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]