---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: maertenm
manager: AnnBe
ms.date: 02/06/2020
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
ms.openlocfilehash: 9db4b6d355d6499bce6c550b2fbe76b82cf69fd4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143564"
---
# <a name="create-new-users"></a>Nieuwe gebruikers maken

[!include [banner](../../includes/banner.md)]

Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken te doen.

## <a name="associate-a-user-with-a-license-new-license-types-only"></a>Een gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)
Voor klanten met een van de nieuwe licentietypen die zijn toegevoegd in oktober 2019, moeten gebruikers aan een licentie zijn gekoppeld. Gebruikers die aan een licentie zijn gekoppeld, worden automatisch toegevoegd als systeemgebruikers die geen rollen hebben wanneer ze zich voor de eerste keer aanmelden.

Systeembeheerders [kunnen licenties aan gebruikers toewijzen](https://docs.microsoft.com/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](https://docs.microsoft.com/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="associate-an-external-user-with-a-license-new-license-types-only"></a>Een externe gebruiker aan een licentie koppelen (alleen nieuwe licentietypen)
Gebruikers buiten de tenant waarin de omgeving is geïmplementeerd, moeten worden weergegeven in de tenant-directory van de host (Azure Active Directory (Azure AD)), zodat hieraan licenties kunnen worden toegewezen. Deze externe gebruikers moeten aan de tenant in Azure AD als gast gebruikers worden toegevoegd en vervolgens de vereiste licenties toegewezen krijgen. Zie [Gebruikers van Azure Active Directory B2B-samenwerking toevoegen in de Azure Portal](https://docs.microsoft.com/azure/active-directory/b2b/add-users-administrator)voor meer informatie.

## <a name="add-a-new-user"></a>Een nieuwe gebruiker toevoegen
1. Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in. Een gebruikers-id is vereist.  
4. Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.  
5. Voer in het veld **Domein** het domein van de gebruiker in.  
6. Voer in het veld **Alias** de alias van de gebruiker in.  
7. Selecteer het gewenste bedrijf in het veld **Bedrijf**. 
8. Selecteer op het sneltabblad **Rollen van gebruiker** de optie **Rollen toewijzen** om gebruikers aan beveiligingsrollen toe te wijzen. Zie [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie.
9. Selecteer **OK**.
10. Selecteer **Opslaan**.

## <a name="import-users"></a>Gebruikers importeren
1. Selecteer **Gebruikers importeren** in het Actievenster.
2. Markeer in de lijst de geselecteerde rij.
3. Selecteer **Gebruikers importeren**.
4. Selecteer **Sluiten**.

