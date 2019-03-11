---
title: Servicetaken
description: Met servicetaken kunt de taken omschrijven die voor een serviceorder moeten worden voltooid. Zowel technici als klanten kunnen deze informatie bekijken.
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2538a7b4a4c13a299afb37dd336f2f5d6f36a23
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "308593"
---
# <a name="service-tasks"></a>Servicetaken  

[!include [banner](../includes/banner.md)]

Met servicetaken kunt de taken omschrijven die voor een serviceorder moeten worden voltooid.
Zowel technici als klanten kunnen deze informatie bekijken.

Servicetaken maakt u op de pagina **Servicetaken** en koppelt u met behulp van servicetaakrelaties aan een specifieke serviceovereenkomst of serviceorder. Telkens wanneer u een servicetaakrelatie maakt, kunt u het volgende maken:

-  Interne notities voor de taak, zoals uitgebreide informatie over technische vereisten voor de taak waarvan de technicus op de hoogte moet zijn.

-  Externe notities die door de klant kunnen worden bekeken. Hierin kunt u bijvoorbeeld een minder technische uitleg opnemen van de taak die wordt voltooid conform de overeenkomst tussen de klant en het servicebedrijf.

Wanneer u een servicetaakrelatie hebt ingesteld tussen een servicetaak en een serviceorder of serviceovereenkomst, kunt u deze servicetaak opgeven bij het maken van regels voor de huidige serviceorder of serviceovereenkomst.

Als u serviceorders genereert op basis van een serviceovereenkomst, kunt u met behulp van de servicetaken die aan elke serviceovereenkomst zijn toegewezen, de serviceorderregels groeperen in serviceorders.

## <a name="create-a-service-task"></a>Een servicetaak maken

1. Klik op **Servicebeheer** \> **Instellen** \> **Servicetaken**.
2. Maak een nieuwe regel.
3. Voer de service-ID en de omschrijving in.

## <a name="example"></a>Voorbeeld

Een technicus moet twee taken uitvoeren voor een versnellingsbak (serviceobject GB-1234) op een klantlocatie. Er wordt een serviceovereenkomst gemaakt voor de klant en er worden verschillende transacties aan de taken gekoppeld. De serviceovereenkomst en de serviceovereenkomstregels voor beide taken zijn als volgt:

### <a name="service-agreement"></a>Serviceovereenkomst_

| Project | Serviceovereenkomst_ | Omschrijving                                  | Groep   |
|---------|-------------------|----------------------------------------------|---------|
| 9012    | 000008\_001       | Inspectie en routinevervanging - GB – 1234 | Premie |

### <a name="service-agreement-lines"></a>Serviceovereenkomstregels

| Omschrijving             | Transactietype | Serviceobject | Servicetaak |
|-------------------------|------------------|----------------|--------------|
| Inspectie en reiniging | Uur             | GB-1234        | I/C - GB1234 |
| Reiskosten                  | Expense          | GB-1234        | I/C - GB1234 |
| Materialen               | Artikel             | GB-1234        | I/C - GB1234 |
| Routinevervanging     | Uur             | GB-1234        | RR - GB1234  |
| GR-1                    | Artikel             | GB-1234        | RR - GB1234  |
| GR-5                    | Artikel             | GB-1234        | RR - GB1234  |

Aan de serviceovereenkomstregels voor de twee taken zijn twee servicetaken gekoppeld. Op basis van de servicetaken wordt bepaald welke transacties bij elke taak horen. In het eerste geval worden met servicetaak I/C - GB1234 alle serviceovereenkomstregels aangegeven die betrekking hebben op de inspectie en de reiniging van object GB-1234. In het tweede geval worden met servicetaak RR - GB1234 alle serviceovereenkomstregels aangegeven die betrekking hebben op het uitvoeren van een routinevervanging.

Met de volgende servicetaakrelaties worden de servicetaken aan de specifieke serviceovereenkomst gekoppeld:

### <a name="service-tasks"></a>Servicetaken

| Servicetaak | Omschrijving                             | Interne notitie                                                                                                                 | Externe notitie                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| I/C - GB1234 | Inspectie van versnellingsbak GB-1234           | Visuele en mechanische inspectie en reiniging van versnellingsbak GB-1234                                                              | Routine-inspectie van versnellingsbak |
| RR - GB1234  | Routinevervanging van onderdelen in GB-1234 | Routineservice: vervanging van onderdelen GR-1 en GR-5 (voor versnellingsbakken die zijn geproduceerd vóór 2002, moet ook onderdeel GR-2 worden vervangen) | Routine: vervanging van onderdelen  |

## <a name="group-service-orders"></a>Serviceorders groeperen

Automatisch gemaakte serviceorders kunt u met behulp van servicetaken groeperen. Als u serviceorders op servicetaken wilt groeperen, definieert u in de serviceovereenkomst dat serviceorders op basis van deze overeenkomst moeten worden gegroepeerd op de ID van de servicetaak als eerste criterium.

**Groeperen op servicetaak**

1. Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.
2. Op het tabblad **Instellen** selecteert u **Per servicetaak** in het veld **Serviceorders combineren**.


