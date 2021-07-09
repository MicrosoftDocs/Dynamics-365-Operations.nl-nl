---
title: Power BI inschakelen voor Algemene voorraadboekhouding
description: In dit onderwerp wordt beschreven hoe u deze functie Microsoft Power BIkunt inschakelen voor Algemene voorraadboekhouding.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d7979ed18b98ee6133774cd91bc866d6fca92d5f
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273137"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a><span data-ttu-id="69fbd-103">Power BI inschakelen voor Algemene voorraadboekhouding</span><span class="sxs-lookup"><span data-stu-id="69fbd-103">Enable Power BI for Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="69fbd-104">U kunt tegels, dashboards en rapporten vastzetten vanuit uw [PowerBI.com](https://powerbi.com/)-account naar uw Microsoft Dynamics 365-toepassingswerkgebied.</span><span class="sxs-lookup"><span data-stu-id="69fbd-104">You can pin tiles, dashboards, and reports from your [PowerBI.com](https://powerbi.com/) account to your Microsoft Dynamics 365 application workspace.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69fbd-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="69fbd-105">Prerequisites</span></span>

<span data-ttu-id="69fbd-106">Aan de volgende vereisten moet zijn voldaan voordat u Power BI-rapportage kunt inschakelen:</span><span class="sxs-lookup"><span data-stu-id="69fbd-106">The following prerequisites must be in place before you can enable Power BI reporting:</span></span>

- <span data-ttu-id="69fbd-107">U moet een systeembeheerder zijn in de toepassing Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="69fbd-107">You must be a system administrator in the Dynamics 365 application.</span></span>
- <span data-ttu-id="69fbd-108">U moet over een [PowerBI.com](https://powerbi.com/)-account beschikken.</span><span class="sxs-lookup"><span data-stu-id="69fbd-108">You must have a [PowerBI.com](https://powerbi.com/) account.</span></span>
- <span data-ttu-id="69fbd-109">U moet ten minste één dashboard en één rapport in uw Power BI-account hebben.</span><span class="sxs-lookup"><span data-stu-id="69fbd-109">You must have at least one dashboard and one report in your Power BI account.</span></span>
- <span data-ttu-id="69fbd-110">U moet een beheerder zijn voor uw Azure AD-account (Azure Active Directory).</span><span class="sxs-lookup"><span data-stu-id="69fbd-110">You must be an administrator for your Azure Active Directory (Azure AD) account.</span></span>
- <span data-ttu-id="69fbd-111">Het Azure AD-domein moet hetzelfde domein zijn dat u hebt gebruikt voor uw [PowerBI.com](https://powerbi.com/)-account.</span><span class="sxs-lookup"><span data-stu-id="69fbd-111">The Azure AD domain must be the same domain that you used for your [PowerBI.com](https://powerbi.com/) account.</span></span>

## <a name="setup"></a><span data-ttu-id="69fbd-112">Instelling</span><span class="sxs-lookup"><span data-stu-id="69fbd-112">Setup</span></span>

<span data-ttu-id="69fbd-113">Volg deze stappen voor het instellen van de Power BI-integratie.</span><span class="sxs-lookup"><span data-stu-id="69fbd-113">To set up the Power BI integration, follow these steps.</span></span>

1. <span data-ttu-id="69fbd-114">Meld u aan bij [Microsoft Dynamics LCS (LifeCycle Services)](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="69fbd-114">Sign in to [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="69fbd-115">Ga naar de **Bibliotheek voor gedeelde activa**, selecteer een **Power BI-rapportmodel** als het activatype en download het pakket **Global Inventory Accounting** (Algemene voorraadboekhouding).</span><span class="sxs-lookup"><span data-stu-id="69fbd-115">Go to **Shared asset library**, select **Power BI report model** as the asset type, and download the **Global Inventory Accounting** package.</span></span> 
1. <span data-ttu-id="69fbd-116">Meld u aan bij [PowerBI.com](https://app.powerbi.com/) en ga als volgt te werk om het rapportbestand **Algemene voorraadboekhouding** van Power BI te uploaden:</span><span class="sxs-lookup"><span data-stu-id="69fbd-116">Sign in to [PowerBI.com](https://app.powerbi.com/), and upload the **Global Inventory Accounting** Power BI report file by following these steps:</span></span>

    1. <span data-ttu-id="69fbd-117">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-117">Select **New**.</span></span>
    1. <span data-ttu-id="69fbd-118">Selecteer **Een bestand uploaden**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-118">Select **Upload a file**.</span></span>
    1. <span data-ttu-id="69fbd-119">Selecteer het Power BI-rapportbestand **Algemene voorraadboekhouding**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-119">Select the **Global Inventory Accounting** Power BI report file.</span></span>

1. <span data-ttu-id="69fbd-120">Configureer het Power BI-rapportbestand **Algemene voorraadboekhouding** als volgt:</span><span class="sxs-lookup"><span data-stu-id="69fbd-120">Configure the **Global Inventory Accounting** Power BI report by following these steps:</span></span>

    1. <span data-ttu-id="69fbd-121">Ga naar **Mijn werkruimte**, zoek de gegevensset voor Algemene voorraadboekhouding en selecteer vervolgens **Instellingen** in het menu **Opties**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-121">Go to **My workspace**, find the dataset for Global Inventory Accounting, and then, on the **Options** menu, select **Settings**.</span></span>
    1. <span data-ttu-id="69fbd-122">Vouw in **Instellingen voor Algemene voorraadboekhouding** de optie **Parameters** uit en werk alle parameters waar nodig bij.</span><span class="sxs-lookup"><span data-stu-id="69fbd-122">In **Settings for Global inventory accounting**, expand **Parameters**, and update all parameters as required.</span></span>

1. <span data-ttu-id="69fbd-123">Registreer de toepassing zoals beschreven in [Integratie van PowerBI.com configureren ](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span><span class="sxs-lookup"><span data-stu-id="69fbd-123">Register the application as described in [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process).</span></span>
1. <span data-ttu-id="69fbd-124">Integreer het Power BI-rapportbestand **Algemene voorraadboekhouding** als volgt in Dynamics 365 Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="69fbd-124">Integrate the **Global Inventory Accounting** Power BI report file into Dynamics 365 Supply Chain Management by following these steps:</span></span>

    1. <span data-ttu-id="69fbd-125">Ga naar **Systeembeheer \> Instellingen \> Configuratie PowerBI.com**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-125">Go to **System administration \> Setup \> PowerBI.com configuration**.</span></span>
    1. <span data-ttu-id="69fbd-126">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-126">Select **Edit**.</span></span>
    1. <span data-ttu-id="69fbd-127">Selecteer **Integratie PowerBI.com inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-127">Select **Enable PowerBI.Com integration**.</span></span>
    1. <span data-ttu-id="69fbd-128">Voer in het veld **Toepassings-id** de volgende id in:</span><span class="sxs-lookup"><span data-stu-id="69fbd-128">In the **Application ID** field, enter the application ID.</span></span>
    1. <span data-ttu-id="69fbd-129">Voer in het veld **Toepassingssleutel** de volgende sleutel in:</span><span class="sxs-lookup"><span data-stu-id="69fbd-129">In the **Application key** field, enter the application key.</span></span>
    1. <span data-ttu-id="69fbd-130">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-130">Select **Save**.</span></span>

1. <span data-ttu-id="69fbd-131">Vernieuw de pagina zodat het dialoogvenster voor aanmelding bij Power BI wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="69fbd-131">Refresh the page so that the Power BI sign-in dialog box appears.</span></span>
1. <span data-ttu-id="69fbd-132">Selecteer op het tabblad **Opties** de optie **Rapportcatalogus openen** en selecteer vervolgens het Power BI--rapportbestand **Algemene voorraadboekhouding** dat u eerder hebt geüpload.</span><span class="sxs-lookup"><span data-stu-id="69fbd-132">On the **Options** tab, select **Open report catalog**, and then select the **Global Inventory Accounting** Power BI report file that you uploaded earlier.</span></span>
1. <span data-ttu-id="69fbd-133">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="69fbd-133">Refresh the page.</span></span> <span data-ttu-id="69fbd-134">Als het goed is, ziet u dat uw rapport is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="69fbd-134">You should see that your report has been added.</span></span>
1. <span data-ttu-id="69fbd-135">Selecteer onder **Power BI-rapporten** de koppeling **Algemene voorraadboekhouding**.</span><span class="sxs-lookup"><span data-stu-id="69fbd-135">Under **Power BI reports**, select the **Global Inventory Accounting** link.</span></span>

<span data-ttu-id="69fbd-136">Zie [Integratie van PowerBI.com configureren](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="69fbd-136">For more information, see [Configure PowerBI.com integration](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).</span></span>
