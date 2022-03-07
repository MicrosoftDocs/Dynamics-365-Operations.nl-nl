---
title: Conflicten bij scheiding van taken identificeren en oplossen
description: In dit onderwerp wordt uitgelegd hoe u conflicten bij de scheiding van taken kunt identificeren en oplossen.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0638699c0e569bbe67024a87d6c55729642557cb085ee899aa98aa0022b12840
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748307"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a>Conflicten bij scheiding van taken identificeren en oplossen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u conflicten bij de scheiding van taken kunt identificeren en oplossen. U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd. Dit concept wordt scheiding van taken genoemd. Wanneer de definitie van een beveiligingsrol of de roltoewijzingen van een gebruiker de regels overtreden, wordt het conflict vastgelegd. Alle conflicten moeten door de beheerder worden opgelost. Voer de volgende procedure uit om conflicten te identificeren en op te lossen.

Controleer nadat u een regel hebt toegevoegd of alle bestaande rollen compatibel zijn. 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a>Controleren of bestaande rollen en taken voldoen aan nieuwe regels voor scheiding van taken
1. Ga naar **Systeembeheer** > **Beveiliging** > **Scheiding van taken** > **Regels voor scheiding van taken**.
3. Selecteer **Taken en rollen valideren**. Als er rollen zijn die de regels overtreden, wordt een bericht weergegeven dat de naam van de regel, de rol en de namen van de conflicterende taken bevat. Conflicterende rollen moeten worden gewijzigd met de **Beveiligingsconfiguratie** en kunnen geen conflicterende taken bevatten. Als geen rollen de geselecteerde regel overtreden, wordt een bericht weergegeven dat alle rollen voldoen.   

> [!NOTE]
> De validatie wordt alleen voor de geselecteerde regel uitgevoerd. Het is belangrijk dat de conformiteit voor elke regel wordt gevalideerd.   

Wanneer u een rol maakt of wijzigt, worden de regels voor de scheiding van taken automatisch afgedwongen. U kunt conflicterende taken niet aan een rol toewijzen.

Controleer vervolgens of alle bestaande roltoewijzingen compatibel zijn.

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a>Controleren of toewijzingen van gebruikersrollen voldoen aan nieuwe regels voor scheiding van taken
1. Ga naar **Systeembeheer > Beveiliging > Scheiding van taken > Naleving van toewijzingen van gebruikersrollen controleren**.
2. Selecteer **OK**. Een melding geeft het resultaat van de validatie weer. Conflicten worden vastgelegd op de pagina **Niet-opgeloste conflicten met betrekking tot scheiding van taken**.   

Wanneer u gebruikers aan rollen toewijst, worden de regels voor de scheiding van taken automatisch afgedwongen. Als u een gebruiker probeert toe te wijzen aan rollen die conflicterende taken bevatten, ontvangt u een foutbericht. U moet het conflict vervolgens oplossen door de aanvullende roltoewijzing te weigeren of toe te staan. De extra rol wordt toegewezen nadat de toewijzing is toegestaan. 

> [!NOTE]
> Conflicten worden momenteel niet gecontroleerd voor gebruikers die aan rollen zijn toegewezen op basis van de Active Directory-domeingroepen.

## <a name="view-and-resolve-conflicting-user-role-assignments"></a>Conflicterende toewijzingen van gebruikersrollen weergeven en oplossen
1. Ga naar **Systeembeheer** > **Beveiliging** > **Scheiding van taken** > **Niet-opgeloste conflicten met betrekking tot scheiding van taken**. 
2. Selecteer een conflict en selecteer vervolgens een van de volgende acties: 

  - **Toewijzing niet toestaan**: hiermee wordt de toewijzing van de gebruiker aan de aanvullende beveiligingsrol geweigerd. Als u een automatische roltoewijzing afwijst, wordt de gebruiker gemarkeerd als uitgesloten van de rol. De uitgesloten gebruiker krijgt niet de toegang die aan de rol is gekoppeld en kan niet aan de rol worden toegewezen tot de beheerder de uitsluiting verwijdert. 
-  **Toewijzing toestaan** hiermee wordt het conflict overschreven en wordt het aan de gebruiker toegestaan aan de extra beveiligingsrol te worden toegewezen. Als u een conflict overschrijft, moet u een reden invoeren in het veld **Reden voor overschrijving**. Alle overschreven roltoewijzingen kunnen worden weergegeven op de pagina **Conflicten voor scheiding van taken**.  

> [!NOTE]
> Als er meerdere conflicten worden vermeld voor dezelfde gebruiker, selecteert u de gebruikersrecord en evalueert u de toegewezen rollen op de pagina **Gebruikers**. Om dit conflict te voorkomen valideert u elke regel nadat deze is toegevoegd of gewijzigd.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]