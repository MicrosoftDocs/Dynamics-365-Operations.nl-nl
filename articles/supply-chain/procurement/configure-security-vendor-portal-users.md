---
title: Gebruikersbeveiliging leveranciersportal
description: In dit artikel wordt beschreven hoe u beveiliging instelt voor externe leveranciers die de leveranciersportal gebruiken. Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.
author: kamaybac
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8539837adc5c5e775d073f142f00afc9f14de669
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807843"
---
# <a name="vendor-portal-user-security"></a><span data-ttu-id="210b0-104">Gebruikersbeveiliging in leveranciersportal</span><span class="sxs-lookup"><span data-stu-id="210b0-104">Vendor portal user security</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="210b0-105">In dit artikel wordt beschreven hoe u beveiliging instelt voor externe leveranciers die de leveranciersportal gebruiken.</span><span class="sxs-lookup"><span data-stu-id="210b0-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="210b0-106">Deze informatie geldt alleen voor de versies van februari 2016 en mei 2016 van Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="210b0-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="210b0-107">De functionaliteit Leveranciersportal is vervangen door de verbeterde functionaliteit voor leverancierssamenwerking in Dynamics 365 for Operations versie 1611.</span><span class="sxs-lookup"><span data-stu-id="210b0-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="210b0-108">Meer informatie over het instellen van beveiliging voor leverancierssamenwerking vindt u in [Samenwerking met leveranciers instellen en onderhouden](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="210b0-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="210b0-109">De leveranciersportal maakt een beperkte set informatie over inkooporders (IOs) beschikbaar voor externe leveranciers.</span><span class="sxs-lookup"><span data-stu-id="210b0-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="210b0-110">Het is belangrijk dat u correct de machtigingen van gebruikers instelt voor de leveranciersportal in Microsoft Dynamics AX, zodat leveranciers geen onbedoelde toegang tot extra informatie in uw Dynamics AX-installatie hebben.</span><span class="sxs-lookup"><span data-stu-id="210b0-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="210b0-111">**Belangrijk:** In tegenstelling tot andere gebruikers moeten externe leveranciers niet de rol **SystemUser** hebben.</span><span class="sxs-lookup"><span data-stu-id="210b0-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="210b0-112">De rol **SystemUser** geeft toegang tot een set bevoegdheden die niet geschikt zijn voor externe gebruikers.</span><span class="sxs-lookup"><span data-stu-id="210b0-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="210b0-113">Het instellen van een Leveranciersportal-gebruiker</span><span class="sxs-lookup"><span data-stu-id="210b0-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="210b0-114">Voordat u een gebruikersaccount maakt voor iemand die de leveranciersportal zal gebruiken, moet u de leverancier instellen op leveranciersportalsamenwerking.</span><span class="sxs-lookup"><span data-stu-id="210b0-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="210b0-115">Gebruik het veld **Inkoopordersamenwerking** op het tabblad **Algemeen** op de pagina **Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="210b0-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="210b0-116">Externe leveranciers die de leveranciersportal gebruiken, moeten de volgende instelling hebben:</span><span class="sxs-lookup"><span data-stu-id="210b0-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="210b0-117">Een Microsoft Azure Active Directory (AAD)-gebruikersaccount moet worden geregistreerd voor de leverancier op de pagina **Gebruikers** in Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="210b0-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="210b0-118">De leverancier moet de beveiligingsrol **Leverancier (extern)** hebben, niet de rol **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="210b0-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="210b0-119">**Opmerking**: de rol **SystemUser** wordt automatisch verleend als u een nieuw gebruikersaccount in Dynamics AX maakt.</span><span class="sxs-lookup"><span data-stu-id="210b0-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="210b0-120">Daarom moet u die rol verwijderen en het waarschuwingsbericht bevestigen dat u ontvangt.</span><span class="sxs-lookup"><span data-stu-id="210b0-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="210b0-121">De leveranciersgebruiker mag geen toestemming geven voor het toevoegen van extra velden vanuit de inkoopordertabellen aan hun weergave van de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="210b0-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="210b0-122">Op het **Persoonlijke instellingen** tabblad, op het **Gebruikers** tabblad, stelt u de optie **Expliciete aanpassing toegestaan** voor de gebruiker in op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="210b0-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="210b0-123">De gebruikersaccount moet zijn gekoppeld aan een geregistreerde contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="210b0-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="210b0-124">Op de **Gebruikers** pagina, selecteert u een contactpersoon in het **Naam** veld.</span><span class="sxs-lookup"><span data-stu-id="210b0-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="210b0-125">De persoon die u selecteert moet de rol **Contactpersoon** hebben voor de relevante leverancier.</span><span class="sxs-lookup"><span data-stu-id="210b0-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="210b0-126">Als dezelfde persoon toegang nodig heeft tot de Leveranciersportal voor meerdere leverancierrekeningen (voor verschillende rechtspersonen misschien), moet elk van de gebruikersrekeningen van die persoon met dezelfde geregistreerde contactpersoon zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="210b0-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="210b0-127">De rol **Leverancier (extern)** bevat alle basismogelijkheden die zijn vereist om de functionaliteit te gebruiken die in de leveranciersportal beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="210b0-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="210b0-128">Deze instellingen helpen waarborgen dat de gebruikersinterface die de externe gebruiker ziet uitsluitend is gericht op het beoogde scenario.</span><span class="sxs-lookup"><span data-stu-id="210b0-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="additional-resources"></a><span data-ttu-id="210b0-129">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="210b0-129">Additional resources</span></span>
--------

[<span data-ttu-id="210b0-130">Samenwerken met leveranciers met behulp van de leveranciersportal</span><span class="sxs-lookup"><span data-stu-id="210b0-130">Collaborate with vendors by using the Vendor portal</span></span>](collaborate-vendors-vendor-portal.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]