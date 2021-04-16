---
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: peakerbl
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e25fee324ce95cd04b86ee0e4e6a56cfacb61a53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745736"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="d78b6-103">Scheiding van taken instellen</span><span class="sxs-lookup"><span data-stu-id="d78b6-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d78b6-104">U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="d78b6-105">Dit concept wordt scheiding van taken genoemd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="d78b6-106">Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt.</span><span class="sxs-lookup"><span data-stu-id="d78b6-106">For example, you might not want the same person to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="d78b6-107">Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren.</span><span class="sxs-lookup"><span data-stu-id="d78b6-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="d78b6-108">U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="d78b6-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="d78b6-109">Voer de volgende procedure uit om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="d78b6-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="d78b6-110">U moet een systeembeheerder zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d78b6-110">You must be a system administrator to complete the procedure.</span></span>

1. <span data-ttu-id="d78b6-111">Ga naar **Systeembeheer** > **Beveiliging** > **Scheiding van taken** > **Regels voor scheiding van taken**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-111">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
2. <span data-ttu-id="d78b6-112">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-112">Click **New**.</span></span>
3. <span data-ttu-id="d78b6-113">Typ een waarde voor de regel in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-113">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="d78b6-114">Klik in het veld **Eerste functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d78b6-114">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d78b6-115">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d78b6-115">In the list, find and select the desired record.</span></span> <span data-ttu-id="d78b6-116">Selecteer de eerste functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-116">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="d78b6-117">Klik in het veld **Tweede functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d78b6-117">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="d78b6-118">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d78b6-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="d78b6-119">Selecteer de tweede functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-119">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="d78b6-120">Selecteer een optie in het veld **Ernst**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-120">In the **Severity** field, select an option.</span></span> <span data-ttu-id="d78b6-121">Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d78b6-121">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="d78b6-122">Typ een waarde in het veld **Beveiligingsrisico**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-122">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="d78b6-123">Voer een omschrijving van het beveiligingsrisico in.</span><span class="sxs-lookup"><span data-stu-id="d78b6-123">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="d78b6-124">Typ een waarde in het veld **Risicobeperking beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-124">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="d78b6-125">Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken.</span><span class="sxs-lookup"><span data-stu-id="d78b6-125">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="d78b6-126">Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.</span><span class="sxs-lookup"><span data-stu-id="d78b6-126">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="d78b6-127">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d78b6-127">Click **Save**.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d78b6-128">Wanneer u een regel maakt, wordt niet gecontroleerd of de regels voor de scheiding van taken worden nageleefd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-128">Compliance with the rules for segregation of duties is not verified when you create a rule.</span></span> <span data-ttu-id="d78b6-129">U kunt een regel maken die een conflict veroorzaakt voor bestaande rollen.</span><span class="sxs-lookup"><span data-stu-id="d78b6-129">You can create a rule that creates a conflict for existing roles.</span></span> <span data-ttu-id="d78b6-130">Bestaande gebruikersroltoewijzingen kunnen ook in conflict zijn met de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="d78b6-130">Existing user role assignments can also be in conflict with the new rule.</span></span> <span data-ttu-id="d78b6-131">U moet de conformiteit valideren nadat u een regel hebt gemaakt of gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="d78b6-131">You must validate compliance after you create or modify a rule.</span></span> <span data-ttu-id="d78b6-132">Zie [Conflicten bij scheiding van taken identificeren en oplossen](identify-resolve-conflicts-segregation-duties.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d78b6-132">For more information, see [Identify and resolve conflicts in segregation of duties](identify-resolve-conflicts-segregation-duties.md)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]