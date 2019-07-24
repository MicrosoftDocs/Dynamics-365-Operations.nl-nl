---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
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
ms.openlocfilehash: ab9f2f5ea07ae1d616c48dffa8810b966f7dbb2f
ms.sourcegitcommit: 33e98f89294086334fe9c0a350abb6a52ef9dacb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/28/2019
ms.locfileid: "1711126"
---
# <a name="assign-users-to-security-roles"></a>Gebruikers aan beveiligingsrollen toewijzen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Voor toegang tot Microsoft Dynamics 365 for Finance and Operations moeten gebruikers zijn toegewezen aan beveiligingsrollen. In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="automatically-assign-users-to-roles"></a>Gebruikers automatisch aan rollen toewijzen
1. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
2. Selecteer Supervisor boekhouding in de structuur. Selecteer de rol waarvoor u de regel wilt configureren Selecteer voor dit voorbeeld Supervisor boekhouding. 
3. Klik op **Regel toevoegen** om het dialoogvenster voor beëindigen te openen.
4. Zoek en selecteer de gewenste record in de lijst **Selecteer een query**. Selecteer de query die u voor deze regel wilt gebruiken.  
5. Klik in de lijst **Regelnaam lidmaatschap** op de koppeling in de geselecteerde rij.
6. Klik op **Query bewerken**. Bewerk de query indien nodig.  
7. Klik op **OK**.

## <a name="exclude-users-from-automatic-role-assignment"></a>Gebruikers uitsluiten van automatische roltoewijzing
1. Sluit de pagina.
2. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
3. Selecteer Supervisor boekhouding in de structuur. Hier kunt u een rol selecteren. Selecteer voor dit voorbeeld Supervisor boekhouding.  
4. Selecteer in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen / uitsluiten**.
5. Markeer in de geselecteerde rij in de lijst **Gebruikers toewijzen aan of uitsluiten voor rol**. Selecteer een gebruiker.  
6. Selecteer **Uitsluiten voor rol** in het **actievenster**.
    
    Klik op **Uitsluiten voor rol** om de geselecteerde gebruikers voor de rol uit te sluiten. Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op **Status opnieuw instellen**. Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen. De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt. In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.  
