---
title: Conflicten bij scheiding van taken identificeren en oplossen
description: In dit onderwerp wordt uitgelegd hoe u conflicten bij de scheiding van taken kunt identificeren en oplossen.
author: peakerbl
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7e25a568b86ce3161e2c52045ff2361c0bc4a0e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681589"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Conflicten bij scheiding van taken identificeren en oplossen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u conflicten bij de scheiding van taken kunt identificeren en oplossen. U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd. Dit concept wordt scheiding van taken genoemd. Wanneer de definitie van een beveiligingsrol of de roltoewijzingen van een gebruiker de regels overtreden, wordt het conflict vastgelegd. Alle conflicten moeten door de beheerder worden opgelost. Voer de volgende procedure uit om conflicten te identificeren en op te lossen. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="verify-whether-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Controleren of toewijzingen van gebruikersrollen voldoen aan nieuwe regels voor scheiding van taken
1. Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Naleving van toewijzingen van gebruikersrollen controleren**.
2. Selecteer **OK**. Een melding geeft het resultaat van de validatie weer. Als er een conflict is, kunt u de pagina **Gebruikers** openen en de roltoewijzingen van de gebruiker wijzigen. Conflicten worden vastgelegd op de pagina **Conflicten voor scheiding van functies**. Om het verificatieproces als batchtaak uit te voeren, selecteert u **Batchverwerking** en stelt u de overige batchparameters in. Nadat de batchtaak is uitgevoerd, kunt u de conflicten bekijken op de pagina **Conflicten voor scheiding van functies**.  

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Conflicterende toewijzingen van gebruikersrollen weergeven en oplossen
1. Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Conflicten voor scheiding van taken**. Selecteer een conflict en selecteer een van de volgende knoppen: **Toewijzing niet toestaan - De toewijzing van de gebruiker aan de aanvullende beveiligingsrol niet toestaan**. Als u een automatische roltoewijzing afwijst, wordt de gebruiker gemarkeerd als uitgesloten van de rol. De uitgesloten gebruiker krijgt niet de toegang die aan de rol is gekoppeld en de gebruiker kan niet aan de rol worden toegewezen tot de beheerder de uitsluiting verwijdert. Toewijzing toestaan - **Overschrijf** het conflict en sta de gebruiker toe aan beide beveiligingsrollen te worden toegewezen. Als u een conflict overschrijft, moet u een reden invoeren in het veld **Reden voor overschrijving**.  
2. Sluit de pagina.
3. Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Niet-opgeloste conflicten met betrekking tot scheiding van functies**. Selecteer een conflict en selecteer een van de volgende knoppen: **Toewijzing niet toestaan - De toewijzing van de gebruiker aan de aanvullende beveiligingsrol niet toestaan**. Als u een automatische roltoewijzing afwijst, wordt de gebruiker gemarkeerd als uitgesloten van de rol. De uitgesloten gebruiker krijgt niet de toegang die aan de rol is gekoppeld en de gebruiker kan niet aan de rol worden toegewezen tot de beheerder de uitsluiting verwijdert. Toewijzing toestaan - **Overschrijf** het conflict en sta de gebruiker toe aan beide beveiligingsrollen te worden toegewezen. Als u een conflict overschrijft, moet u een reden invoeren in het veld **Reden voor overschrijving**.    
4. Sluit de pagina.

## <a name="verify-whether-existing-roles-comply-with-new-rules-for-segregation-of-duties"></a>Controleren of bestaande rollen voldoen aan nieuwe regels voor scheiding van taken
1. Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Regels voor scheiding van taken**. Selecteer een regel.  
2. Selecteer **Taken en rollen valideren**. Als bestaande rollen de geselecteerde regel overtreden, wordt een bericht weergegeven dat de naam van de rol en de namen van de conflicterende functies bevat. De beheerder moet de beperking van het beveiligingsrisico aangeven of de rol wijzigen zodat deze niet de regels voor scheiding van taken overtreedt. Als geen rollen de geselecteerde regel overtreden, wordt een bericht weergegeven dat alle rollen voldoen.  

