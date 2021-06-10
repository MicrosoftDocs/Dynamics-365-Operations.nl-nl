---
title: Een teamkalender maken
description: Geef teamkalenders weer en maak deze in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cedff4031c6455b446af9c56a770a00f3b2efc80
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052092"
---
# <a name="view-team-and-company-calendars"></a>Team- en bedrijfsagenda's weergeven

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

U kunt team- en bedrijfskalenders weergeven in Dynamics 365 Human Resources. In teamkalenerds worden alleen directe rapporten weergegeven, zoals gedefinieerd in de regelhiërarchie.

## <a name="view-your-team-calendar-as-an-employee"></a>Uw teamkalender als werknemer weergeven

1. Selecteer in het werkgebied **Selfservice werknemer** de optie **Teamverzuimkalender** onder **Overzicht**.

## <a name="view-your-team-calendar-as-a-manager"></a>Uw teamkalender als manager weergeven

1. Selecteer in het werkgebied **Selfservice werknemer** de optie **Mijn team**.

2. Selecteer **Verlof en verzuim** en selecteer vervolgens **Verzuimkalender manager weergeven**.

Managers kunnen ook toegang krijgen tot de teamkalender via **Uitstaande verlofaanvragen voor mijn team**, **Goedgekeurd verlof** en **Verlofaanvragen**. 

## <a name="view-a-company-calendar"></a>Een bedrijfskalender weergeven

Mensen in Human Resources-rollen kunnen bedrijfskalenders weergeven. In bedrijfs kalenders worden alle werknemers weergegeven. Standaard wordt in de kalender de datum van vandaag plus 28 dagen weergegeven, maar u kunt het datumbereik wijzigen. U kunt de kalender ook filteren op **naam**, **personeelsnummer** en **verloftype**.

1. Selecteer in het werkgebied **Verlof en verzuim** de optie **Koppelingen**.

2. Selecteer **Verlof- en verzuimkalender**.

Rollen van Human Resources kunnen ook toegang krijgen tot de bedrijfskalender via **Aanvragen voor verlof en verzuim**, **Goedgekeurd verlof** en **Verlofaanvragen**. 

Kalenders bevatten nu extra filters en opties. Alle kalenders bevatten weergaveopties voor:

- Goedgekeurde aanvragen
- Aanvragen in behandeling
- Werknemers met verlofaanvragen
- Werknemers zonder verlofaanvragen
- Verjaardagen van werknemers
- Verlofaanvragen 
- Verlofaanvragen

Kalenderconfiguratie in Verlof- en verzuimparameters bepalen beschikbare weergaveopties.

U kunt kalenders ook filteren op manager of afdeling. De primaire positietoewijzing bepaalt welke werknemers worden weergegeven wanneer deze filters zijn ingesteld. 

>[!IMPORTANT]
>Het bekijken van verlof en afwezigheid binnen bedrijven wordt momenteel in een voorbeeld weergegeven. U moet deze in uw **Sandbox**-omgeving inschakelen. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van previewfuncties.<br><br>
>Vervolgens moet u de functie in **Gedeelde Human Resources-parameters** inschakelen om de rechtspersoonfilter in kalenders weer te geven. Zie [Verlof- en verzuimparameters configureren](hr-leave-and-absence-parameters.md) voor meer informatie.<br><br>
>U kunt de kalender filteren op rechtspersoon. Als u alle werknemers wilt weergeven, ongeacht de rechtspersoon, wist u het vak filteren en selecteert u invoeren. 

Zie [Kalenderparameters configureren](hr-leave-and-absence-parameters.md?configure-calendar-parameters) voor meer informatie over kalenderinstellingen.



[!INCLUDE[footer-include](../includes/footer-banner.md)]