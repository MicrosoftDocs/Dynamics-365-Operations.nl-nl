---
title: Migratie Valuta-gegevenstype voor Twee keer wegschrijven
description: In dit onderwerp wordt beschreven hoe u het aantal decimalen wijzigt dat door Twee keer wegschrijven wordt ondersteund voor valuta.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456809"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="f6599-103">Migratie Valuta-gegevenstype voor Twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="f6599-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6599-104">U kunt het aantal decimalen dat voor valutawaarden wordt ondersteund, verhogen tot maximaal 10.</span><span class="sxs-lookup"><span data-stu-id="f6599-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="f6599-105">De standaard limiet is vier decimalen.</span><span class="sxs-lookup"><span data-stu-id="f6599-105">The default limit is four decimal places.</span></span> <span data-ttu-id="f6599-106">Door het aantal decimalen te verhogen voorkomt u gegevensverlies wanneer u met gegevens synchroniseert met Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="f6599-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="f6599-107">De verhoging van het aantal decimalen is een optionele wijziging.</span><span class="sxs-lookup"><span data-stu-id="f6599-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="f6599-108">Om dit te implementeren moet u ondersteuning vragen aan Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6599-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="f6599-109">Het proces waarbij het aantal decimalen wordt gewijzigd, heeft twee stappen:</span><span class="sxs-lookup"><span data-stu-id="f6599-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="f6599-110">De migratie aanvragen bij Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f6599-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="f6599-111">Het aantal decimalen wijzigen in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f6599-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="f6599-112">De Finance and Operations-app en Common Data Service moet hetzelfde aantal decimale posities in valutawaarden ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f6599-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="f6599-113">Anders kunnen gegevens verloren gaan wanneer de gegevens tussen apps worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="f6599-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="f6599-114">Het migratieproces configureert de manier waarop valuta- en wisselkoerswaarden worden opgeslagen, maar wijzigt geen gegevens.</span><span class="sxs-lookup"><span data-stu-id="f6599-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="f6599-115">Nadat de migratie is voltooid, kan het aantal decimalen voor valutacodes en prijzen worden verhoogd. De gegevens die gebruikers invoeren en weergeven, kunnen de decimalen nauwkeuriger aangeven.</span><span class="sxs-lookup"><span data-stu-id="f6599-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="f6599-116">Migratie is optioneel.</span><span class="sxs-lookup"><span data-stu-id="f6599-116">Migration is optional.</span></span> <span data-ttu-id="f6599-117">Als u meer decimalen wilt gebruiken, is het raadzaam om de migratie te overwegen.</span><span class="sxs-lookup"><span data-stu-id="f6599-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="f6599-118">Organisaties die geen waarden nodig hebben met meer dan vier decimalen, hoeven niet te worden gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="f6599-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="f6599-119">De migratie aanvragen bij Microsoft</span><span class="sxs-lookup"><span data-stu-id="f6599-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="f6599-120">Opslag voor bestaande valutavelden in Common Data Service kan niet meer dan vier decimalen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f6599-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="f6599-121">Daarom worden valutawaarden tijdens het migratieproces naar nieuwe interne velden in de database gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="f6599-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="f6599-122">Dit proces vindt voortdurend plaats totdat alle gegevens zijn gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="f6599-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="f6599-123">Intern worden de oude opslagtypen aan het eind van de migratie vervangen door de nieuwe opslagtypen, maar de gegevenswaarden blijven ongewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f6599-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="f6599-124">De valutavelden kunnen vervolgens maximaal 10 decimale posities ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="f6599-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="f6599-125">Tijdens het migratieproces kunt u Common Data Service zonder onderbreking blijven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f6599-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="f6599-126">Tegelijkertijd worden wisselkoersen gewijzigd, zodat ze maximaal 12 decimalen ondersteunen in plaats van de huidige limiet van 10.</span><span class="sxs-lookup"><span data-stu-id="f6599-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="f6599-127">Deze wijziging is vereist om ervoor te zorgen dat het aantal decimalen in de Finance and Operations-app hetzelfde is als in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f6599-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="f6599-128">Bij de migratie worden de gegevens niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="f6599-128">Migration doesn't change any data.</span></span> <span data-ttu-id="f6599-129">Nadat de velden met valuta en wisselkoers zijn geconverteerd, kunnen beheerders het systeem zo configureren dat er maximaal tien decimalen worden gebruikt voor valutavelden door het aantal decimalen voor elke transactievaluta en voor prijzen op te geven.</span><span class="sxs-lookup"><span data-stu-id="f6599-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="f6599-130">Een migratie aanvragen</span><span class="sxs-lookup"><span data-stu-id="f6599-130">Request a migration</span></span>

<span data-ttu-id="f6599-131">Om deze functie beschikbaar te maken stuurt u een e-mail naar **CDSExpandDecimal@microsoft.com** en voegt u de volgende informatie toe:</span><span class="sxs-lookup"><span data-stu-id="f6599-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="f6599-132">**Onderwerp:** aanvraag om ondersteuning voor uitgebreide decimalen in te schakelen voor \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="f6599-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="f6599-133">**Tekst:** Ik wil ondersteuning voor uitgebreide decimalen inschakelen voor mijn organisatie \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="f6599-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="f6599-134">Voor de vervolgstappen neemt een Microsoft-vertegenwoordiger binnen twee tot drie werkdagen contact met u op.</span><span class="sxs-lookup"><span data-stu-id="f6599-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="f6599-135">Wanneer u een migratie aanvraagt, moet u op de hoogte zijn van de volgende details en kunt u deze dienovereenkomstig plannen:</span><span class="sxs-lookup"><span data-stu-id="f6599-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="f6599-136">De benodigde tijd voor het migreren van de gegevens is afhankelijk van de hoeveelheid gegevens in het systeem.</span><span class="sxs-lookup"><span data-stu-id="f6599-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="f6599-137">De migratie van grote databases kan enkele dagen duren.</span><span class="sxs-lookup"><span data-stu-id="f6599-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="f6599-138">De grootte van de database neemt tijdelijk toe terwijl de migratie wordt uitgevoerd, omdat er extra ruimte nodig is voor indexen.</span><span class="sxs-lookup"><span data-stu-id="f6599-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="f6599-139">De meeste extra ruimte wordt vrijgemaakt wanneer de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f6599-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="f6599-140">Als er tijdens het migratieproces fouten optreden waardoor de migratie niet kan worden voltooid, stuurt het systeem waarschuwingen aan Microsoft Ondersteuning, zodat ondersteuningsmedewerkers kunnen ingrijpen.</span><span class="sxs-lookup"><span data-stu-id="f6599-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="f6599-141">Zelfs als er tijdens de migratie fouten optreden, blijft Common Data Service echter volledig beschikbaar voor normaal gebruik.</span><span class="sxs-lookup"><span data-stu-id="f6599-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="f6599-142">Het migratieproces kan niet ongedaan worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f6599-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="f6599-143">Het aantal decimalen wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f6599-143">Changing the number of decimal places</span></span>

<span data-ttu-id="f6599-144">Wanneer de migratie is voltooid, kunt u in Common Data Service getallen met meer decimalen opslaan.</span><span class="sxs-lookup"><span data-stu-id="f6599-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="f6599-145">Beheerders kunnen kiezen hoeveel decimalen er worden gebruikt voor specifieke valutacodes en voor prijzen.</span><span class="sxs-lookup"><span data-stu-id="f6599-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="f6599-146">Gebruikers van Microsoft Power Apps, Power BI en Power Automate kunnen getallen met meer decimalen weergeven en gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f6599-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="f6599-147">Als u deze wijziging wilt aanbrengen, moet u de volgende instellingen bijwerken in Power Apps:</span><span class="sxs-lookup"><span data-stu-id="f6599-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="f6599-148">**Systeeminstellingen: valutanauwkeurigheid voor prijzen**: het veld **Valutanauwkeurigheid instellen die in het systeem voor prijzen wordt gebruikt** bepaalt de manier waarop de valuta wordt berekend in de organisatie wanneer **Prijsprecisie** wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f6599-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="f6599-149">**Bedrijfsbeheer: Valuta's**: in het veld **Valutaprecisie** kunt u een aangepast aantal decimalen voor een bepaalde valuta opgeven.</span><span class="sxs-lookup"><span data-stu-id="f6599-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="f6599-150">Er is een terugval voor de instelling voor de gehele organisatie.</span><span class="sxs-lookup"><span data-stu-id="f6599-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="f6599-151">Er zijn enkele beperkingen:</span><span class="sxs-lookup"><span data-stu-id="f6599-151">There are some limitations:</span></span>

+ <span data-ttu-id="f6599-152">U kunt het valutaveld niet configureren voor een entiteit.</span><span class="sxs-lookup"><span data-stu-id="f6599-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="f6599-153">U kunt meer dan vier decimalen opgeven op de niveaus **Prijzen** en **Transactievaluta**.</span><span class="sxs-lookup"><span data-stu-id="f6599-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="f6599-154">Systeeminstellingen: Valutanauwkeurigheid voor prijzen</span><span class="sxs-lookup"><span data-stu-id="f6599-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="f6599-155">Beheerders kunnen de valutanauwkeurigheid instellen nadat de migratie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="f6599-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="f6599-156">Ga naar **Instellingen \> Beheer** en selecteer **Systeeminstellingen**.</span><span class="sxs-lookup"><span data-stu-id="f6599-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="f6599-157">Wijzig vervolgens op het tabblad **Algemeen** de waarde van het veld **Valutanauwkeurigheid instellen die in het systeem voor prijzen wordt gebruikt**, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f6599-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Systeeminstellingen voor valuta](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="f6599-159">Bedrijfsbeheer: Valuta's</span><span class="sxs-lookup"><span data-stu-id="f6599-159">Business Management: Currencies</span></span>

<span data-ttu-id="f6599-160">Als u wilt dat de valutanauwkeurigheid voor een bepaalde valuta afwijkt van de valutanauwkeurigheid die voor prijzen wordt gebruikt, kunt u deze wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f6599-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="f6599-161">Ga naar **Instellingen \> Bedrijfsbeheer**, selecteer **Valuta's** en selecteer de valuta die u wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="f6599-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="f6599-162">Vervolgens stelt u het veld **Valutanauwkeurigheid** in op het gewenste aantal decimalen, zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="f6599-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Valuta-instellingen voor een bepaalde landinstelling](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="f6599-164">Entiteiten: veld Valuta</span><span class="sxs-lookup"><span data-stu-id="f6599-164">Entities: Currency field</span></span>

<span data-ttu-id="f6599-165">Het aantal decimalen achter de komma dat kan worden geconfigureerd voor specifieke valutavelden is beperkt tot vier.</span><span class="sxs-lookup"><span data-stu-id="f6599-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>