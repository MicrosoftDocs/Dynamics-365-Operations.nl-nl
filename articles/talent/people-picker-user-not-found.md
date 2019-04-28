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
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="44366-103">Azure Active Directory-gebruikers niet gevonden in personenkiezer</span><span class="sxs-lookup"><span data-stu-id="44366-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="44366-104">Uitgifte</span><span class="sxs-lookup"><span data-stu-id="44366-104">Issue</span></span>

<span data-ttu-id="44366-105">Bepaalde geldige gebruikers in Microsoft Azure Active Directory (Azure AD) voor de tenant worden niet weergegeven bij het zoeken naar de naam in de personenkiezer in de Dynamics 365 for Talent Attract- of Onboard-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="44366-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="44366-106">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="44366-106">Cause</span></span>

<span data-ttu-id="44366-107">Bepaalde gebruikerstypen worden momenteel niet ondersteund in de Attract- en Onboard-toepassingen.</span><span class="sxs-lookup"><span data-stu-id="44366-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="44366-108">Controleer of de gebruiker niet een Azure AD Business-to-Business (B2B)-gastgebruiker is.</span><span class="sxs-lookup"><span data-stu-id="44366-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="44366-109">Gegevens over het "Gebruikerstype" vindt u in het Azure Active Directory-blad van de Azure-portal.</span><span class="sxs-lookup"><span data-stu-id="44366-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="44366-110">Zie voor meer informatie over Azure B2B [Wat is gastgebruikerstoegang in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="44366-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="44366-111">Voor niet-B2B-gebruikers geldt dat er bepaalde gebruikers zijn die mogelijk een onvolledige eigenschap "Gebruikerstype" in het object **Gebruiker** hebben.</span><span class="sxs-lookup"><span data-stu-id="44366-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="44366-112">Dit kan worden geverifieerd en opgelost met de module Azure AD Powershell.</span><span class="sxs-lookup"><span data-stu-id="44366-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="44366-113">Zie [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="44366-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="44366-114">Oplossing</span><span class="sxs-lookup"><span data-stu-id="44366-114">Resolution</span></span>

<span data-ttu-id="44366-115">Als u de volgende stappen wilt uitvoeren om het probleem te verhelpen, moet u over de rechten "Globale beheerder" in de Azure Active Directory-tenant beschikken of over rechten voor **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="44366-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="44366-116">Om het "Gebruikerstype" te verifiëren voor de betreffende gebruiker.</span><span class="sxs-lookup"><span data-stu-id="44366-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="44366-117">De opdracht retourneert de volgende gegevens.</span><span class="sxs-lookup"><span data-stu-id="44366-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="44366-118">Let op de eigenschap **UserType** voor de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="44366-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="44366-119">Als **UserType** leeg is, bijvoorbeeld niet "Lid" of "Gast", werk dan **UserType** met de volgende opdracht bij.</span><span class="sxs-lookup"><span data-stu-id="44366-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
