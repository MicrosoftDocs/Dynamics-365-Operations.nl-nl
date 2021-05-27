---
title: U kunt een sjabloon niet toepassen op een vrijgegeven product
description: U kunt een sjabloon niet toepassen op een vrijgegeven product.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ad6efdced9bce924fbf5bc207c92fa2c3a6c79d
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026398"
---
# <a name="you-cant-apply-a-template-to-create-a-released-product"></a><span data-ttu-id="ff960-103">U kunt een sjabloon niet toepassen om een vrijgegeven product te maken</span><span class="sxs-lookup"><span data-stu-id="ff960-103">You can't apply a template to create a released product</span></span>

<span data-ttu-id="ff960-104">KB-nummer: 4612097</span><span class="sxs-lookup"><span data-stu-id="ff960-104">KB number: 4612097</span></span>

## <a name="symptoms"></a><span data-ttu-id="ff960-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="ff960-105">Symptoms</span></span>

<span data-ttu-id="ff960-106">Wanneer u een nieuw vrijgegeven product maakt met behulp van het dialoogvenster **Nieuw vrijgegeven product**, kunt u een sjabloon selecteren.</span><span class="sxs-lookup"><span data-stu-id="ff960-106">When you create a new released product by using the **New released product** dialog box, you can select a template.</span></span> <span data-ttu-id="ff960-107">De sjabloon moet standaardinstellingen geven voor een groot aantal velden van het nieuwe vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="ff960-107">The template is supposed to provide default settings for many fields of the new released product.</span></span> <span data-ttu-id="ff960-108">Sommige of alle velden worden echter niet ingesteld nadat u de sjabloon hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ff960-108">However, some or all of the fields aren't set after you select the template.</span></span>

## <a name="cause"></a><span data-ttu-id="ff960-109">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="ff960-109">Cause</span></span>

<span data-ttu-id="ff960-110">Op veel pagina's in Microsoft Dynamics 365 Supply Chain Management kunt u een sjabloon maken die de begininstellingen vastlegt voor de records die op die pagina's worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ff960-110">Many pages in Microsoft Dynamics 365 Supply Chain Management let you create a template that establishes initial settings for the records that are shown on those pages.</span></span> <span data-ttu-id="ff960-111">U kunt een van deze sjablonen maken door **Recordinfo** te selecteren op het tabblad **Opties** van het actievenster.</span><span class="sxs-lookup"><span data-stu-id="ff960-111">You can create one of these templates by selecting **Record info** on the **Options** tab of the Action Pane.</span></span> <span data-ttu-id="ff960-112">Vrijgegeven producten zijn echter veel complexer dan de meeste andere typen records.</span><span class="sxs-lookup"><span data-stu-id="ff960-112">However, released products are much more complex than most other types of records.</span></span> <span data-ttu-id="ff960-113">Hoewel u **Recordinfo** op de pagina **Vrijgegeven producten** kunt selecteren om een sjabloon te maken en hoewel u die sjabloon kunt selecteren wanneer u een vrijgegeven product maakt, levert de sjabloon niet de verwachte veldwaarden voor het nieuwe vrijgegeven product.</span><span class="sxs-lookup"><span data-stu-id="ff960-113">Although you can select **Record info** on the **Released products** page to create a template, and although you can select that template when you create a released product, the template won't provide the expected field values for the new released product.</span></span> <span data-ttu-id="ff960-114">U kunt daarom geen recordinfo-sjablonen gebruiken voor vrijgegeven producten.</span><span class="sxs-lookup"><span data-stu-id="ff960-114">Therefore, you can't use "record info" templates for released products.</span></span> <span data-ttu-id="ff960-115">In plaats daarvan moet u specifieke productsjablonen maken.</span><span class="sxs-lookup"><span data-stu-id="ff960-115">Instead, you must create dedicated product templates.</span></span>

## <a name="resolution"></a><span data-ttu-id="ff960-116">Oplossing</span><span class="sxs-lookup"><span data-stu-id="ff960-116">Resolution</span></span>

<span data-ttu-id="ff960-117">Als u een productsjabloon wilt maken, gebruikt u het menu **Sjabloon** op het tabblad **Product** van het actievenster en niet de knop **Recordinfo** op het tabblad **Opties**.</span><span class="sxs-lookup"><span data-stu-id="ff960-117">To create a product template, use the **Template** menu on the **Product** tab of the Action Pane, not the **Record info** button on the **Options** tab.</span></span>

1. <span data-ttu-id="ff960-118">Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.</span><span class="sxs-lookup"><span data-stu-id="ff960-118">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="ff960-119">Selecteer **Sjabloon** in het actievenster op het tabblad **Product** in de groep **Nieuw** en selecteer **Persoonlijke sjabloon maken** of een **Gedeelde sjabloon maken**.</span><span class="sxs-lookup"><span data-stu-id="ff960-119">On the Action Pane, on the **Product** tab, in the **New** group, select **Template**, and then select either **Create personal template** or **Create shared template**, as appropriate.</span></span>
