---
title: Geleende activa
description: In dit onderwerp wordt beschreven hoe u geleende activa registreert in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 07472188051aea7084142cc417c6d725462cf4f9
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205248"
---
# <a name="asset-loans"></a><span data-ttu-id="3a7c7-103">Geleende activa</span><span class="sxs-lookup"><span data-stu-id="3a7c7-103">Asset loans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="3a7c7-104">Als uw bedrijf activa ontvangt voor reparatie- of onderhoudstaken van interne vestigingen of klanten, en als u activa tijdelijk uitleent aan die vestigingen of klanten, kan Activabeheer de geleende activa volgen.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-104">If your company receives assets for repair or maintenance jobs from either internal locations or customers, and if you temporarily loan assets to those locations or customers, Asset Management can track the asset loans.</span></span>

## <a name="register-asset-loans-on-a-maintenance-request"></a><span data-ttu-id="3a7c7-105">Geleende activa registreren op een onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="3a7c7-105">Register asset loans on a maintenance request</span></span>

1. <span data-ttu-id="3a7c7-106">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-106">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="3a7c7-107">Selecteer het onderhoudsverzoek waarvoor u een geleend activum wilt registreren en selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-107">Select the maintenance request to register an asset loan on, and then select **Edit**.</span></span>
3. <span data-ttu-id="3a7c7-108">Op de pagina **Aanvragen** selecteert u **Geleend activum verzenden**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-108">On the **Request** page, select **Send loan asset**.</span></span>
4. <span data-ttu-id="3a7c7-109">Selecteer het activum en voer de verwachte retourdatum in.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-109">Select the asset, and enter the expected return date.</span></span>
5. <span data-ttu-id="3a7c7-110">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-110">Select **OK**.</span></span>

> [!NOTE]
> - <span data-ttu-id="3a7c7-111">U kunt een geleend activum alleen verzenden als een activum van hetzelfde type beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-111">You can send a loan asset only if an asset of the same asset type is available.</span></span>
> - <span data-ttu-id="3a7c7-112">Het activum dat u leent, moet een levenscyclusstatus hebben waarmee het als geleend activum kan worden gebruikt, zoals **InStorage**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-112">The asset that you loan must have an asset lifecycle state that allows it to be used as a loan asset, such as **InStorage**.</span></span> <span data-ttu-id="3a7c7-113">Wanneer het geleende activum wordt geregistreerd, wordt de levenscyclusstatus van het activum automatisch bijgewerkt naar bijvoorbeeld **OnLoan**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-113">When the asset loan is registered, the asset lifecycle state of the asset is automatically updated to, for example, **OnLoan**.</span></span>

<span data-ttu-id="3a7c7-114">Als u een lijst wilt weergeven met alle activa die u hebt uitgeleend aan andere vestigingen of klanten, selecteert u **Activabeheer** \>**Algemeen** \>**Geleend activum** \>**Alle geleende activa**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-114">To view a list of all the assets that you've loaned to other locations or customers, select **Asset management** \> **Common** \> **Asset loan** \> **All asset loans**.</span></span> <span data-ttu-id="3a7c7-115">Als het selectievakje **Beëindigd** is ingeschakeld voor een activum, is het activum geregistreerd als geretourneerd aan uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-115">If the **Ended** check box is selected for an asset, the asset has been registered as returned to your company.</span></span>

![Onderhoudsaanvragen beheren](media/06-manage-maintenance-requests.png)

<span data-ttu-id="3a7c7-117">Op de pagina **Actieve geleende activa** kunt u een lijst weergeven met alle geleende activa die nog niet aan uw bedrijf zijn geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-117">On the **Active asset loans** page, you can view a list of all the loan assets that haven't yet been returned to your company.</span></span>

## <a name="register-loan-assets-as-returned"></a><span data-ttu-id="3a7c7-118">Geleende activa als geretourneerd registreren</span><span class="sxs-lookup"><span data-stu-id="3a7c7-118">Register loan assets as returned</span></span>

1. <span data-ttu-id="3a7c7-119">Selecteer **Activabeheer** \>**Algemeen** \> **Geleende activa** \> **Actieve geleende activa**. </span><span class="sxs-lookup"><span data-stu-id="3a7c7-119">Select **Asset management** \> **Common** \> **Asset loan** \> **Active asset loans**.</span></span>
2. <span data-ttu-id="3a7c7-120">Selecteer het geleende activum dat u als geretourneerd wilt registreren en selecteer **Geleend activum retourneren**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-120">Select the asset loan to register as returned, and then select **Return asset loan**.</span></span>
3. <span data-ttu-id="3a7c7-121">Voer de datum en de tijd in het veld **Geretourneerd** in.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-121">In the **Returned** field, enter the date and time.</span></span>
4. <span data-ttu-id="3a7c7-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-122">Select **OK**.</span></span>
5. <span data-ttu-id="3a7c7-123">Vernieuw de pagina met de lijst **Actieve geleende activa** en u ziet dat het geleende activum niet meer op de lijst voorkomt.</span><span class="sxs-lookup"><span data-stu-id="3a7c7-123">Refresh the **Active asset loans** list page, and notice that the asset loan no longer appears in the list.</span></span>
