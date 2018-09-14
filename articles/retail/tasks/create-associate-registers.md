--- 
title: " Registers maken en koppelen"
description: In deze procedure wordt weergegeven hoe u een kassa op het verkooppunt (POS) kunt maken.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 07e4b9f32a3a74b273272bd0b759d35c2a963e2e
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="ccac2-103"> Registers maken en koppelen</span><span class="sxs-lookup"><span data-stu-id="ccac2-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ccac2-104">In deze procedure wordt weergegeven hoe u een kassa op het verkooppunt (POS) kunt maken.</span><span class="sxs-lookup"><span data-stu-id="ccac2-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="ccac2-105">Bij deze procedure wordt het demobedrijf USRT gebruikt.</span><span class="sxs-lookup"><span data-stu-id="ccac2-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="ccac2-106">Ga naar Detailhandel en commerce > Kanaalinstellingen > POS-instellingen > Kassa´s.</span><span class="sxs-lookup"><span data-stu-id="ccac2-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="ccac2-107">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="ccac2-107">Click New.</span></span>
3. <span data-ttu-id="ccac2-108">Typ in het veld Kassanummer een id voor de nieuwe kassa.</span><span class="sxs-lookup"><span data-stu-id="ccac2-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="ccac2-109">De kassa-id bevat gewoonlijk codes die helpen de kassa aan de winkel te koppelen waarvan deze deel uitmaakt en aan de locatie binnen de winkel.</span><span class="sxs-lookup"><span data-stu-id="ccac2-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="ccac2-110">Typ in het veld Naam een beschrijvende naam voor de kassa.</span><span class="sxs-lookup"><span data-stu-id="ccac2-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="ccac2-111">Typ of selecteer een waarde in het veld Winkelnummer.</span><span class="sxs-lookup"><span data-stu-id="ccac2-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="ccac2-112">Typ of selecteer een waarde in het veld Hardwareprofiel.</span><span class="sxs-lookup"><span data-stu-id="ccac2-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="ccac2-113">Hardwareprofielen worden gebruikt om de randapparaten voor de detailhandel op te geven die aan de kassa worden gekoppeld, zoals kassalade en kassabonprinter.</span><span class="sxs-lookup"><span data-stu-id="ccac2-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="ccac2-114">Typ of selecteer een waarde in het veld Visueel profiel.</span><span class="sxs-lookup"><span data-stu-id="ccac2-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="ccac2-115">Visuele profielen worden gebruikt om de afbeeldingen op te geven die op de POS-achtergrond en aanmeldingspagina worden gebruikt alsmede thema's voor het POS-systeem.</span><span class="sxs-lookup"><span data-stu-id="ccac2-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="ccac2-116">Typ een waarde in het veld EFT POS-kassanummer.</span><span class="sxs-lookup"><span data-stu-id="ccac2-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="ccac2-117">Het EFT POS-kassanummer wordt gebruikt om aan de betalingsverwerker te melden welke betalingsterminal autorisatieaanvragen verzendt.</span><span class="sxs-lookup"><span data-stu-id="ccac2-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="ccac2-118">Deze waarde wordt vaak de "terminal-id" of "TID" genoemd.</span><span class="sxs-lookup"><span data-stu-id="ccac2-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="ccac2-119">De TID is meestal te vinden op een sticker op het betalingsapparaat.</span><span class="sxs-lookup"><span data-stu-id="ccac2-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="ccac2-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="ccac2-120">Click Save.</span></span>


