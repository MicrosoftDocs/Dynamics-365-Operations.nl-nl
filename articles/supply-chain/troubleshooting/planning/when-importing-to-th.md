---
title: U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht
description: U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: DataManagementWorkspace_
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: angarmas
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3dfa974740420433af1e1b37630b22509510c91b
ms.sourcegitcommit: 3c15a26e9708adc9a75082dc551f0a3a0a7d89f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049460"
---
# <a name="youre-prompted-to-save-item-coverage-settings-even-though-you-made-no-changes"></a><span data-ttu-id="5281e-103">U wordt gevraagd de instellingen voor artikelbehoefteplanning op te slaan, ook als u geen wijzigingen hebt aangebracht</span><span class="sxs-lookup"><span data-stu-id="5281e-103">You're prompted to save item coverage settings even though you made no changes</span></span>

<span data-ttu-id="5281e-104">KB-nummer: 4615588</span><span class="sxs-lookup"><span data-stu-id="5281e-104">KB number: 4615588</span></span>

## <a name="symptoms"></a><span data-ttu-id="5281e-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="5281e-105">Symptoms</span></span>

<span data-ttu-id="5281e-106">In sommige scenario's ontvangt u mogelijk het volgende bericht wanneer u de pagina **Artikelbehoefteplanning** opent nadat u artikelen hebt geïmporteerd via de entiteit *Artikelbehoefteplanning V2*:</span><span class="sxs-lookup"><span data-stu-id="5281e-106">In some scenarios, you might receive the following message when you open the **Item coverage** page after you import items through the *Item coverage V2* entity:</span></span>

> <span data-ttu-id="5281e-107">Wilt u uw wijzigingen opslaan alvorens te sluiten?</span><span class="sxs-lookup"><span data-stu-id="5281e-107">Do you want to save your changes before closing?</span></span>

<span data-ttu-id="5281e-108">U ontvangt dit bericht ook als u geen wijzigingen hebt aangebracht.</span><span class="sxs-lookup"><span data-stu-id="5281e-108">You receive this message even though you haven't made any changes.</span></span>

## <a name="resolution"></a><span data-ttu-id="5281e-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="5281e-109">Resolution</span></span>

<span data-ttu-id="5281e-110">De pagina **Artikelbehoefteplanning** bevat complexe standaardlogica die ertoe kan leiden dat het bericht wordt weergegeven nadat er recent directe wijzigingen in de database zijn aangebracht, bijvoorbeeld via het importeren van entiteiten.</span><span class="sxs-lookup"><span data-stu-id="5281e-110">The **Item coverage** page includes complex defaulting logic that might cause the message to be shown after direct changes have recently been made in the database, such as through entity import.</span></span> <span data-ttu-id="5281e-111">Het entiteitsveld `AREGENERALSETTINGSOVERRIDDEN` is bijvoorbeeld ingesteld op *Nee*, maar u importeert een bestand dat nieuwe of gewijzigde waarden bevat voor velden zoals `PRODUCTCOVERAGEGROUPID` en/of `VENDORACCOUNTNUMBER`.</span><span class="sxs-lookup"><span data-stu-id="5281e-111">For example, the `AREGENERALSETTINGSOVERRIDDEN` entity field is set to *No*, but you import a file that provides new or modified values for fields such as `PRODUCTCOVERAGEGROUPID` and/or `VENDORACCOUNTNUMBER`.</span></span> <span data-ttu-id="5281e-112">Omdat het veld `AREGENERALSETTINGSOVERRIDDEN` in dit geval is ingesteld op *Nee*, worden de waarden automatisch uit de velden gewist wanneer u de pagina **Artikelbehoefteplanning** voor de eerste keer na het importeren opent.</span><span class="sxs-lookup"><span data-stu-id="5281e-112">In this case, because the `AREGENERALSETTINGSOVERRIDDEN` field is set to *No*, the values are automatically cleared from the fields when you open the **Item coverage** page for the first time after the import.</span></span> <span data-ttu-id="5281e-113">Als u de wijzigingen opslaat wanneer daarom in het berichtvak wordt gevraagd, worden deze opgeslagen in de database.</span><span class="sxs-lookup"><span data-stu-id="5281e-113">If you save the changes as the message box prompts, they are stored in the database.</span></span> <span data-ttu-id="5281e-114">Anders ontvangt u hetzelfde bericht wanneer u de pagina de volgende keer opent.</span><span class="sxs-lookup"><span data-stu-id="5281e-114">Otherwise, you will receive the same message the next time that you open the page.</span></span>

<span data-ttu-id="5281e-115">Om dit gedrag te voorkomen, maar ook waarden op te nemen voor velden, zoals `PRODUCTCOVERAGEGROUPID` via entiteitsimport, stelt u `AREGENERALSETTINGSOVERRIDDEN` in op *Ja* wanneer u importeert.</span><span class="sxs-lookup"><span data-stu-id="5281e-115">To prevent this behavior but also include values for fields such as `PRODUCTCOVERAGEGROUPID` through entity import, set `AREGENERALSETTINGSOVERRIDDEN` to *Yes* when you import.</span></span>
