---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: maertenm
manager: AnnBe
ms.date: 10/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3c347a34a389c32d005cc8086c4a1349ecb8a698
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570516"
---
# <a name="create-new-users"></a>Nieuwe gebruikers maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken te doen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Een gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)
Voor klanten met een van de nieuwe licentietypen die zijn toegevoegd in oktober 2019, moeten gebruikers aan een licentie zijn gekoppeld. Gebruikers die aan een licentie zijn gekoppeld, worden automatisch toegevoegd als systeemgebruikers die geen rollen hebben wanneer ze zich voor de eerste keer aanmelden. Gebruikers die niet aan een licentie zijn gekoppeld, ontvangen een waarschuwingsbericht.

Systeembeheerders [kunnen licenties aan gebruikers toewijzen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-a-new-user"></a>Een nieuwe gebruiker toevoegen
1. Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in. Een gebruikers-id is vereist.  
4. Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.  
5. Voer in het veld **Domein** het domein van de gebruiker in.  
6. Voer in het veld **Alias** de alias van de gebruiker in.  
7. Selecteer het gewenste bedrijf in het veld **Bedrijf**. 
8. Selecteer op het sneltabblad **Rollen van gebruiker** de optie **Rollen toewijzen** om [gebruikers aan beveiligingsrollen toe te wijzen](assign-users-security-roles.md).
9. Selecteer **OK**.
10. Selecteer **Opslaan**.

## <a name="import-users"></a>Gebruikers importeren
1. Selecteer **Gebruikers importeren** in het Actievenster.
2. Markeer in de lijst de geselecteerde rij.
3. Selecteer **Gebruikers importeren**.
4. Selecteer **Sluiten**.

