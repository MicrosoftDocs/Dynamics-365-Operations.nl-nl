---
title: Aanschaf van vaste activa voorstellen
description: In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.
author: saraschi2
ms.date: 03/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d529cd53b41827a78b282afd4d2c69d2f2db555e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817156"
---
# <a name="propose-fixed-asset-acquisitions"></a><span data-ttu-id="21eda-103">Aanschaf van vaste activa voorstellen</span><span class="sxs-lookup"><span data-stu-id="21eda-103">Propose fixed asset acquisitions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21eda-104">In dit onderwerp wordt beschreven hoe u een vast activum bijboekt met het verwervingsvoorstel in het vaste-activajournaal.</span><span class="sxs-lookup"><span data-stu-id="21eda-104">This topic describes how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="21eda-105">Het gebruikt de rol Accountant en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="21eda-105">It uses the accountant role and demo data for the USMF legal entity.</span></span> <span data-ttu-id="21eda-106">Als u een vast activum via een voorsteljournaal voor vaste activa wilt verkrijgen, moet u eerst de record voor de vaste activa maken en vervolgens de aanschafprijs definiëren in het activaboek.</span><span class="sxs-lookup"><span data-stu-id="21eda-106">To acquire a fixed asset through a fixed asset proposal journal, you must first create the fixed asset record, and then define the acquisition price in the asset book.</span></span>

## <a name="create-an-asset-acquisition-proposal"></a><span data-ttu-id="21eda-107">Een voorstel voor het verwerven van activa maken</span><span class="sxs-lookup"><span data-stu-id="21eda-107">Create an asset acquisition proposal</span></span>

<span data-ttu-id="21eda-108">Voer de volgende stappen uit om een voorstel voor het verwerven van activa te maken.</span><span class="sxs-lookup"><span data-stu-id="21eda-108">Complete the following steps to create an asset acquisition proposal.</span></span> 

1. <span data-ttu-id="21eda-109">Ga in het navigatievenster naar **Modules > Vaste activa > Journaalboekingen > Vaste-activajournaal**.</span><span class="sxs-lookup"><span data-stu-id="21eda-109">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="21eda-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="21eda-110">Select **New**.</span></span>
3. <span data-ttu-id="21eda-111">Typ of selecteer een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="21eda-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="21eda-112">Selecteer **Regels** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="21eda-112">In the Action Pane, select **Lines**.</span></span>
5. <span data-ttu-id="21eda-113">Selecteer **Voorstellen**.</span><span class="sxs-lookup"><span data-stu-id="21eda-113">Select **Proposals**.</span></span>
6. <span data-ttu-id="21eda-114">Selecteer **Verwervingsvoorstel**.</span><span class="sxs-lookup"><span data-stu-id="21eda-114">Select **Acquisition proposal**.</span></span>
7. <span data-ttu-id="21eda-115">Selecteer **Filter**.</span><span class="sxs-lookup"><span data-stu-id="21eda-115">Select **Filter**.</span></span> <span data-ttu-id="21eda-116">Selecteer **Opnieuw instellen** om eerdere waarden te wissen.</span><span class="sxs-lookup"><span data-stu-id="21eda-116">Select **Reset** to clear previous values.</span></span>
8. <span data-ttu-id="21eda-117">Selecteer de rij **Vaste-activanummer**.</span><span class="sxs-lookup"><span data-stu-id="21eda-117">Select the **Fixed asset number** row.</span></span>
9. <span data-ttu-id="21eda-118">Typ of selecteer een waarde in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="21eda-118">In the **Criteria** field, enter or select a value.</span></span> <span data-ttu-id="21eda-119">Stel de resterende criteria in voor de vaste activa die u met dit voorstel wilt bijboeken.</span><span class="sxs-lookup"><span data-stu-id="21eda-119">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
10. <span data-ttu-id="21eda-120">Selecteer tweemaal **OK** om het deelvenster af te sluiten.</span><span class="sxs-lookup"><span data-stu-id="21eda-120">Select **OK** twice to exit out of the pane.</span></span>
- <span data-ttu-id="21eda-121">Controleer of de transactieregels worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="21eda-121">Verify that the transaction lines are created.</span></span>  
- <span data-ttu-id="21eda-122">Alleen vaste activa waarvoor de verwervingsdatum en -prijs zijn ingesteld in het boek worden in het verwervingsvoorstel opgenomen.</span><span class="sxs-lookup"><span data-stu-id="21eda-122">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
11. <span data-ttu-id="21eda-123">Selecteer op de pagina het tabblad **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="21eda-123">On the page, select the **Books** tab.</span></span>
12. <span data-ttu-id="21eda-124">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="21eda-124">Select **Post**.</span></span>

## <a name="include-default-financial-dimensions-in-an-acquisition-proposal"></a><span data-ttu-id="21eda-125">Financiële standaarddimensies opnemen in een overnamevoorstel</span><span class="sxs-lookup"><span data-stu-id="21eda-125">Include default financial dimensions in an acquisition proposal</span></span>

<span data-ttu-id="21eda-126">De verwervingstransactie kan worden gemaakt met Excel-invoegtoepassingen door naar **Vaste activa > Journaalposten > Vaste-activajournaal** te gaan.</span><span class="sxs-lookup"><span data-stu-id="21eda-126">The acquisition transaction can be created using Excel add-ins, by going to **Fixed assets > Journal entries > Fixed asset journal**.</span></span> <span data-ttu-id="21eda-127">Maak een nieuw journaal en ga naar de sectie **Regels** op de pagina en selecteer het Excel-pictogram en vervolgens een journaalregel voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="21eda-127">Create a new journal and move to the **Lines** section on the page and select the Excel icon, and then select a Fixed asset journal line.</span></span> <span data-ttu-id="21eda-128">Er wordt een Excel-sjabloon voor journaalregels gemaakt en geopend.</span><span class="sxs-lookup"><span data-stu-id="21eda-128">The system will create and open an Excel template representing journal lines.</span></span> <span data-ttu-id="21eda-129">U kunt gegevens toevoegen voor de journaalregels die u aan de sjabloon toevoegt en deze gegevens vervolgens weer in het systeem publiceren.</span><span class="sxs-lookup"><span data-stu-id="21eda-129">You can add data for the journal lines you're adding into the template, and then publish that information back into the system.</span></span> 

<span data-ttu-id="21eda-130">Als er standaarddimensies zijn ingesteld voor het geselecteerde activaboek en de bijbehorende vaste activa die zijn ingevoerd in de Excel-sjabloon, worden de financiële standaarddimensies aangeroepen vanuit de hoofdgegevens van het activaboek wanneer het journaal vanuit Excel naar het systeem wordt gepubliceerd.</span><span class="sxs-lookup"><span data-stu-id="21eda-130">If default dimensions have been set up for the selected asset book and the corresponding fixed assets that were entered in the Excel template, the default financial dimensions will be called from the asset book master data when the journal is published from the Excel to the system.</span></span> <span data-ttu-id="21eda-131">Als u automatisch financiële dimensies in een activaboek wilt opnemen tijdens het publiceren van het vaste-activajournaal vanuit de Excel-invoegtoepassing, moeten de standaarddimensies van tevoren zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="21eda-131">To include financial dimensions on an asset book automatically while publishing the fixed asset journal from the Excel add-in, the default dimensions must be set up in advance.</span></span>  


[!INCLUDE [footer-include](../../../includes/footer-banner.md)]
