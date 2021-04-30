---
title: Nieuwe gebruikers maken
description: Gebruikers zijn interne werknemers van uw organisatie of externe klanten en leveranciers, die toegang nodig hebben tot het systeem om hun taken uit te voeren.
author: peakerbl
ms.date: 01/12/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88d3f1fba05d944e78e4595018d190c3dc41e076
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5907906"
---
# <a name="create-new-users"></a>Nieuwe gebruikers maken

[!include [banner](../../includes/banner.md)]

Voordat u toegang kunt krijgen tot Finance and Operations-apps, moet u eerst worden toegevoegd aan de pagina **Gebruikers** (**Systeembeheer \> Gebruikers \> Gebruikers**). Gebruikers kunnen interne werknemers van uw organisatie of externe klanten en leveranciers zijn. Gebruikers kunnen handmatig worden geïmporteerd of toegevoegd. Alle gebruikers moeten over een juiste licentie voor compatibel gebruik beschikken.

Voor informatie over hoe u Finance and Operations-apps koopt en hiervoor een licentie krijgt, raadpleegt u [Microsoft Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544&amp;clcid=0x409).

## <a name="assign-a-license-to-a-user"></a>Een licentie aan een gebruiker toewijzen
Systeembeheerders [kunnen licenties aan gebruikers toewijzen](/office365/admin/subscriptions-and-billing/assign-licenses-to-users?view=o365-worldwide) in het [Microsoft 365-beheercentrum](/office365/admin/admin-overview/about-the-admin-center?view=o365-worldwide).

## <a name="add-an-external-user-in-azure-ad-and-assign-a-license"></a>Een externe gebruiker toevoegen in Azure AD en een licentie toewijzen 
Externe gebruikers moeten worden vertegenwoordigd in uw tenantdirectory (Azure Active Directory (Azure AD)) zodat aan hen licenties kunnen worden toegewezen. Deze externe gebruikers moeten aan de tenant in Azure AD als gast gebruikers worden toegevoegd en vervolgens de vereiste licenties toegewezen krijgen. Een vereiste voor Finance and Operations-apps is dat het bedrijf van de gastgebruiker Azure AD moet gebruiken. Zie [Gebruikers van Azure Active Directory B2B-samenwerking toevoegen in de Azure Portal](/azure/active-directory/b2b/add-users-administrator)voor meer informatie.

## <a name="import-new-users-from-azure-ad"></a>Nieuwe gebruikers importeren vanuit Azure AD 
1. Ga naar **Systeembeheer** \> **Gebruiker** \> **Gebruikers**.
2. Selecteer **Gebruikers importeren** in het Actievenster.
3. Selecteer de gebruikers die moeten worden geïmporteerd. De lijst bevat Azure AD-gebruikers die momenteel geen gebruikers in deze omgeving zijn.
4. Selecteer **Gebruikers importeren**.
5. Selecteer **Sluiten**.

> [!NOTE]
> De waarde voor het veld **Bedrijf** wordt ingesteld op basis van het bedrijf van de huidige sessie voor de beheerder. Na de import moet u rollen en organisaties toewijzen voor zover van toepassing. Zie [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie. Soms is het ook nodig dat u de gebruiker aan een **Persoon** koppelt en gebruikersopties, zoals taal, bijwerkt.

## <a name="manually-add-a-new-user"></a>Een nieuwe gebruiker handmatig toevoegen
1. Ga naar **Systeembeheer** \> **Gebruikers** \> **Gebruikers**.
2. Selecteer **Nieuw** in het actievenster.
3. Voer in het veld **Gebruikers-id** een unieke id voor de gebruiker in.   
4. Voer in het veld **Gebruikersnaam** de naam van de gebruiker in.  
5. In het veld **Provider**:
 - Voor interne gebruikers gebruikt u de standaardwaarde. Bijvoorbeeld de Azure AD-tenant met vooraf https://sts.windows.net/.  
 - Voor niet-Azure AD-gebruikers, zoals Service-2-Service-account, voert u een basistekstwaarde in. Bijvoorbeeld: n.v.t. Met deze waarde voorkomt u onjuiste verificatieoproepen die kunnen leiden tot fouten als een geldige identiteitsproviderwaarde wordt gebruikt.  
 - Voor externe gebruikers of gastgebruikers voegt u de naam van de Azure AD-tenant toe na https://sts.windows.net/.
6. Voer in het veld **E-mail** de volledige e-mailnaam/user principal name in.  
7. Selecteer in het veld **Bedrijf** het standaardopstartbedrijf voor de gebruiker. 
8. Selecteer **Opslaan**.

De waarden voor identiteitsprovider en telemetrie-ID worden bijgewerkt op basis van een [Microsoft Graph](/graph/overview)-oproep wanneer de gebruikersrecord wordt opgeslagen. De telemetrie-ID is gebaseerd op de object-ID/Security Identifier (SID) van de gebruiker in Azure AD.

> [!NOTE]
> Nadat u een gebruiker hebt toevoegt, moet u voor zover van toepassing rollen en organisaties toewijzen. Zie [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie. Soms is het ook nodig dat u de gebruiker aan een **Persoon** koppelt en **Gebruikersopties**, zoals taal, bijwerkt.

## <a name="change-a-user-id"></a>Een gebruikers-ID wijzigen
Als u een gebruikers-ID wilt wijzigen, moet u de naam van de sleutel in de database wijzigen. Wanneer u een gebruikers-ID wijzigt met deze procedure, worden alle gerelateerde gebruikersinstellingen gewijzigd om de nieuwe gebruikers-ID te gebruiken. Zo wordt de gebruiksinformatie in de tabel **SysLastValue** bijgewerkt om te verwijzen naar de nieuwe gebruikers-ID.

> [!NOTE]
> De gebruikers-ID is de primaire sleutel van de tabel met gebruikersgegevens. Het wijzigen van de naam van de primaire sleutel kan even duren voor bestaande gebruikers, omdat alle verwijzingen naar de sleutel ook in de database worden bijgewerkt. 

1. Ga naar **Systeembeheer \> Gebruikers \> Gebruikers**.
2. Selecteer een gebruiker in de lijst en selecteer **Opties\> Recordgegevens**.
3. Selecteer **Naam wijzigen**.
4. Voer een nieuwe unieke waarde voor de gebruikers-ID in en kies **OK**. 
5. Selecteer **Ja** om te bevestigen.

## <a name="additional-resources"></a>Aanvullende bronnen

Zie [B2B-gebruikers exporteren naar Azure AD](../implement-b2b.md) voor meer opties voor het implementeren van B2B-gebruikers.

Zie [Vooraf geconfigureerde systeemaccounts](../pre-configured-system-accounts.md) voor informatie over vooraf geconfigureerde systeemaccounts


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]