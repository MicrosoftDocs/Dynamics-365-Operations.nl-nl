---
title: Configuraties stopzetten in de globale opslagplaats van RCS
description: In dit artikel wordt beschreven hoe u stopt met de configuraties in de globale opslagplaats van RFS.
author: gionoder
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.custom: 97423
ms.assetid: ''
ms.search.form: ERSolutionTable, ERWorkspace
ms.openlocfilehash: b0605f56058e3c93ea088ee8386ba26c4ce2b65a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272331"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Configuraties stopzetten in de globale opslagplaats van RCS

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u stopt met de configuratie in de globale opslagplaats van RFS. Voorheen was het alleen mogelijk om configuraties te verwijderen die niet meer nodig waren. Nu kunt u echter een vrijgegeven configuratie als **Beëindigd** markeren in de globale opslagplaats van RCS. Met deze functionaliteit kunt u ook het volgende doen: 
 
 - Vooraf meldingen opgeven wanneer een configuratie volgens de planning moet worden beëindigd.
 - Toepasselijke gegevens over de vervangingsconfiguratie opnemen.
 - Een datum **Ondersteund tot** instellen voor de specifieke configuratie om de gebruiker te informeren wanneer deze wordt beëindigd.

Wanneer u een configuratieversie beëindigt, kunt u de volgende optionele informatie opgeven:

  - **Vervangingsconfiguratie**
  - **Versie van vervangingsconfiguratie**
  - **Vrije-tekstnotitie**: gebruik dit veld als u documentatiekoppelingen of verwijzingen wilt leveren
  - **Ondersteund tot**: dit veld bevat de voorgestelde datum tot wanneer de huidige configuratie/versie wordt ondersteund. Deze datum moet handmatig worden bijgewerkt.
  
Als u de configuratie wilt beëindigen, voltooit u de volgende stappen. 

1. Selecteer of u wilt één versie of alle versies met dezelfde instellingen in één bewerking wilt beëindigen door **Alle versies** in te stellen op **Ja**. 
2. Stel de parameter **Beëindigen** in op **Ja**.
3. Selecteer **OK** om de configuraties te beëindigen. Het veld **Einddatum** wordt ingevuld wanneer u de wijzigingen opslaat.

![Configuratiegegevens stopzetten.](media/Discontinue-details-2.png)
  
U kunt de configuratie op elk moment terugdraaien naar **Gedeeld** of beëindigingsgegevens aanpassen. Als u een configuratie deelt, geeft u de datum **Ondersteund tot** en alle andere informatie met betrekking tot de beëindiging op om aan te geven dat u toekomstige beëindiging plant.

Als u informatie wilt delen over een geplande beëindiging voordat de configuratie daadwerkelijk wordt beëindigd, kan de gebruiker alle velden die zijn gerelateerd aan de vervanging vooraf invullen, maar de parameter **Beëindigen** op **Nee** laten staan.

> [!NOTE]
> Bij beëindiging worden bewerkingen met configuraties niet beperkt. U kunt de configuraties blijven importeren, uitvoeren of afleiden. Deze velden dienen ter informatie.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance ondersteunt het weergeven van deze informatie vanaf versie 10.0.14

Vanaf versie 10.0.14 ondersteunt Dynamics 365 Finance het weergeven van beëindigingsinformatie. Op de pagina **Globale opslagplaats** kunt u actuele informatie weergeven met betrekking tot beëindiging. Configuraties die zijn beëindigd worden standaard uitgefilterd.
  
Op de pagina **Geïmporteerde configuraties** (ERSolutionTable) worden configuraties weergegeven die al waren beëindigd toen zij werden geïmporteerd. Voor configuraties die zijn beëindigd na het importeren, kan de beëindigingsinformatie worden gesynchroniseerd door de taak **Updates van configuraties importeren** uit te voeren.


