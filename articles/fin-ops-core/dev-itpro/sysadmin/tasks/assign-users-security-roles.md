---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Finance and Operations-apps moeten gebruikers zijn toegewezen aan beveiligingsrollen.
author: ChrisGarty
manager: AnnBe
ms.date: 11/14/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0744f45ac91dfb9b5aae35091e3675202c9144f9
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143535"
---
# <a name="assign-users-to-security-roles"></a>Gebruikers aan beveiligingsrollen toewijzen

[!include [banner](../../includes/banner.md)]

Als u andere dan algemene mogelijkheden wilt gebruiken, moeten gebruikers aan beveiligingsrollen worden toegewezen. In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens. 

## <a name="automatically-assign-users-to-roles"></a>Gebruikers automatisch aan rollen toewijzen
1. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
2. Selecteer Supervisor boekhouding in de structuur. Selecteer de rol waarvoor u de regel wilt configureren Selecteer voor dit voorbeeld Supervisor boekhouding. 
3. Klik op **Regel toevoegen** om het dialoogvenster voor beëindigen te openen.
4. Zoek en selecteer de gewenste record in de lijst **Selecteer een query**. Selecteer de query die u voor deze regel wilt gebruiken.  
5. Klik in de lijst **Regelnaam lidmaatschap** op de koppeling in de geselecteerde rij.
6. Klik op **Query bewerken**. Bewerk de query indien nodig.  
7. Klik op **OK**.
8. Klik op **Automatische roltoewijzing uitvoeren**.
9. Ga naar **Navigatiedeelvenster > modules > Systeembeheer > Gebruikers > Gebruikers** (in het ideale geval op een afzonderlijk tabblad van de browser).
10. Controleer de rollen die aan verschillende gebruikers zijn toegewezen om te bevestigen dat de query voor roltoewijzing juist is. Pas aan en voer opnieuw uit, indien nodig.

## <a name="exclude-users-from-automatic-role-assignment"></a>Gebruikers uitsluiten van automatische roltoewijzing
1. Sluit de pagina.
2. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
3. Selecteer Supervisor boekhouding in de structuur. Hier kunt u een rol selecteren. Selecteer voor dit voorbeeld Supervisor boekhouding.  
4. Selecteer in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen / uitsluiten**.
5. Markeer in de geselecteerde rij in de lijst **Gebruikers toewijzen aan of uitsluiten voor rol**. Selecteer een gebruiker.  
6. Selecteer **Uitsluiten voor rol** in het **actievenster**.
    
    Klik op **Uitsluiten voor rol** om de geselecteerde gebruikers voor de rol uit te sluiten. Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op **Status opnieuw instellen**. Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch opnieuw toegewezen. De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt. In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.  
