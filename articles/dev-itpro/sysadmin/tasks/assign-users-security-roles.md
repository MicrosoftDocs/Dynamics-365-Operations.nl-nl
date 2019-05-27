---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55cb085bb5170aa4894a2240a12f6ca451b922fb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556704"
---
# <a name="assign-users-to-security-roles"></a>Gebruikers aan beveiligingsrollen toewijzen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen. In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="automatically-assign-users-to-roles"></a>Gebruikers automatisch aan rollen toewijzen
1. Ga naar Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen.
2. Selecteer Supervisor boekhouding in de structuur.
    * Selecteer de rol waarvoor u de regel wilt configureren Selecteer voor dit voorbeeld Supervisor boekhouding.  
3. Klik op Regel toevoegen om het dialoogvenster voor beëindigen te openen.
4. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de query die u voor deze regel wilt gebruiken.  
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Query bewerken.
    * Bewerk de query indien nodig.  
7. Klik op OK.

## <a name="exclude-users-from-automatic-role-assignment"></a>Gebruikers uitsluiten van automatische roltoewijzing
1. Sluit de pagina.
2. Ga naar Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen.
3. Selecteer Supervisor boekhouding in de structuur.
    * Hier kunt u een rol selecteren. Selecteer voor dit voorbeeld Supervisor boekhouding.  
4. Klik op Gebruikers handmatig toewijzen / uitsluiten.
5. Markeer in de lijst de geselecteerde rij.
    * Selecteer een gebruiker.  
6. Klik op Uitsluiten van rol.
    * Klik op Uitsluiten van rol om de geselecteerde gebruikers van de rol uit te sluiten. Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op Status opnieuw instellen. Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen. De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt. In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.  

