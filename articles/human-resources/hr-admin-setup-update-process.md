---
title: Het updateproces
description: Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt met wijzigingen in toepassingen en platforms.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ca8868069fca4453efbb76694702a554da6d7aa6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892270"
---
# <a name="update-process"></a><span data-ttu-id="8debb-103">Het updateproces</span><span class="sxs-lookup"><span data-stu-id="8debb-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8debb-104">Microsoft Dynamics 365 Human Resources is echt software in de vorm van een service (SaaS) die voortdurende 'touchless' updates verzorgt.</span><span class="sxs-lookup"><span data-stu-id="8debb-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="8debb-105">Deze updates bevatten zowel toepassings-als platformwijzigingen die vaak belangrijke verbeteringen voor de service bieden, waaronder wettelijke updates.</span><span class="sxs-lookup"><span data-stu-id="8debb-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="8debb-106">Updatebeleid</span><span class="sxs-lookup"><span data-stu-id="8debb-106">Update policy</span></span>

<span data-ttu-id="8debb-107">Er worden regelmatig updates uitgebracht voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="8debb-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="8debb-108">Human Resources wordt ondersteund volgens het [Microsoft Support Lifecycle-beleid](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), dat consistente en voorspelbare richtlijnen bevat voor de beschikbaarheid van ondersteuning.</span><span class="sxs-lookup"><span data-stu-id="8debb-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="8debb-109">Releasetempo</span><span class="sxs-lookup"><span data-stu-id="8debb-109">Release cadence</span></span> 

<span data-ttu-id="8debb-110">Human Resources-updates worden automatisch op alle omgevingen toegepast.</span><span class="sxs-lookup"><span data-stu-id="8debb-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="8debb-111">Human Resources biedt twee typen releases:</span><span class="sxs-lookup"><span data-stu-id="8debb-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="8debb-112">**Service-updates**: tweewekelijkse updates die correcties en nieuwe functies bevatten.</span><span class="sxs-lookup"><span data-stu-id="8debb-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="8debb-113">Service-updates bevatten ook toepasselijke platformupdates wanneer ze worden uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="8debb-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="8debb-114">Zie [Tabel 3: platform-releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases) om na te gaan wanneer platform-updates gewoonlijk worden uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="8debb-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="8debb-115">Tweewekelijkse updates bieden een gefaseerde globale implementatie tussen regio's.</span><span class="sxs-lookup"><span data-stu-id="8debb-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="8debb-116">Zie [Nieuwe of gewijzigde functies in Dynamics 365 Human Resources](hr-admin-whats-new.md) voor meer informatie over tweewekelijkse updates.</span><span class="sxs-lookup"><span data-stu-id="8debb-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="8debb-117">Alle ondersteunde gegevenscentra worden tweewekelijks bijgewerkt, tenzij anders aangegeven.</span><span class="sxs-lookup"><span data-stu-id="8debb-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="8debb-118">In de volgende regio's worden tweewekelijkse updates uitgebracht: Verenigde Staten, Australië, Europa, Groot-Brittannië, Azië en Canada.</span><span class="sxs-lookup"><span data-stu-id="8debb-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="8debb-119">**Dataverse-oplossingsupdates**: deze updates worden ongeveer om de zes weken uitgevoerd, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="8debb-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="8debb-120">Deze bevatten nieuwe entiteiten en wijzigingen in bestaande entiteiten in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="8debb-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="8debb-121">Deze updates worden in dezelfde regio's uitgebracht als de tweewekelijkse updates en het duurt ongeveer zes weken voordat ze door alle datacentra zijn gerepliceerd.</span><span class="sxs-lookup"><span data-stu-id="8debb-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="8debb-122">Oplossingsupdates kunnen al dan niet samenvallen met tweewekelijkse service-updates.</span><span class="sxs-lookup"><span data-stu-id="8debb-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="8debb-123">Oplossingsupdates zijn beschikbaar in alle datacentra zodra deze zijn uitgebracht.</span><span class="sxs-lookup"><span data-stu-id="8debb-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="8debb-124">Als u niet wilt wachten totdat de updates automatisch worden gerepliceerd, kunt u deze updates handmatig toepassen op elke willekeurige omgeving in elk datacentrum.</span><span class="sxs-lookup"><span data-stu-id="8debb-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="8debb-125">Indien nodig biedt Human Resources ook de volgende typen oplossingen:</span><span class="sxs-lookup"><span data-stu-id="8debb-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="8debb-126">**Revisie (hotfix)**: foutcorrecties die kunnen optreden samen met, of los van, een tweewekelijkse service-updaterelease</span><span class="sxs-lookup"><span data-stu-id="8debb-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="8debb-127">**Noodoplossing**: proactieve en reactieve hotfixes die zelfstandig zijn, kunnen alleen configuratiewijzigingen of ook codewijzigingen bevatten om problemen met live-sites op te lossen en kunnen los van een tweewekelijkse service-updaterelease optreden</span><span class="sxs-lookup"><span data-stu-id="8debb-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="8debb-128">Releases worden beoordeeld, getest en gevalideerd in een interne omgeving.</span><span class="sxs-lookup"><span data-stu-id="8debb-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="8debb-129">Nadat de builds zijn afgemeld, worden ze geïmplementeerd voor productie.</span><span class="sxs-lookup"><span data-stu-id="8debb-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="8debb-130">Uitzonderingen in releasetempo in 2021</span><span class="sxs-lookup"><span data-stu-id="8debb-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="8debb-131">Om rekening te houden met feestdagen, is de releaseplanning voor november en december 2021 als volgt:</span><span class="sxs-lookup"><span data-stu-id="8debb-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="8debb-132">Release van november: 1 november - 14 november</span><span class="sxs-lookup"><span data-stu-id="8debb-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="8debb-133">Release van december: 29 november - 12 december</span><span class="sxs-lookup"><span data-stu-id="8debb-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="8debb-134">Her releasetempo van een keer per twee weken wordt op de gebruikelijke manier hervat op 10 januari 2022.</span><span class="sxs-lookup"><span data-stu-id="8debb-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="8debb-135">Berichtgeving</span><span class="sxs-lookup"><span data-stu-id="8debb-135">Communications</span></span>

<span data-ttu-id="8debb-136">Op de volgende locaties kunt u nagaan wat er is gepland voor Human Resources en wat we hebben uitgebracht:</span><span class="sxs-lookup"><span data-stu-id="8debb-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="8debb-137">Dynamics 365 Human Resources-roadmap</span><span class="sxs-lookup"><span data-stu-id="8debb-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="8debb-138">Dynamics 365-releaseplannen</span><span class="sxs-lookup"><span data-stu-id="8debb-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="8debb-139">Nieuwe of gewijzigde functies in Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="8debb-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="8debb-140">[Problemen zoeken in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (alleen voor fouten die betrekking hebben op platforms)</span><span class="sxs-lookup"><span data-stu-id="8debb-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="8debb-141">Human resources-blog</span><span class="sxs-lookup"><span data-stu-id="8debb-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="8debb-142">Human Resources Yammer-community</span><span class="sxs-lookup"><span data-stu-id="8debb-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="8debb-143">Preview-functies in een sandbox-omgeving</span><span class="sxs-lookup"><span data-stu-id="8debb-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="8debb-144">U kunt preview-functies in een sandbox-omgeving valideren voordat u deze in uw productie-omgeving inschakelt.</span><span class="sxs-lookup"><span data-stu-id="8debb-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="8debb-145">Zie [Overzicht van functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie over het inschakelen van nieuwe functies.</span><span class="sxs-lookup"><span data-stu-id="8debb-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="8debb-146">Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus.</span><span class="sxs-lookup"><span data-stu-id="8debb-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="8debb-147">De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode.</span><span class="sxs-lookup"><span data-stu-id="8debb-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="8debb-148">Zodra u nieuwe functies in het werkgebied Functiebeheer ziet, kunt u deze inschakelen.</span><span class="sxs-lookup"><span data-stu-id="8debb-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="8debb-149">Sommige functies zijn mogelijk standaard ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8debb-149">Some features may be on by default.</span></span>

<span data-ttu-id="8debb-150">Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied Functiebeheer).</span><span class="sxs-lookup"><span data-stu-id="8debb-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="8debb-151">Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen.</span><span class="sxs-lookup"><span data-stu-id="8debb-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="8debb-152">Het werkgebied Functiebeheer geeft aan wanneer een previewfunctie verplicht wordt.</span><span class="sxs-lookup"><span data-stu-id="8debb-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="8debb-153">Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen.</span><span class="sxs-lookup"><span data-stu-id="8debb-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="8debb-154">U kunt verplichte functies niet uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="8debb-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="8debb-155">Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="8debb-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="8debb-156">Het is raadzaam om de functies vooraf in een sandbox- of testomgeving te bekijken.</span><span class="sxs-lookup"><span data-stu-id="8debb-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="8debb-157">U kunt het beste een kopie van uw huidige productie-omgeving of database maken in een sandbox-omgeving, zodat u beschikt over de volledige ervaring van de nieuwe functies met uw gegevens.</span><span class="sxs-lookup"><span data-stu-id="8debb-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="8debb-158">Zie [Een Human Resources-project inrichten](hr-admin-setup-provision.md) voor meer informatie over het inrichten van een sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="8debb-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="8debb-159">Zie [Een exemplaar verwijderen](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment) als u een testomgeving wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8debb-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="8debb-160">Fouten rapporteren</span><span class="sxs-lookup"><span data-stu-id="8debb-160">Report bugs</span></span>

<span data-ttu-id="8debb-161">Tijdens het testen van preview-functies of het uitproberen van nieuwe mogelijkheden, is het mogelijk dat u items vindt die niet werken zoals u verwacht.</span><span class="sxs-lookup"><span data-stu-id="8debb-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="8debb-162">Meld eventuele fouten via [Microsoft Dynamics 365-ondersteuning](https://dynamics.microsoft.com/support/).</span><span class="sxs-lookup"><span data-stu-id="8debb-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="8debb-163">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8debb-163">See also</span></span>

[<span data-ttu-id="8debb-164">Releaseplannen voor Dynamics 365 en Power Platform</span><span class="sxs-lookup"><span data-stu-id="8debb-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="8debb-165">Nieuwe of gewijzigde functies in Dynamics 365 Human Resource</span><span class="sxs-lookup"><span data-stu-id="8debb-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8debb-166">Lifecycle-beleid voor software</span><span class="sxs-lookup"><span data-stu-id="8debb-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]