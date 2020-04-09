---
title: Het updateproces
description: Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt met wijzigingen in toepassingen en platforms.
author: andreabichsel
manager: AnnBe
ms.date: 02/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 424027e82717b8636d59289b28978d6ce3c6db4d
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154500"
---
# <a name="update-process"></a><span data-ttu-id="015fc-103">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="015fc-103">Update process</span></span>

<span data-ttu-id="015fc-104">Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt.</span><span class="sxs-lookup"><span data-stu-id="015fc-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="015fc-105">Deze updates bevatten zowel toepassings-als platformwijzigingen die vaak belangrijke verbeteringen voor de service bieden, waaronder wettelijke updates.</span><span class="sxs-lookup"><span data-stu-id="015fc-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="015fc-106">Updatebeleid</span><span class="sxs-lookup"><span data-stu-id="015fc-106">Update policy</span></span>

<span data-ttu-id="015fc-107">Er worden regelmatig updates uitgebracht voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="015fc-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="015fc-108">Human Resources wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="015fc-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="015fc-109">Releasetempo</span><span class="sxs-lookup"><span data-stu-id="015fc-109">Release cadence</span></span>

<span data-ttu-id="015fc-110">Human Resources-updates worden automatisch op alle omgevingen toegepast.</span><span class="sxs-lookup"><span data-stu-id="015fc-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="015fc-111">Human Resources biedt twee typen releases:</span><span class="sxs-lookup"><span data-stu-id="015fc-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="015fc-112">**Service-updates**: tweewekelijkse updates die correcties en nieuwe functies bevatten.</span><span class="sxs-lookup"><span data-stu-id="015fc-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="015fc-113">Service-updates bevatten ook toepasselijke platformupdates wanneer ze worden uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="015fc-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="015fc-114">Zie [Tabel 3: platform-releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases) om na te gaan wanneer platform-updates gewoonlijk worden uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="015fc-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases).</span></span> <span data-ttu-id="015fc-115">Tweewekelijkse updates bieden een gefaseerde globale implementatie tussen regio's.</span><span class="sxs-lookup"><span data-stu-id="015fc-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="015fc-116">Zie [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md) voor meer informatie over tweewekelijkse updates.</span><span class="sxs-lookup"><span data-stu-id="015fc-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="015fc-117">Alle ondersteunde gegevenscentra worden tweewekelijks bijgewerkt, tenzij anders aangegeven.</span><span class="sxs-lookup"><span data-stu-id="015fc-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="015fc-118">In de volgende regio's worden tweewekelijkse updates uitgebracht: Verenigde Staten, Australië, Europa, Groot-Brittannië, Azië en Canada.</span><span class="sxs-lookup"><span data-stu-id="015fc-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="015fc-119">**Common Data Service-oplossingsupdates**: deze updates worden ongeveer om de zes weken uitgevoerd, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="015fc-119">**Common Data Service solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="015fc-120">Deze bevatten nieuwe entiteiten en wijzigingen in bestaande entiteiten in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="015fc-120">They include new entities and changes to existing entities in Common Data Service.</span></span> <span data-ttu-id="015fc-121">Deze updates worden in dezelfde regio's uitgebracht als de tweewekelijkse updates en het duurt ongeveer zes weken voordat ze door alle datacentra zijn gerepliceerd.</span><span class="sxs-lookup"><span data-stu-id="015fc-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="015fc-122">Oplossingsupdates kunnen al dan niet samenvallen met tweewekelijkse service-updates.</span><span class="sxs-lookup"><span data-stu-id="015fc-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="015fc-123">Oplossingsupdates zijn beschikbaar in alle datacentra zodra deze zijn uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="015fc-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="015fc-124">Als u niet wilt wachten totdat de updates automatisch worden gerepliceerd, kunt u deze updates handmatig toepassen op elke willekeurige omgeving in elk datacentrum.</span><span class="sxs-lookup"><span data-stu-id="015fc-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="015fc-125">Indien nodig biedt Human Resources ook de volgende typen oplossingen:</span><span class="sxs-lookup"><span data-stu-id="015fc-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="015fc-126">**Revisie (hotfix)**: foutcorrecties die kunnen optreden samen met, of los van, een tweewekelijkse service-updaterelease</span><span class="sxs-lookup"><span data-stu-id="015fc-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="015fc-127">**Noodoplossing**: proactieve en reactieve hotfixes die zelfstandig zijn, kunnen alleen configuratiewijzigingen of ook codewijzigingen bevatten om problemen met live-sites op te lossen en kunnen los van een tweewekelijkse service-updaterelease optreden</span><span class="sxs-lookup"><span data-stu-id="015fc-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="015fc-128">Releases worden beoordeeld, getest en gevalideerd in een interne omgeving.</span><span class="sxs-lookup"><span data-stu-id="015fc-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="015fc-129">Nadat de builds zijn afgemeld, worden ze geïmplementeerd voor productie.</span><span class="sxs-lookup"><span data-stu-id="015fc-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2020"></a><span data-ttu-id="015fc-130">Uitzonderingen in releasetempo in 2020</span><span class="sxs-lookup"><span data-stu-id="015fc-130">Release cadence exceptions in 2020</span></span>

<span data-ttu-id="015fc-131">De volgende datums zijn uitzonderingen op de normale releaseplanning:</span><span class="sxs-lookup"><span data-stu-id="015fc-131">The following dates are exceptions to the regular release schedule:</span></span>

| <span data-ttu-id="015fc-132">Datum</span><span class="sxs-lookup"><span data-stu-id="015fc-132">Date</span></span> | <span data-ttu-id="015fc-133">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="015fc-133">Description</span></span> |
| --- | --- |
| <span data-ttu-id="015fc-134">Week van 23 november</span><span class="sxs-lookup"><span data-stu-id="015fc-134">Week of November 23</span></span> | <span data-ttu-id="015fc-135">Geen updates</span><span class="sxs-lookup"><span data-stu-id="015fc-135">No updates</span></span> |
| <span data-ttu-id="015fc-136">Week van 14 december</span><span class="sxs-lookup"><span data-stu-id="015fc-136">Week of December 14</span></span> | <span data-ttu-id="015fc-137">Alleen kleine updates</span><span class="sxs-lookup"><span data-stu-id="015fc-137">Minor updates only</span></span> |
| <span data-ttu-id="015fc-138">Week van 21 december</span><span class="sxs-lookup"><span data-stu-id="015fc-138">Week of December 21</span></span> | <span data-ttu-id="015fc-139">Geen updates</span><span class="sxs-lookup"><span data-stu-id="015fc-139">No updates</span></span> |
| <span data-ttu-id="015fc-140">Week van 28 december</span><span class="sxs-lookup"><span data-stu-id="015fc-140">Week of December 28</span></span> | <span data-ttu-id="015fc-141">Geen updates</span><span class="sxs-lookup"><span data-stu-id="015fc-141">No updates</span></span> |

## <a name="communications"></a><span data-ttu-id="015fc-142">Berichtgeving</span><span class="sxs-lookup"><span data-stu-id="015fc-142">Communications</span></span>

<span data-ttu-id="015fc-143">Op de volgende locaties kunt u nagaan wat er is gepland voor Human Resources en wat we hebben uitgebracht:</span><span class="sxs-lookup"><span data-stu-id="015fc-143">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="015fc-144">Dynamics 365 Human Resources-roadmap</span><span class="sxs-lookup"><span data-stu-id="015fc-144">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="015fc-145">Dynamics 365-releaseplannen</span><span class="sxs-lookup"><span data-stu-id="015fc-145">Dynamics 365 Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans/)

- [<span data-ttu-id="015fc-146">Nieuwe of gewijzigde functies in Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="015fc-146">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="015fc-147">[Problemen zoeken in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (alleen voor fouten die betrekking hebben op platforms)</span><span class="sxs-lookup"><span data-stu-id="015fc-147">[Issue search in Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="015fc-148">Human resources-blog</span><span class="sxs-lookup"><span data-stu-id="015fc-148">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="015fc-149">Human Resources Yammer-community</span><span class="sxs-lookup"><span data-stu-id="015fc-149">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="015fc-150">Preview-functies in een sandbox-omgeving</span><span class="sxs-lookup"><span data-stu-id="015fc-150">Preview features in a sandbox environment</span></span>

<span data-ttu-id="015fc-151">U kunt preview-functies in een sandbox-omgeving valideren voordat u deze in uw productie-omgeving inschakelt.</span><span class="sxs-lookup"><span data-stu-id="015fc-151">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="015fc-152">Zie [Overzicht van functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) voor meer informatie over het inschakelen van nieuwe functies.</span><span class="sxs-lookup"><span data-stu-id="015fc-152">For more information about enabling features, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>

<span data-ttu-id="015fc-153">Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus.</span><span class="sxs-lookup"><span data-stu-id="015fc-153">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="015fc-154">De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode.</span><span class="sxs-lookup"><span data-stu-id="015fc-154">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="015fc-155">Zodra u nieuwe functies in het werkgebied Functiebeheer ziet, kunt u deze inschakelen.</span><span class="sxs-lookup"><span data-stu-id="015fc-155">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="015fc-156">Sommige functies zijn mogelijk standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="015fc-156">Some features may be on by default.</span></span>

<span data-ttu-id="015fc-157">Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied Functiebeheer).</span><span class="sxs-lookup"><span data-stu-id="015fc-157">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="015fc-158">Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="015fc-158">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="015fc-159">Het werkgebied Functiebeheer geeft aan wanneer een previewfunctie verplicht wordt.</span><span class="sxs-lookup"><span data-stu-id="015fc-159">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="015fc-160">Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen.</span><span class="sxs-lookup"><span data-stu-id="015fc-160">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="015fc-161">U kunt verplichte functies niet uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="015fc-161">You can't turn off mandatory features.</span></span> <span data-ttu-id="015fc-162">Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="015fc-162">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="015fc-163">Het is raadzaam om de functies vooraf in een sandbox- of testomgeving te bekijken.</span><span class="sxs-lookup"><span data-stu-id="015fc-163">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="015fc-164">U kunt het beste een kopie van uw huidige productie-omgeving of database maken in een sandbox-omgeving, zodat u beschikt over de volledige ervaring van de nieuwe functies met uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="015fc-164">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="015fc-165">Zie [Een Human Resources-project inrichten](hr-admin-setup-provision.md) voor meer informatie over het inrichten van een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="015fc-165">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="015fc-166">Zie [Een exemplaar verwijderen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) als u een testomgeving wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="015fc-166">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="015fc-167">Fouten rapporteren</span><span class="sxs-lookup"><span data-stu-id="015fc-167">Report bugs</span></span>

<span data-ttu-id="015fc-168">Tijdens het testen van preview-functies of het uitproberen van nieuwe mogelijkheden, is het mogelijk dat u items vindt die niet werken zoals u verwacht.</span><span class="sxs-lookup"><span data-stu-id="015fc-168">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="015fc-169">Meld eventuele fouten via [Microsoft Dynamics 365-ondersteuning](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="015fc-169">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="015fc-170">Zie ook</span><span class="sxs-lookup"><span data-stu-id="015fc-170">See also</span></span>

[<span data-ttu-id="015fc-171">Releaseplannen voor Dynamics 365 en Power Platform</span><span class="sxs-lookup"><span data-stu-id="015fc-171">Dynamics 365 and Power Platform Release Plans</span></span>](https://docs.microsoft.com/dynamics365/release-plans)</br>
[<span data-ttu-id="015fc-172">Nieuwe of gewijzigde functies in Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="015fc-172">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="015fc-173">Lifecycle-beleid voor software</span><span class="sxs-lookup"><span data-stu-id="015fc-173">Software lifecycle policy</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

