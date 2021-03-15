---
title: Overtredingen van controlebeleid en aanvragen
description: In dit artikel wordt beschreven hoe controleaanvragen worden gegenereerd voor overtredingen van controlebeleidsregels. Het bevat ook informatie over de verschillende manieren waarop door controlebeleid wordt gebruikgemaakt van het datumbereik voor documentselectie.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ddd403bfe82b1a7d3c0c5999f89bde19f1bba5e8
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022100"
---
# <a name="audit-policy-violations-and-cases"></a>Overtredingen van controlebeleid en aanvragen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe controleaanvragen worden gegenereerd voor overtredingen van controlebeleidsregels. Het bevat ook informatie over de verschillende manieren waarop door controlebeleid wordt gebruikgemaakt van het datumbereik voor documentselectie.

<a name="how-audit-cases-are-generated"></a>De controleaanvragen worden gegenereerd.
-----------------------------

Controlebeleidsregels worden gebruikt voor het identificeren van onkostennota's, inkooporders en leveranciersfacturen die niet aan de bedrijfsregels voldoen die u definieert en configureert als controlebeleidsregels. 

Controlebeleid moet in batchmodus worden uitgevoerd. Wanneer u een controlebeleid uitvoert, worden alle beleidsregels van het beleid tegelijkertijd uitgevoerd.

Met elke beleidsregel wordt een set documenten geëvalueerd. Met de beleidsregel worden documenten geselecteerd die zich binnen het datumbereik van de documentselectie bevinden en die voldoen aan opgegeven criteria. Eén beleidsregel kan bijvoorbeeld onkostennota's selecteren met maaltijden van meer dan 50. Met een andere beleidsregel kunnen leveranciersfacturen worden geselecteerd die aan een specifieke leverancier moeten worden betaald. Voor elk document dat in de set is geselecteerd, wordt een overtreding gegenereerd. De overtreding is een record waarmee wordt aangegeven dat een bepaald document, zoals factuur 12345, niet voldoet aan de beleidsregel. 

Meerdere controleschendingsregistraties worden gegroepeerd en aan controleaanvragen gekoppeld. Aanvragen voor elk controlebeleid worden standaard op basis van controlebeleidsregel gegroepeerd. Desgewenst kunt u andere groeperingscriteria selecteren met behulp van de pagina **Casegroeperingscritertia**. U kunt bijvoorbeeld kopteksten van onkosten groeperen op project-ID en leveranciersfacturen op leverancierrekening. In dit geval worden alle overtredingen van kopteksten van onkosten met dezelfde project-ID in dezelfde aanvraag gegroepeerd, en worden alle leverancierfacturen met dezelfde leverancierrekening in dezelfde aanvraag gegroepeerd. 

> [!NOTE]
> Bij controlebeleidsregels die zijn gebaseerd op het querytype **Duplicaat**, worden overtredingen niet gegroepeerd op beleidsregel of op de criteria die zijn opgegeven op de pagina **Casegroeperingscriteria**. In plaats daarvan worden ze gegroepeerd op de criteria in de controlebeleidsregel. Als met een beleidsregel bijvoorbeeld onkostennota's worden geëvalueerd voor dubbele onkosten met hetzelfde bedrag, dezelfde verkopers-ID en datum, zijn alle onkosten met dezelfde waarden in deze velden onderdeel één aanvraag. Alle onkosten met andere waarden vormen een andere aanvraag.

Nadat de controleaanvragen zijn gegenereerd, worden ze verwerkt met de normale processen voor aanvraagbeheer.

## <a name="document-selection-date-ranges"></a>Datumbereiken van de documentselectie
Wanneer een controlebeleid wordt uitgevoerd, worden met elke beleidsregel documenten van het opgegeven type geselecteerd met een datum binnen het datumbereik voor documentselectie. Het datumbereik voor documentselectie wordt opgegeven op de pagina **Extra opties** . Aan veel documenten is meer dan een datum gekoppeld. Het datumveld dat wordt gebruikt voor de controlebeleidsregel, wordt opgegeven op de pagina **Beleidsregeltype**.

Hier vindt u enkele andere manieren waarop het datumbereik voor documentselectie voor een controlebeleid wordt gebruikt:

-   In het beleid wordt de versie van elke beleidsregel gebruikt die geldig is op de laatste dag van het datumbereik voor documentselectie. U kunt de ingangsdatums weergeven voor elke beleidsregel op de lijstpagina **Controlebeleid**.
-   Het beleid gebruikt de organisatieknooppunten die aan het beleid zijn gekoppeld op de laatste dag van het datumbereik voor documentselectie. Alleen de organisatieknooppunten die momenteel aan het beleid zijn gekoppeld, worden weergegeven op de lijstpagina **Controlebeleid** .
-   Voor beleidsregels die zijn gebaseerd op het querytype **Zoeken in lijst**, worden met het beleid documenten geëvalueerd voor gecontroleerde entiteiten die geldig zijn op de laatste dag van het datumbereik voor documentselectie.


Zie [Controlebeleidsregels](audit-policy-rules.md) voor meer informatie.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]