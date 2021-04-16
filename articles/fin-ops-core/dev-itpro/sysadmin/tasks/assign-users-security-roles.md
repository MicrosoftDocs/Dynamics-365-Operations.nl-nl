---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot Finance and Operations-apps moeten gebruikers zijn toegewezen aan beveiligingsrollen.
author: Peakerbl
ms.date: 05/06/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecRolesEditUsers, SysSecAssignmentQueryLookup, SysQueryForm, SysSecRoleExcludeUsers
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4b143400a1f092c8f7a15bbb047eda52a4a4d8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745880"
---
# <a name="assign-users-to-security-roles"></a>Gebruikers aan beveiligingsrollen toewijzen

[!include [banner](../../includes/banner.md)]

Als u andere dan algemene mogelijkheden in Finance and Operations-apps wilt gebruiken, moeten gebruikers aan beveiligingsrollen worden toegewezen. U kunt gebruikers automatisch aan rollen toewijzen op basis van regels en zakelijke gegevens, gebruikers uitsluiten van automatische roltoewijzing of gebruikers handmatig aan rollen toevoegen.

## <a name="automatically-assign-users-to-roles"></a>Gebruikers automatisch aan rollen toewijzen
In deze procedure wordt beschreven hoe systeembeheerders gebruikers automatisch aan rollen kunnen toewijzen op basis van bedrijfsgegevens. 
1. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
2. Selecteer Supervisor boekhouding in de structuur. Selecteer de rol waarvoor u de regel wilt configureren Selecteer voor dit voorbeeld Supervisor boekhouding. 
3. Klik op **Regel toevoegen** om het dialoogmenu te openen.
4. Zoek en selecteer de gewenste record in de lijst **Selecteer een query**. Selecteer de query die u voor deze regel wilt gebruiken.  
5. Klik in de lijst **Regelnaam lidmaatschap** op de koppeling in de geselecteerde rij.
6. Selecteer **Query bewerken**. Bewerk de query indien nodig.  
7. Selecteer **OK**.
8. Selecteer **Automatische roltoewijzing uitvoeren**.
9. Ga naar **Navigatiedeelvenster > modules > Systeembeheer > Gebruikers > Gebruikers** (in het ideale geval op een afzonderlijk tabblad van de browser).
10. Controleer de rollen die aan verschillende gebruikers zijn toegewezen om te bevestigen dat de query voor roltoewijzing juist is. Pas aan en voer opnieuw uit, indien nodig.

## <a name="exclude-users-from-automatic-role-assignment"></a>Gebruikers uitsluiten van automatische roltoewijzing
1. Sluit de pagina.
2. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
3. Selecteer Supervisor boekhouding in de structuur. Hier kunt u een rol selecteren. Selecteer voor dit voorbeeld Supervisor boekhouding.  
4. Selecteer in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen / uitsluiten**.
5. Markeer in de geselecteerde rij in de lijst **Gebruikers toewijzen aan of uitsluiten voor rol**. Selecteer een gebruiker.  
6. Selecteer **Uitsluiten voor rol** in het **actievenster**.
7. Selecteer **Uitsluiten voor rol** om de geselecteerde gebruikers voor de rol uit te sluiten. Om uitsluitingen te verwijderen, selecteert u de gebruikers voor wie u uitsluitingen wilt verwijderen. Vervolgens klikt u op **Status opnieuw instellen**. Wanneer u een uitsluiting verwijdert door de status van de gebruiker opnieuw in te stellen, wordt de rol van de gebruiker automatisch toegewezen. De gebruiker wordt echter niet onmiddellijk aan de rol toegewezen of van de rol uitgesloten wanneer u de status opnieuw instelt. In plaats daarvan wordt de gebruiker de volgende keer dat de regels voor automatische roltoewijzing worden uitgevoerd, aan de rol toegewezen of van de rol verwijderd.  

## <a name="manually-assign-users-to-roles"></a>Gebruikers handmatig aan rollen toewijzen
Gebruikers die handmatig aan beveiligingsrollen zijn toegewezen, moeten ook handmatig door de beheerder worden verwijderd. Deze gebruikers worden niet verwijderd via regels voor automatische roltoewijzing.

1. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
2. Selecteer een rol in de structuur en in het menu **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen/uitsluiten**.
4. In **Gebruikers toewijzen aan of uitsluiten van rol** worden gebruikers aan wie de rol niet is toegewezen, weergegeven en wordt de **Toewijzingsmodus** ingesteld op **Geen**. Selecteer een of meer gebruikers waaraan u de rol wilt toewijzen.
5. Selecteer **Toewijzen aan rol** in het **actievenster**. De **Toewijzingsmodus** wordt bijgewerkt naar **Handmatig** en aan de gebruikers wordt nu een nieuwe rol toegewezen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]