---
title: Afschrijvingsconventies voor vaste activa
description: Dit onderwerp bevat een overzicht van de afschrijvingsconventies van vaste activa.
author: saraschi2
manager: AnnBe
ms.date: 03/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad44282de9d999aa211548601eb416f4bdba2047
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177150"
---
# <a name="fixed-asset-depreciation-conventions"></a>Afschrijvingsconventies voor vaste activa

[!include [banner](../includes/banner.md)]

Afschrijvingsconventies worden gebruikt om te bepalen wanneer en hoe de afschrijving wordt berekend voor zowel het jaar waarin het vaste activum is verworven en het jaar waarop het vaste activum is afgestoten.

Afschrijvingsconventies kunnen worden toegewezen aan de instelling voor een boek van de vaste-activagroep. Als u de afschrijvingsconventie wilt weergeven of toewijzen, selecteert u in het instellingsgebied **Groepen vaste activa**. Selecteer de knop **Boeken**. In dit geval worden de afschrijvingsconventies die zijn toegewezen, gebruikt als standaardwaarden wanneer de boeken voor vaste activa worden gemaakt. Afschrijvingsconventies kunnen ook worden ingesteld voor een afzonderlijke vaste-activaboek. Selecteer hiervoor **Boeken** in het instellingsgebied van vaste activa en selecteer vervolgens de knop **Groepen vaste activa**.


|  Afschrijvingsconventie  |   Beschrijving  |
|---------------------------|-----------------|
|           Geen            |  Activaafschrijving begint vanaf de datum <strong>In gebruik genomen</strong>.|
|         Half jaar         |  Trek een half jaar afschrijving af voor het eerste jaar en het laatste jaar waarin u het eigendom afschrijft. Trek een heel jaar afschrijving af voor alle andere jaren van de afschrijvingsperiode. |
|        Hele maand         | Activa met een datum <strong>In gebruik genomen</strong> die zich voordoet op een moment tijdens de maand beginnen met afschrijven op de eerste dag van die maand. Activa die zijn afgestoten op een moment tijdens de maand worden beschouwd als afgestoten voor afschrijvingsdoeleinden op de laatste dag van de vorige maand.  |
|        Midden kwartaal        | Voor het berekenen van de afschrijvingsaftrek voor het jaar wanneer u het eigendom in gebruik neemt, vermenigvuldigt u de afschrijving voor een heel jaar met het percentage voor het kwartaal waarin het eigendom in gebruik wordt genomen, zoals in de volgende tabel.<table><thead><tr><th>Kwartaal</th><th>Percentage</th></tr></thead><tbody><tr><td>Voornaam</td><td>87,5</td></tr><tr><td>Tweede</td><td>62,5</td></tr><tr><td>Derde</td><td>37,5</td></tr><tr><td>Vierde</td><td>12,5</td></tr></tbody></table>Een half-kwartaal afschrijving wordt overgenomen in het kwartaal van afstoting (of het volledig afgeschreven kwartaal). |
| Midden maand (1ste van de maand)  | Activa met een datum <strong>In gebruik genomen</strong> in de eerste helft van de maand (1 tot en met 15 dagen) beginnen met afschrijven op de eerste dag van de maand van de datum <strong>In gebruik genomen</strong>. Activa met een datum <strong>In gebruik genomen</strong> in de tweede helft van de maand (dag 16 tot het einde van de maand) beginnen met afschrijven op de eerste dag van de maand na de datum <strong>In gebruik genomen</strong>. Activa die zijn afgestoten in de eerste helft van de maand (dag 1 tot en met 15) worden beschouwd als afgestoten voor afschrijvingsdoeleinden op de laatste dag van de vorige maand. Activa die zijn afgestoten in de tweede helft van de maand (dag 16 tot en met het einde van de maand) worden beschouwd als afgestoten voor afschrijvingsdoeleinden op de laatste dag van de vorige maand. |
| Midden maand (15e van de maand) |  Voor het berekenen van de inhoudingsafschrijving voor het jaar wanneer u het eigendom in gebruik neemt, vermenigvuldigt u de afschrijving voor een heel jaar met een breuk. De teller (bovenste getal) van deze breuk is het aantal volledige maanden in het jaar dat het eigendom in gebruik is genomen, plus 1/2 of (0,5). De noemer (onderste getal) is 12. Als u het eigendom vóór het einde van de afschrijvingsperiode afstoot, moet u dezelfde methode gebruiken voor het berekenen van de afschrijvingsaftrek voor het jaar van afstoting.   |
| Half jaar (begin van het jaar) | Activa met een datum <strong>In gebruik genomen</strong> in de eerste helft van het jaar beginnen met afschrijven op de eerste dag van het jaar (hele jaar). Activa met een datum <strong>In gebruik genomen</strong> in de tweede helft van het jaar beginnen met afschrijven midden in het jaar.|
|   Halfjaar (volgend jaar)   |   Activa met een datum <strong>In gebruik genomen</strong> in de eerste helft van het jaar beginnen met afschrijven op de eerste dag van het jaar (hele jaar). Activa met een datum <strong>In gebruik genomen</strong> in de tweede helft van het jaar beginnen met afschrijven op de eerste dag van het volgende jaar. Activa die zijn afgestoten in de eerste helft van het jaar, worden beschouwd als afgestoten voor afschrijvingsdoeleinden op de laatste dag van het vorige jaar. De afschrijving die is geboekt in het huidige jaar, moet worden omgekeerd of aangepast. Activa die zijn ingetrokken in de tweede helft van het jaar, worden beschouwd als afgestoten voor afschrijvingsdoeleinden op de laatste dag van het jaar van afstoten.|

