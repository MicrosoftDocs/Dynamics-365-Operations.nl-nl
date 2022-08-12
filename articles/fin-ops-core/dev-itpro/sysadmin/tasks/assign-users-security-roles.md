---
title: Gebruikers aan beveiligingsrollen toewijzen
description: Voor toegang tot apps voor financiën en bedrijfsactiviteiten moeten gebruikers worden toegewezen aan beveiligingsrollen.
author: Peakerbl
ms.date: 02/09/2022
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
ms.openlocfilehash: b5e69a79f123daff3f85d0100647615ad818288e
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103863"
---
# <a name="manage-users-and-security-roles"></a>Gebruikers en beveiligingsrollen beheren

[!include [banner](../../includes/banner.md)]

Als u andere dan algemene mogelijkheden in apps voor financiën en bedrijfsactiviteiten wilt gebruiken, moeten gebruikers aan beveiligingsrollen worden toegewezen. U kunt gebruikers automatisch aan rollen toewijzen op basis van regels en zakelijke gegevens, gebruikers uitsluiten van automatische roltoewijzing of gebruikers handmatig aan rollen toevoegen.

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
In deze procedure wordt uitgelegd hoe u gebruikers kunt uitsluiten van automatische roltoewijzing.

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

## <a name="manually-remove-users-from-roles"></a>Gebruikers handmatig verwijderen uit rollen
Gebruikers die handmatig aan beveiligingsrollen zijn toegewezen, moeten ook handmatig door de beheerder worden verwijderd. Deze gebruikers worden niet verwijderd via regels voor automatische roltoewijzing.

1. Ga naar **Navigatievenster >Modules > Systeembeheer > Beveiliging > Gebruikers aan rollen toewijzen**.
2. Volg deze stappen om één gebruiker te verwijderen:
   1. Selecteer een rol in de structuur. 
   2. Selecteer de gebruiker die moet worden verwijderd in het gebied **Gebruikers die aan rol zijn toegewezen**.
   3. Selecteer **Verwijderen** om de gebruiker uit de rol te verwijderen.
3. Volg deze stappen om meerdere gebruikers te verwijderen:
   1. Selecteer een rol in de structuur. 
   2. Selecteer in het gebied **Gebruikers die aan rol zijn toegewezen** de optie **Gebruikers handmatig toewijzen/uitsluiten**.
   3. Op de pagina **Gebruikers toewijzen aan of uitsluiten van rol** wordt voor gebruikers aan wie de rol niet is toegewezen de waarde **Geen** weergegeven in de kolom **Toewijzingsmodus**. Selecteer de gebruikers die moeten worden uitgesloten van de rol.
   4. Selecteer **Uitsluiten voor rol** in het **actievenster**. De kolom **Toewijzingsmodus** wordt nu bijgewerkt naar **Handmatig** en de gebruikers zijn nu uitgesloten van de rol.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

