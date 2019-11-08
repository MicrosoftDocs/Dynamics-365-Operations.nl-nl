---
title: Bestandsindelingen voor betalingsmethoden
description: In dit onderwerp worden de twee methoden beschreven voor het verkrijgen van bestandsindelingen die u voor betalingsmethoden kunt gebruiken.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 262514
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 36f12fbc21fe782555c348f8a401e7aef6219f41
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183819"
---
# <a name="file-formats-for-methods-of-payment"></a><span data-ttu-id="72286-103">Bestandsindelingen voor betalingsmethoden</span><span class="sxs-lookup"><span data-stu-id="72286-103">File formats for methods of payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72286-104">In dit onderwerp worden de twee methoden beschreven voor het verkrijgen van bestandsindelingen die u voor betalingsmethoden kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="72286-104">This topic describes the two methods for getting file formats that you can use for methods of payment.</span></span>

<span data-ttu-id="72286-105">Er zijn twee methoden waarmee u bestandsindelingen kunt verkrijgen voor gebruik bij betalingsmethoden, ER-bestandsindelingen (elektronische rapportage) of X ++-bestandsindelingen.</span><span class="sxs-lookup"><span data-stu-id="72286-105">There are two methods that you can use to get file formats for use with methods of payment, electronic reporting (ER) file formats or X++ file formats.</span></span> <span data-ttu-id="72286-106">Wanneer u een betalingsmethode voor een klant of leverancier instelt, geeft u aan welke bestandsindelingen en standaarden moeten worden gebruikt voor betalingen en hoe betalingen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="72286-106">When you set up a method of payment for a customer or vendor, you indicate which file formats and standards should be used for payments and how payments will be processed.</span></span> <span data-ttu-id="72286-107">U kunt de volgende typen indelingen selecteren:</span><span class="sxs-lookup"><span data-stu-id="72286-107">You can select from the following types of formats:</span></span>

-   <span data-ttu-id="72286-108">Exporteren</span><span class="sxs-lookup"><span data-stu-id="72286-108">Export</span></span>
-   <span data-ttu-id="72286-109">Importeren</span><span class="sxs-lookup"><span data-stu-id="72286-109">Import</span></span>
-   <span data-ttu-id="72286-110">Retour</span><span class="sxs-lookup"><span data-stu-id="72286-110">Return</span></span>
-   <span data-ttu-id="72286-111">Remise</span><span class="sxs-lookup"><span data-stu-id="72286-111">Remittance</span></span>

### <a name="method-1-electronic-reporting-file-formats"></a><span data-ttu-id="72286-112">Methode 1: bestandsindelingen elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="72286-112">Method 1: Electronic reporting file formats</span></span>

<span data-ttu-id="72286-113">Voor bestandsindelingen die zijn gebaseerd op ER-configuraties, moet u de configuraties van Lifecycle Services (LCS) importeren.</span><span class="sxs-lookup"><span data-stu-id="72286-113">For file formats that are based on ER configurations, you must import the configurations from Lifecycle Services (LCS).</span></span> <span data-ttu-id="72286-114">Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="72286-114">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="72286-115">Nadat u configuraties voor rapportage hebt geïmporteerd voor deze bestandsindelingen, zijn de geïmporteerde indelingen beschikbaar om te selecteren op de pagina **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="72286-115">After you import reporting configurations for those file formats, the imported formats will be available to select on the **Methods of payment** page.</span></span> <span data-ttu-id="72286-116">Het proces voor het importeren en selecteren van bestandsindelingen voor Europa is vergelijkbaar met de procedure voor Japan.</span><span class="sxs-lookup"><span data-stu-id="72286-116">The process for importing and selecting file formats for Europe is similar to the procedure for Japan.</span></span> <span data-ttu-id="72286-117">Zie [JBA-betalingsbestandsindeling inschakelen](tasks/jba-payment-file-format.md) voor meer informatie</span><span class="sxs-lookup"><span data-stu-id="72286-117">For more details, see [Enable the JBA payment file format](tasks/jba-payment-file-format.md)</span></span>

### <a name="method-2-x-file-formats"></a><span data-ttu-id="72286-118">Methode 2: X++-bestandsindelingen</span><span class="sxs-lookup"><span data-stu-id="72286-118">Method 2: X++ file formats</span></span>

<span data-ttu-id="72286-119">Als u de bestandsindelingen die zijn gebaseerd op X++-code wilt selecteren, moet u de volgende stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="72286-119">To select file formats that are based on X++ code, complete the following steps.</span></span>

1.  <span data-ttu-id="72286-120">Ga naar de pagina **Betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="72286-120">Go to the **Methods of payment** page.</span></span>
2.  <span data-ttu-id="72286-121">Klik op het sneltabblad **Bestandsindelingen** op **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="72286-121">On the **File formats** FastTab, click **Setup**.</span></span>
3.  <span data-ttu-id="72286-122">Selecteer het tabblad dat overeenkomt met het type bestandsindeling.</span><span class="sxs-lookup"><span data-stu-id="72286-122">Select the tab that corresponds with the file format type.</span></span>
4.  <span data-ttu-id="72286-123">Selecteer een bestandsindeling in de lijst **Beschikbaar** en verplaats deze naar de lijst **Geselecteerd** met het pijlbesturingselement.</span><span class="sxs-lookup"><span data-stu-id="72286-123">Select a file format from the **Available** list and move it to the **Selected** list with the arrow control.</span></span>
5.  <span data-ttu-id="72286-124">Sluit de pagina **Bestandsindelingen voor betalingsmethoden**.</span><span class="sxs-lookup"><span data-stu-id="72286-124">Close the **File formats for methods of payment** page.</span></span>
6.  <span data-ttu-id="72286-125">Selecteer op het sneltabblad **Bestandsindelingen** de bestandsindeling voor de betalingsmethode in het juiste veld met bestandsindelingen.</span><span class="sxs-lookup"><span data-stu-id="72286-125">On the **File formats** FastTab, select the file format to use for the method of payment from the appropriate file format field.</span></span> <span data-ttu-id="72286-126">De algemene opties voor elektronische aangifte moeten worden ingesteld op **Nee** voor X ++-bestandsindelingen.</span><span class="sxs-lookup"><span data-stu-id="72286-126">The General electronic reporting options should be set to **No** for X++ file formats.</span></span>



