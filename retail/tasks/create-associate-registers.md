--- 
title: " Registers maken en koppelen"
description: In deze procedure wordt weergegeven hoe u een kassa op het verkooppunt (POS) kunt maken.
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="08fca-103"> Registers maken en koppelen</span><span class="sxs-lookup"><span data-stu-id="08fca-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="08fca-104">In deze procedure wordt weergegeven hoe u een kassa op het verkooppunt (POS) kunt maken.</span><span class="sxs-lookup"><span data-stu-id="08fca-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="08fca-105">Bij deze procedure wordt het demobedrijf USRT gebruikt.</span><span class="sxs-lookup"><span data-stu-id="08fca-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="08fca-106">Ga naar Detailhandel en commerce > Kanaalinstellingen > POS-instellingen > Kassa´s.</span><span class="sxs-lookup"><span data-stu-id="08fca-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="08fca-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="08fca-107">Click New.</span></span>
3. <span data-ttu-id="08fca-108">Typ in het veld Kassanummer een id voor de nieuwe kassa.</span><span class="sxs-lookup"><span data-stu-id="08fca-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="08fca-109">De kassa-id bevat gewoonlijk codes die helpen de kassa aan de winkel te koppelen waarvan deze deel uitmaakt en aan de locatie binnen de winkel.</span><span class="sxs-lookup"><span data-stu-id="08fca-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="08fca-110">Typ in het veld Naam een beschrijvende naam voor de kassa.</span><span class="sxs-lookup"><span data-stu-id="08fca-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="08fca-111">Typ of selecteer een waarde in het veld Winkelnummer.</span><span class="sxs-lookup"><span data-stu-id="08fca-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="08fca-112">Typ of selecteer een waarde in het veld Hardwareprofiel.</span><span class="sxs-lookup"><span data-stu-id="08fca-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="08fca-113">Hardwareprofielen worden gebruikt om de randapparaten voor de detailhandel op te geven die aan de kassa worden gekoppeld, zoals kassalade en kassabonprinter.</span><span class="sxs-lookup"><span data-stu-id="08fca-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="08fca-114">Typ of selecteer een waarde in het veld Visueel profiel.</span><span class="sxs-lookup"><span data-stu-id="08fca-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="08fca-115">Visuele profielen worden gebruikt om de afbeeldingen op te geven die op de POS-achtergrond en aanmeldingspagina worden gebruikt alsmede thema's voor het POS-systeem.</span><span class="sxs-lookup"><span data-stu-id="08fca-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="08fca-116">Typ een waarde in het veld EFT POS-kassanummer.</span><span class="sxs-lookup"><span data-stu-id="08fca-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="08fca-117">Het EFT POS-kassanummer wordt gebruikt om aan de betalingsverwerker te melden welke betalingsterminal autorisatieaanvragen verzendt.</span><span class="sxs-lookup"><span data-stu-id="08fca-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="08fca-118">Deze waarde wordt vaak de "terminal-id" of "TID" genoemd.</span><span class="sxs-lookup"><span data-stu-id="08fca-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="08fca-119">De TID is meestal te vinden op een sticker op het betalingsapparaat.</span><span class="sxs-lookup"><span data-stu-id="08fca-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="08fca-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="08fca-120">Click Save.</span></span>


