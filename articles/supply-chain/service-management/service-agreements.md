---
title: Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen
description: Met serviceovereenkomsten kunt u de middelen opgeven die bij een standaardonderhoudsbezoek worden gebruikt en opgeven hoe die middelen aan de klant worden gefactureerd.
author: sorenva
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf28619e66fa5d3e86bdbb3838dc7f711916bcec
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905597"
---
# <a name="develop-and-establish-service-agreements-overview"></a>Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen

[!include [banner](../includes/banner.md)]

Met serviceovereenkomsten kunt u de middelen opgeven die bij een standaardonderhoudsbezoek worden gebruikt en opgeven hoe die middelen aan de klant worden gefactureerd.

Elke serviceovereenkomst is gekoppeld aan een project en via dit project worden transacties geboekt en gefactureerd. U kunt serviceordertransacties echter ook rechtstreeks via het project factureren, zonder dat u eerst de serviceorder aan een serviceovereenkomst hoeft te koppelen. U kunt dit doen als de serviceorder een serviceorder voor een eenmalig bezoek is en het verwerken van de servicetransacties belangrijker is dan de noodzaak om gedetailleerd de gegevens van de serviceovereenkomst voor de klant gedurende een bepaalde periode bij te houden.

## <a name="service-agreement"></a>Serviceovereenkomst

In elke serviceovereenkomst moet u een project, een serviceovereenkomst-ID en een serviceovereenkomstgroep opgeven. De serviceovereenkomstgroep kan worden gebruikt voor het sorteren en organiseren van serviceovereenkomsten.

De koptekst van een serviceovereenkomst bevat de instellingen die voor alle bijgevoegde serviceovereenkomstregels gelden:

-  Of de serviceovereenkomst is uitgesteld. Als de serviceovereenkomst is uitgesteld, kunt u geen serviceorders van de serviceovereenkomst genereren.
-  De duur van de serviceovereenkomst.
-  De manier waarop serviceorderregels in serviceorders moeten worden gecombineerd.
-  Of de serviceovereenkomst een sjabloon is.

In de kop van een serviceovereenkomst stelt u ook alle serviceobjecten en -taken in die met de serviceovereenkomst kunnen worden gebruikt. Daarvoor voert u de specifieke servicetaken of -objecten in die aan de diverse regels van de overeenkomst moeten worden gekoppeld.

Vanuit de koptekst van de serviceovereenkomst kunt u ook serviceovereenkomstregels of servicesjabloonregels naar de huidige serviceovereenkomst kopiëren.

U kunt serviceovereenkomsten uitstellen en afzonderlijke serviceovereenkomstregels stoppen.

Als u het selectievakje **Uitgesteld** voor een serviceovereenkomstregel inschakelt, bent u niet in staat om:

-    automatisch of handmatig serviceorders te maken op basis van de serviceovereenkomst.

Als u het selectievakje **Gestopt** voor een serviceovereenkomstregel inschakelt, bent u niet in staat om:

-    automatisch of handmatig serviceorders te maken op basis van de serviceovereenkomstregel.
-    de serviceovereenkomstregel te kopiëren naar een andere serviceovereenkomst of serviceorder.


> [!NOTE]
> Indien een serviceovereenkomst wordt uitgesteld, worden alle gekoppelde regels gestopt ongeacht de afzonderlijke status van deze regels.

## <a name="service-agreement-lines"></a>Serviceovereenkomstregels

Elke serviceovereenkomstregel beschrijft in detail de inhoud van het voorgestelde servicewerk. Deze regels bevatten de volgende instellingen:

-  Het transactietype en de omschrijving van het transactietype.
-  De werknemer die het servicewerk uitvoert.
-  De objecten waarop de service conform de serviceovereenkomst moet worden uitgevoerd.
-  De frequentie waarmee het werk wordt uitgevoerd, en bijhorende artikel-, onkosten- en bijzondere-kostentransacties worden geregistreerd.
-  Het tijdvenster waarbinnen serviceorderregels in een serviceorder kunnen worden gegroepeerd.
-  De servicetaken waarmee sets overeenkomstregels worden gegroepeerd in werktaken en waarmee voor servicemonteurs en klanten wordt samengevat welke servicetaak er dient te worden uitgevoerd.
-  Of een regel is geblokkeerd. Als een regel is geblokkeerd, kunt u voor die regel geen serviceorders maken.
-  Projectinstellingen zoals de categorie en de regeleigenschap.

## <a name="related-articles"></a>Gerelateerde artikelen

[Serviceovereenkomsten maken](create-service-agreements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]