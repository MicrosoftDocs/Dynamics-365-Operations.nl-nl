---
title: Gebruiker niet gevonden in personenkiezer in Attract of Onboard
description: In dit onderwerp wordt uitgelegd wat u moet doen wanneer gebruikers in de bedrijfstenant niet worden weergegeven in de personenkiezer in de Dynamics 365 for Talent Attract- of Onboard-toepassingen.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/19/2019
ms.locfileid: "859500"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a>Azure Active Directory-gebruikers niet gevonden in personenkiezer

[!include [banner](includes/banner.md)]

## <a name="issue"></a>Uitgifte

Bepaalde geldige gebruikers in Microsoft Azure Active Directory (Azure AD) voor de tenant worden niet weergegeven bij het zoeken naar de naam in de personenkiezer in de Dynamics 365 for Talent Attract- of Onboard-toepassingen.

## <a name="cause"></a>Oorzaak

Bepaalde gebruikerstypen worden momenteel niet ondersteund in de Attract- en Onboard-toepassingen. Controleer of de gebruiker niet een Azure AD Business-to-Business (B2B)-gastgebruiker is. Gegevens over het "Gebruikerstype" vindt u in het Azure Active Directory-blad van de Azure-portal.

Zie voor meer informatie over Azure B2B [Wat is gastgebruikerstoegang in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).

Voor niet-B2B-gebruikers geldt dat er bepaalde gebruikers zijn die mogelijk een onvolledige eigenschap "Gebruikerstype" in het object **Gebruiker** hebben. Dit kan worden geverifieerd en opgelost met de module Azure AD Powershell. Zie [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0) voor meer informatie.

## <a name="resolution"></a>Oplossing

Als u de volgende stappen wilt uitvoeren om het probleem te verhelpen, moet u over de rechten "Globale beheerder" in de Azure Active Directory-tenant beschikken of over rechten voor **User.ReadWrite.All**.

Om het "Gebruikerstype" te verifiëren voor de betreffende gebruiker.

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
De opdracht retourneert de volgende gegevens.
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
Let op de eigenschap **UserType** voor de gebruiker. Als **UserType** leeg is, bijvoorbeeld niet "Lid" of "Gast", werk dan **UserType** met de volgende opdracht bij.

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
