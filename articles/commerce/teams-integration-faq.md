---
title: Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams
description: Dit onderwerp bevat antwoorden op veelgestelde vragen met betrekking tot integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bf9aebb1c8ba7cf4fee3f0471a10872de1e23ce6
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908851"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="96b74-103">Veelgestelde vragen over integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="96b74-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96b74-104">Dit onderwerp bevat antwoorden op veelgestelde vragen met betrekking tot integratie van Microsoft Dynamics 365 Commerce en Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="96b74-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="96b74-105">Wie in de winkel wordt eigenaar van een team bij het inrichtgen van Teams vanuit Commerce?</span><span class="sxs-lookup"><span data-stu-id="96b74-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="96b74-106">Alle winkelmanagers worden automatisch toegevoegd als eigenaren aan de bijbehorende teamgroep, zodat ze bewerkingen kunnen uitvoeren, zoals het toevoegen van een privékanaal en het toevoegen of verwijderen van leden.</span><span class="sxs-lookup"><span data-stu-id="96b74-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="96b74-107">Hoe wijs ik de rol "communicatiemanager" toe aan een werknemer in Commerce Headquarters?</span><span class="sxs-lookup"><span data-stu-id="96b74-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="96b74-108">Communicatiemanagers in Microsoft Teams kunnen takenlijsten maken en publiceren.</span><span class="sxs-lookup"><span data-stu-id="96b74-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="96b74-109">Aan organisatiewerknemers die communicatiemanager moeten worden, moet de rol "Taakbeheer detailhandel" worden toegewezen in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="96b74-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="96b74-110">Volg deze stappen om de rol Taakbeheer detailhandel toe te wijzen aan een werknemer in Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="96b74-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="96b74-111">Ga naar **Detailhandel en commerce \> Werknemers \> Gebruikers**.</span><span class="sxs-lookup"><span data-stu-id="96b74-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="96b74-112">Selecteer een werknemer.</span><span class="sxs-lookup"><span data-stu-id="96b74-112">Select an employee.</span></span>
1. <span data-ttu-id="96b74-113">Selecteer op het sneltabblad **Rollen van gebruiker** op **Rollen toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="96b74-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="96b74-114">Selecteer in het dialoogvenster **Rollen toewijzen aan gebruiker** de rol **Taakbeheer detailhandel** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="96b74-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="96b74-115">Hoe maak ik een specifieke organisatiehiërarchie beschikbaar om te uploaden naar Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="96b74-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="96b74-116">In Commerce Headquarters is de hiërarchie van elke organisatie aan een of meer doelen gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="96b74-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="96b74-117">Zorg ervoor dat aan de hiërarchie die u wilt inrichten in Microsoft Teams het doel **Detailhandelsrapportage** is gekoppeld, zoals in de volgende afbeelding van het voorbeeld wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="96b74-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Voorbeeld van een organisatiehiërarchiedoel in Commerce Headquarters](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="96b74-119">Hoe schakel ik winkelmedewerkers in om zich aan te melden bij Commerce POS (verkooppunt) met Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="96b74-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="96b74-120">Zie [Verificatie voor Azure Active Directory inschakelen voor POS-aanmelding](aad-pos-logon.md) voor informatie over het configureren van de aanmeldingservaring van Commerce POS voor het gebruik van Azure AD.</span><span class="sxs-lookup"><span data-stu-id="96b74-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="96b74-121">Hoe wijs ik winkels en overeenkomende teams toe in Commerce Headquarters als mijn organisatie al teams heeft gemaakt in Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="96b74-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="96b74-122">Zie [Winkels en overeenkomende teams toewijzen indien uw organisatie al bestaande teams heeft in Microsoft Teams](map-stores-existing-teams.md) voor informatie over het toewijzen van winkels en teams.</span><span class="sxs-lookup"><span data-stu-id="96b74-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="96b74-123">Hoe wis ik het Microsoft Graph API-token dat is opgeslagen in de sessieopslag?</span><span class="sxs-lookup"><span data-stu-id="96b74-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="96b74-124">Een gebruiker die is aangemeld bij het POS (verkooppunt) met een Azure Active Directory (Azure AD) rekening moet zich aanmelden via het POS of de toepassing sluiten om de sessieopslag te verwijderen.</span><span class="sxs-lookup"><span data-stu-id="96b74-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="96b74-125">Een aanbevolen procedure is om altijd winkelmedewerkers de POS-terminal te laten vergrendelen of zich af te melden voor een sessie wanneer de terminal niet wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="96b74-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="96b74-126">Wat gebeurt er als een winkel geen winkelmanagers heeft?</span><span class="sxs-lookup"><span data-stu-id="96b74-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="96b74-127">Als een winkel geen managers heeft, wordt er geen teamgroep gemaakt voor de winkel of in Teams.</span><span class="sxs-lookup"><span data-stu-id="96b74-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="96b74-128">Wat gebeurt er als een winkelmanager het bedrijf verlaat?</span><span class="sxs-lookup"><span data-stu-id="96b74-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="96b74-129">Iedereen met de rol Eigenaar kan een nieuwe winkelmanager toevoegen in Commerce Headquarters en Teams opnieuw inrichten, zodat de nieuwe manager over de benodigde rechten in Teams beschikt voor de groep.</span><span class="sxs-lookup"><span data-stu-id="96b74-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="96b74-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="96b74-130">Additional resources</span></span>

[<span data-ttu-id="96b74-131">Overzicht van integratie van Dynamics 365 Commerce en Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="96b74-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="96b74-132">Integratie van Dynamics 365 Commerce en Microsoft Teams inschakelen</span><span class="sxs-lookup"><span data-stu-id="96b74-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="96b74-133">Microsoft Teams inrichten vanuit Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="96b74-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="96b74-134">Taakbeheer synchroniseren tussen Microsoft Teams en Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="96b74-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="96b74-135">Gebruikersrollen beheren in Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="96b74-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="96b74-136">Winkels en teams toewijzen als er reeds bestaande teams in Microsoft Teams zijn</span><span class="sxs-lookup"><span data-stu-id="96b74-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
