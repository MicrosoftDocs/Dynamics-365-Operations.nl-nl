---
title: Azure Active Directory-verificatie inschakelen voor POS-aanmelding
description: In dit onderwerp wordt uitgelegd hoe u de aanmeldingservaring voor het Microsoft Dynamics 365 Commerce-verkooppunt (POS) zo configureert dat Azure Active Directory-verificatie wordt gebruikt.
author: boycezhu
manager: annbe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: d6073a04814adf8237b4caa952b31b011f4b34bf
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982735"
---
# <a name="enable-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="892c4-103">Azure Active Directory-verificatie inschakelen voor POS-aanmelding</span><span class="sxs-lookup"><span data-stu-id="892c4-103">Enable Azure Active Directory authentication for POS sign-in</span></span>
[!include [banner](includes/banner.md)]


<span data-ttu-id="892c4-104">Veel klanten die Microsoft Dynamics 365 Commerce gebruiken, gebruiken ook andere Microsoft-cloudservices en ze kunnen Azure Active Directory (Azure AD) gebruiken om gebruikersreferenties voor deze services te beheren.</span><span class="sxs-lookup"><span data-stu-id="892c4-104">Many customers who use Microsoft Dynamics 365 Commerce also use other Microsoft cloud services, and they might use Azure Active Directory (Azure AD) to manage user credentials for those services.</span></span> <span data-ttu-id="892c4-105">In deze gevallen willen de klanten mogelijk dezelfde Azure AD-account gebruiken voor verschillende toepassingen.</span><span class="sxs-lookup"><span data-stu-id="892c4-105">In those cases, the customers might want to use the same Azure AD account across applications.</span></span> <span data-ttu-id="892c4-106">In dit onderwerp wordt uitgelegd hoe u de aanmeldingservaring voor het Commerce-verkooppunt (POS) zo configureert dat Azure AD-verificatie wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="892c4-106">This topic explains how to configure the Commerce point of sale (POS) sign-in experience to use Azure AD authentication.</span></span>

## <a name="configure-azure-ad-authentication"></a><span data-ttu-id="892c4-107">Azure AD-verificatie configureren</span><span class="sxs-lookup"><span data-stu-id="892c4-107">Configure Azure AD authentication</span></span>

<span data-ttu-id="892c4-108">Als u Azure AD beschikbaar wilt maken als de verificatiemethode voor POS-aanmelding voor een winkel, moet u de instellingen van het functionaliteitsprofiel van de winkel configureren en deze instelling vervolgens toepassen op POS-clients.</span><span class="sxs-lookup"><span data-stu-id="892c4-108">To make Azure AD available as the authentication method for POS sign-in for a store, you must configure the settings of the store's functionality profile and then apply those setting to POS clients.</span></span>

<span data-ttu-id="892c4-109">Volg deze stappen om een functionaliteitsprofiel te configureren.</span><span class="sxs-lookup"><span data-stu-id="892c4-109">To configure a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="892c4-110">Ga naar **Retail en Commerce** \> **Kanaalinstellingen** \> **POS-instellingen** \> **POS-profielen** \> **Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="892c4-110">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profiles** \> **Functionality profiles**.</span></span>
1. <span data-ttu-id="892c4-111">Selecteer het functionaliteitsprofiel dat u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="892c4-111">Select the functionality profile to change.</span></span>
1. <span data-ttu-id="892c4-112">Wijzig op het sneltabblad **Functies** in de sectie **Aanmelding POS-personeel** de waarde van het veld **Verificatiemethode bij aanmelding** van **Personeels-id en wachtwoord** in **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="892c4-112">On the **Functions** FastTab, in the **POS staff logon** section, change the value of the **Logon Authentication Method** field from **Personnel ID and Password** to **Azure Active Directory**.</span></span>

<span data-ttu-id="892c4-113">Standaard gebruiken alle functionaliteitsprofielen **Personeels-id en wachtwoord** als de POS-verificatiemethode.</span><span class="sxs-lookup"><span data-stu-id="892c4-113">By default, all functionality profiles use **Personnel ID and Password** as the POS authentication method.</span></span> <span data-ttu-id="892c4-114">Daarom moet u de waarde van het veld **Verificatiemethode bij aanmelding** wijzigen als u Azure AD wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="892c4-114">Therefore, you must change the value of the **Logon Authentication Method** field if you want to use Azure AD.</span></span> <span data-ttu-id="892c4-115">Elke detailhandelwinkel die is gekoppeld aan het geselecteerde functionaliteitsprofiel wordt beïnvloed door deze wijziging.</span><span class="sxs-lookup"><span data-stu-id="892c4-115">Every retail store that is linked to the selected functionality profile will be affected by this change.</span></span>

<span data-ttu-id="892c4-116">Voer de volgende stappen uit om de instellingen toe te passen op POS-clients.</span><span class="sxs-lookup"><span data-stu-id="892c4-116">To apply the settings to POS clients, follow these steps.</span></span>

1. <span data-ttu-id="892c4-117">Ga naar **Retail en Commerce** \> **Retail en Commerce IT** \> **Distributieplanning**.</span><span class="sxs-lookup"><span data-stu-id="892c4-117">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
1. <span data-ttu-id="892c4-118">Voer de distributieplanning **1070** (**Kanaalconfiguratie**) uit.</span><span class="sxs-lookup"><span data-stu-id="892c4-118">Run the **1070** (**Channel configuration**) distribution schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="892c4-119">Voor Azure AD-verificatie is een internetverbinding vereist.</span><span class="sxs-lookup"><span data-stu-id="892c4-119">Azure AD authentication requires an internet connection.</span></span> <span data-ttu-id="892c4-120">Het werkt niet als POS zich in de offlinemodus bevindt.</span><span class="sxs-lookup"><span data-stu-id="892c4-120">It won't work when POS is in offline mode.</span></span>
> 
> <span data-ttu-id="892c4-121">Momenteel wordt door de functie **Overschrijving door manager** Azure AD niet als verificatiemethode ondersteund.</span><span class="sxs-lookup"><span data-stu-id="892c4-121">Currently, the **Manager override** function doesn't support Azure AD as an authentication method.</span></span> <span data-ttu-id="892c4-122">Een operator-id en wachtwoord zijn vereist, zelfs als Azure AD is geconfigureerd als verificatiemethode voor POS-aanmelding.</span><span class="sxs-lookup"><span data-stu-id="892c4-122">An operator ID and password are required even if Azure AD is configured as the authentication method for POS sign-in.</span></span>

## <a name="associate-an-azure-ad-account-with-a-worker"></a><span data-ttu-id="892c4-123">Een Azure AD-account aan een werknemer koppelen</span><span class="sxs-lookup"><span data-stu-id="892c4-123">Associate an Azure AD account with a worker</span></span>

<span data-ttu-id="892c4-124">Voordat een winkelmedewerker een Azure AD-account kan gebruiken om zich aan te melden bij de POS-toepassing, moet de Azure AD-account worden gekoppeld aan die werknemer.</span><span class="sxs-lookup"><span data-stu-id="892c4-124">Before a store worker can use an Azure AD account to sign in to the POS application, the Azure AD account must be associated with that worker.</span></span>

<span data-ttu-id="892c4-125">Voer de volgende stappen uit om een Azure AD-account aan een werknemer te koppelen.</span><span class="sxs-lookup"><span data-stu-id="892c4-125">To associate an Azure AD account with a worker, follow these steps.</span></span>

1. <span data-ttu-id="892c4-126">Ga naar **Detailhandel en commerce** \> **Werknemers** \> **Werknemers**.</span><span class="sxs-lookup"><span data-stu-id="892c4-126">Go to **Retail and Commerce** \> **Employees** \> **Workers**.</span></span>
1. <span data-ttu-id="892c4-127">De gegevenspagina voor een werknemer.</span><span class="sxs-lookup"><span data-stu-id="892c4-127">Open the details page for a worker.</span></span>
1. <span data-ttu-id="892c4-128">Selecteer in het actievenster op het tabblad **Commerce** in de groep **Externe identiteit** de optie **Bestaande identiteit koppelen**.</span><span class="sxs-lookup"><span data-stu-id="892c4-128">On the Action Pane, on the **Commerce** tab, in the **External identity** group, select **Associate existing identity**.</span></span>
1. <span data-ttu-id="892c4-129">Selecteer in het dialoogvenster **Bestaande externe identiteit gebruiken** de optie **Zoeken met behulp van e-mail**, voer een Azure AD-e-mailadres in en selecteer **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="892c4-129">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="892c4-130">Selecteer de Azure AD- account die wordt geretourneerd en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="892c4-130">Select the Azure AD account that is returned, and then select **OK**.</span></span>

<span data-ttu-id="892c4-131">De velden **Alias**, **UPN** en **Externe sub-id** op het tabblad **Commerce** van de pagina met werknemersgegevens wordt ingevuld.</span><span class="sxs-lookup"><span data-stu-id="892c4-131">The **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

> [!NOTE]
> <span data-ttu-id="892c4-132">Nadat een werknemerrecord is bijgewerkt, bijvoorbeeld als een nieuwe Azure AD-account wordt gekoppeld, een wachtwoord wordt gewijzigd of een adresboek van een werknemer wordt bijgewerkt, wordt aangeraden om distributieplanning **1060** (**personeel**) uit te voeren om de meest recente personeelsgegevens naar het kanaal te synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="892c4-132">After a worker record is updated, for example if a new Azure AD account is associated, a password is changed, or an employee address book is updated, it’s recommended that you run **1060** (**Staff**) distribution schedule to synchronize the latest staff information to the channel.</span></span> <span data-ttu-id="892c4-133">Op die manier kan de POS-toepassing de juiste gegevens ophalen voor gebruikersverificatie en verificatiecontrole.</span><span class="sxs-lookup"><span data-stu-id="892c4-133">That way, the POS application can fetch the correct data for user authentication and authorization check.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="892c4-134">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="892c4-134">Additional resources</span></span>

[<span data-ttu-id="892c4-135">Uitgebreide aanmeldingsfunctionaliteit instellen voor MPOS en Cloud POS</span><span class="sxs-lookup"><span data-stu-id="892c4-135">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="892c4-136">Een functionaliteitsprofiel voor detailhandel maken</span><span class="sxs-lookup"><span data-stu-id="892c4-136">Create a retail functionality profile</span></span>](retail-functionality-profile.md)

[<span data-ttu-id="892c4-137"> Een medewerker configureren</span><span class="sxs-lookup"><span data-stu-id="892c4-137">Configure a worker</span></span>](https://docs.microsoft.com/dynamics365/commerce/tasks/worker)
