--- 
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 754f28cd2831d8a9a57c408518d240de460b732b
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="17263-103">Scheiding van taken instellen</span><span class="sxs-lookup"><span data-stu-id="17263-103">Set up segregation of duties</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="17263-104">U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="17263-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="17263-105">Dit concept wordt scheiding van taken genoemd.</span><span class="sxs-lookup"><span data-stu-id="17263-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="17263-106">Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt.</span><span class="sxs-lookup"><span data-stu-id="17263-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="17263-107">Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren.</span><span class="sxs-lookup"><span data-stu-id="17263-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="17263-108">U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="17263-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="17263-109">Voer de volgende procedure uit om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="17263-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="17263-110">U moet een systeembeheerder zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="17263-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="17263-111">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT.</span><span class="sxs-lookup"><span data-stu-id="17263-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="17263-112">Ga naar Systeembeheer > Beveiliging > Scheiding van taken > Regels voor scheiding van taken.</span><span class="sxs-lookup"><span data-stu-id="17263-112">Go to System administration > Security > Segregation of duties > Segregation of duties rules.</span></span>
2. <span data-ttu-id="17263-113">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="17263-113">Click New.</span></span>
3. <span data-ttu-id="17263-114">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="17263-114">In the Name field, type a value.</span></span>
    * <span data-ttu-id="17263-115">Voer een naam voor de regel in.</span><span class="sxs-lookup"><span data-stu-id="17263-115">Enter a name for the rule.</span></span>  
4. <span data-ttu-id="17263-116">Klik in het veld Eerste functie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="17263-116">In the First duty field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17263-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="17263-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17263-118">Selecteer de eerste functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="17263-118">Select the first duty that is controlled by the rule.</span></span>  
6. <span data-ttu-id="17263-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="17263-119">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="17263-120">Klik in het veld Tweede functie op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="17263-120">In the Second duty field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="17263-121">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="17263-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="17263-122">Selecteer de tweede functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="17263-122">Select the second duty that is controlled by the rule.</span></span>  
9. <span data-ttu-id="17263-123">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="17263-123">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="17263-124">Selecteer een optie in het veld Ernst.</span><span class="sxs-lookup"><span data-stu-id="17263-124">In the Severity field, select an option.</span></span>
    * <span data-ttu-id="17263-125">Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.</span><span class="sxs-lookup"><span data-stu-id="17263-125">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="17263-126">Typ een waarde in het veld Beveiligingsrisico.</span><span class="sxs-lookup"><span data-stu-id="17263-126">In the Security risk field, type a value.</span></span>
    * <span data-ttu-id="17263-127">Voer een omschrijving van het beveiligingsrisico in.</span><span class="sxs-lookup"><span data-stu-id="17263-127">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="17263-128">Typ een waarde in het veld Risicobeperking beveiliging.</span><span class="sxs-lookup"><span data-stu-id="17263-128">In the Security mitigation field, type a value.</span></span>
    * <span data-ttu-id="17263-129">Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken.</span><span class="sxs-lookup"><span data-stu-id="17263-129">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="17263-130">Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.</span><span class="sxs-lookup"><span data-stu-id="17263-130">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>  
13. <span data-ttu-id="17263-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="17263-131">Click Save.</span></span>


