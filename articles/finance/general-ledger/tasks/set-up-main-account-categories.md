---
title: Categorieën van hoofdrekening instellen
description: In dit onderwerp wordt uitgelegd hoe u hoofdrekeningcategorieën instelt in Dynamics 365 Finance.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccountCategory, MainAccountCategoryLink
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e0a015283064af2287013bccc065b4467a308c5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144784"
---
# <a name="set-up-main-account-categories"></a><span data-ttu-id="80c61-103">Categorieën van hoofdrekening instellen</span><span class="sxs-lookup"><span data-stu-id="80c61-103">Set up main account categories</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="80c61-104">In dit onderwerp wordt uitgelegd hoe u hoofdrekeningcategorieën instelt.</span><span class="sxs-lookup"><span data-stu-id="80c61-104">This topic explains how to set up main account categories.</span></span> <span data-ttu-id="80c61-105">De categorieën van hoofdrekening worden gebruikt voor de standaardrapporten in de financiële rapportage en in Power BI.</span><span class="sxs-lookup"><span data-stu-id="80c61-105">Main account categories are used for the default reports in financial reporting and in Power BI.</span></span> <span data-ttu-id="80c61-106">U kunt de categorieën van hoofdrekening die standaard zijn gemaakt een andere naam geven maar niet verwijderen.</span><span class="sxs-lookup"><span data-stu-id="80c61-106">Main account categories that are created by default can be renamed but not deleted.</span></span> <span data-ttu-id="80c61-107">De categorieën van aanvullende rekening kunnen worden gemaakt en gebruikt voor rapportage- en analysedoeleinden.</span><span class="sxs-lookup"><span data-stu-id="80c61-107">Additional account categories can be created and used for reporting and analysis purposes.</span></span> <span data-ttu-id="80c61-108">In dit onderwerp wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80c61-108">This topic uses the USMF demo company.</span></span>

## <a name="create-a-main-account-category"></a><span data-ttu-id="80c61-109">Een categorie van hoofdrekening maken</span><span class="sxs-lookup"><span data-stu-id="80c61-109">Create a main account category</span></span>
1. <span data-ttu-id="80c61-110">Ga in het navigatievenster naar **Modules > Grootboek > Rekeningschema > Rekeningen > Categorieën van hoofdrekening**.</span><span class="sxs-lookup"><span data-stu-id="80c61-110">In the navigation pane, go to **Modules > General Ledger > Chart of accounts > Accounts > Main account categories**.</span></span>
2. <span data-ttu-id="80c61-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="80c61-111">Select **New**.</span></span>
3. <span data-ttu-id="80c61-112">Voer in het veld **Categorie van hoofdrekening** een unieke naam in.</span><span class="sxs-lookup"><span data-stu-id="80c61-112">In the **Main account category** field, enter a unique name.</span></span>
4. <span data-ttu-id="80c61-113">Typ in het veld **Beschrijving** een beschrijving voor de categorie van de hoofdrekening.</span><span class="sxs-lookup"><span data-stu-id="80c61-113">In the **Description field**, enter a description for the main account category.</span></span>
5. <span data-ttu-id="80c61-114">Selecteer in het veld **Hoofdrekeningtype** het hoofdrekeningtype dat u aan de categorie wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="80c61-114">In the **Main account type** field, select the main account type that will be linked to the category.</span></span>

## <a name="link-main-accounts-to-account-category"></a><span data-ttu-id="80c61-115">Hoofdrekeningen aan een rekeningcategorie koppelen</span><span class="sxs-lookup"><span data-stu-id="80c61-115">Link main accounts to account category</span></span>
1. <span data-ttu-id="80c61-116">Klik op **Hoofdrekeningen koppelen**.</span><span class="sxs-lookup"><span data-stu-id="80c61-116">Click **Link main accounts**.</span></span>
2. <span data-ttu-id="80c61-117">Selecteer in de lijst de hoofdrekeningen die u aan de hoofdrekeningcategorie wilt toewijzen door de selectievakjes in de kolom **Gekoppeld** in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="80c61-117">In the list, select the main accounts to assign to the main account category by checking the boxes in the **Linked** column.</span></span> <span data-ttu-id="80c61-118">Door het toewijzen van hoofdrekeningen aan een categorie van hoofdrekening worden de saldi van de rekeningen samengevoegd wanneer die categorie voor financiële rapportage en analyse wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="80c61-118">Assigning main accounts to a main account category will aggregate the balances of the accounts when that category is used for financial reporting and analysis.</span></span>  
3. <span data-ttu-id="80c61-119">Schakel de optie **Gekoppeld** in of uit om de hoofdrekeningen te kiezen.</span><span class="sxs-lookup"><span data-stu-id="80c61-119">Select or clear the **Linked** option to choose the main accounts.</span></span>
4. <span data-ttu-id="80c61-120">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="80c61-120">Select **OK**.</span></span>
5. <span data-ttu-id="80c61-121">Selecteer **Ja**.</span><span class="sxs-lookup"><span data-stu-id="80c61-121">Select **Yes**.</span></span>
