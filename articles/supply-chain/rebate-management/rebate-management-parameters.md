---
title: Parameters voor kortingsbeheer
description: In dit onderwerp wordt de pagina Kortingsbeheerparameters beschreven. Deze pagina bevat instellingen die van invloed zijn op boeking, statusupdates, nummerreeksen en ander gedrag.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TAMRebateParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: a0a3bad751aba4f138db7fdae069a67a4faed4a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839096"
---
# <a name="rebate-management-parameters"></a>Parameters voor kortingsbeheer

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

De pagina **Kortingsbeheerparameters** wordt gebruikt om instellingen te definiëren die van toepassing zijn op de module **Kortingsbeheer**. Deze instellingen zijn van invloed op boeking, statusupdates, nummerreeksen en ander gedrag. De instellingen op deze pagina worden gedeeld tussen rechtspersonen en kunnen worden gewijzigd door gebruikers die over de juiste beveiligingsmachtigingen beschikken.

Als u de pagina **Kortingsbeheerparameters** wilt openen, gaat u naar **Kortingen en inhoudingen \> Instellen \> Kortingsbeheerparameters**. Stel vervolgens de velden in volgens de beschrijving in de volgende subsecties.

## <a name="rebate-management-tab"></a>Tabblad Kortingsbeheer

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het tabblad **Kortingsbeheer** van de pagina **Kortingsbeheerparameters**.

| Veld | Beschrijving |
|---|---|
| Standaardstatus | Selecteer de standaardstatus voor alle nieuwe deals. Als u de set statuswaarden wilt definiëren die beschikbaar is voor selectie, gebruikt u de [pagina **Kortingsstatussen**](rebate-statuses.md). |
| Verwerken per dimensie | Selecteer of voorzienings-, kortings- en afschrijvingstransacties per financiële dimensie moeten worden verwerkt. Wanneer deze optie is ingeschakeld, gebruikt het systeem financiële dimensies voor de brontransacties. |
| Controleren of deze eerder is geboekt | <p>Selecteer het systeemgedrag als niet-geboekte kortingstransacties meer dan één keer voor dezelfde periode worden verwerkt:</p><ul><li>**Waarschuwing**: het systeem staat gebruikers toe de oorspronkelijke transactieregels te overschrijven, maar er wordt wel een waarschuwing weergegeven.</li><li>**Fout**: het systeem voorkomt dat gebruikers de oorspronkelijke transactieregels overschrijven en er wordt een foutbericht weergegeven. |
| Automatisch journalen boeken | Selecteer of het systeem voorgestelde journalen automatisch moet boeken. Deze journalen bevatten dagelijkse journalen die worden gebruikt voor voorzieningen en klantinhoudingen, en ook journalen voor leveranciersbelastingfacturen. |
| Automatisch vrije-tekstfacturen boeken | Selecteer of het systeem automatisch vrije-tekstfacturen moet boeken. Deze optie is alleen van toepassing op vrije-tekstfacturen waarbij het betalingstype is ingesteld op *Klantinhoudingen voor belastingfacturen*. |
| Verwijzing kortingsartikelorder | Selecteer de kortingsverwijzing die moet worden gebruikt voor verkoop- en inkooporders die worden gegenereerd uit het kortingsproces (*Geen*, *Kortings- en inhoudingsdeal*, *Kortings- en inhoudingsnummer*, *Kortingstransactienummer* of *Documentnotities*). |
| Claimproces gebruiken | <p>Stel deze optie in op *Ja* om een claimproces te gebruiken. Op deze manier kunt u transacties die door Kortingsbeheer worden gemaakt markeren als geclaimd of niet-geclaimd en vervolgens alleen de geclaimde transacties boeken.</p><p>U berekent bijvoorbeeld kortingen voor een maand aan transacties, maar de klant heeft twee dagen niet geclaimd. In dit geval worden de niet-geclaimde transacties opnieuw gemaakt de volgende keer dat u de functie *Verwerken* uitvoert voor dezelfde periode.</p><p>Als u deze optie instelt op *Nee*, worden alle claimtransacties geboekt.</p> |
| Ordertypejournaal opnemen | Voor deals of dealregels waarbij het transactietype is ingesteld op *Order*, bepaalt deze optie of een verkooporder van het type *Journaal* moet worden opgenomen. Het biedt flexibiliteit als deze typen orders worden gebruikt in scenario's waarin een korting nog niet van toepassing zou moeten zijn. |

## <a name="number-sequences-tab"></a>Tabblad Nummerreeksen

Gebruik het tabblad **Nummerreeksen** op de pagina **Kortingsbeheerparameters** om nummerreekscodes toe te wijzen aan de verschillende nummerreeksen die door Kortingsbeheer worden gebruikt. In de volgende tabel wordt het doel van elk van deze nummerreeksen beschreven. Zie [Overzicht van nummerreeksen](../../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md) en gerelateerde onderwerpen voor meer informatie over nummerreeksen.

| Verwijzing | Beschrijving |
|---|---|
| Kortings- en inhoudingendeal | De nummerreeks wijst een unieke sleutelwaarde toe aan elke kortingsdeal. Deze sleutel wordt gebruikt wanneer deals worden gemaakt. |
| Kortings- en inhoudingsnummer | De nummerreeks wijst een unieke sleutelwaarde toe aan elke korting. Deze sleutel wordt gebruikt om kortingsrelaties te identificeren. |
| Kortingstransactienummer | De nummerreeks wijst een unieke sleutelwaarde toe aan elke kortingstransactie. Deze sleutel wordt gebruikt om kortingstransacties te identificeren. |
| Belastingfactuur | De nummerreeks wijst een unieke sleutelwaarde toe aan elke kortingsfactuur. Deze sleutel wordt gebruikt wanneer kortingsjournalen automatisch worden geboekt. |

## <a name="feature-visibility-tab"></a>Tabblad Functiezichtbaarheid

Met Kortingsbeheer worden functies (velden en functies) aan meerdere gebruikte pagina's in Microsoft Dynamics 365 Supply Chain Management toegevoegd. Deze pagina's bevatten pagina's die betrekking hebben op verkooporders en verkoopdeals. Als u Kortingsbeheer gebruikt, moet u deze functies overal zichtbaar maken voordat u hiervan kunt profiteren. Als u Kortingsbeheer niet gebruikt, kunt u de functies verbergen.

Stel op het tabblad **Functiezichtbaarheid** van de pagina **Kortingsbeheerparameters** de optie **Activeren** in op *Ja* om de functies voor Kortingsbeheer zichtbaar te maken op locaties waar deze beschikbaar zijn. Stel de optie in op *Nee* om de functies op gemeenschappelijke pagina's buiten de module **Kortingsbeheer**. Zelfs wanneer de optie is ingesteld op *Nee*, blijft de module zelf, inclusief de pagina **Kortingsbeheerparameters**, beschikbaar voor gebruikers die over de passende toegangsmachtigingen beschikken.
