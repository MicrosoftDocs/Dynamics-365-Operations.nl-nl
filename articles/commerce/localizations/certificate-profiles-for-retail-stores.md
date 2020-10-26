---
title: Door gebruiker gedefinieerde certificaatprofielen voor winkels
description: Dit onderwerp biedt een overzicht van de manier waarop certificaten worden gebruikt in detailhandelwinkels.
author: josaw
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 0b8bf49a8eb78d0557ef105b40dd4cb5f0d24ce4
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973928"
---
# <a name="user-defined-certificate-profiles-for-retail-stores"></a><span data-ttu-id="eeb39-103">Door gebruiker gedefinieerde certificaatprofielen voor winkels</span><span class="sxs-lookup"><span data-stu-id="eeb39-103">User-defined certificate profiles for retail stores</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="eeb39-104">Overzicht</span><span class="sxs-lookup"><span data-stu-id="eeb39-104">Overview</span></span>

<span data-ttu-id="eeb39-105">Dit onderwerp biedt een overzicht van de certificaatprofielen die beschikbaar zijn in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eeb39-105">This topic provides an overview of the certificate profiles that are available in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="eeb39-106">Met deze functionaliteit wordt de functie [Geheimen voor detailhandelafzetkanalen beheren](../dev-itpro/manage-secrets.md) uitgebreid door ondersteuning voor lokale certificaten toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-106">This functionality extends the [Manage secrets for retail channels](../dev-itpro/manage-secrets.md) feature by adding support for local certificates.</span></span>

<span data-ttu-id="eeb39-107">Als het verkooppunt (POS/Point of Sale) wordt uitgevoerd in de offlinemodus, heeft het geen toegang tot de certificaten die zijn opgeslagen in de sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="eeb39-107">While the point of sale (POS) is running in offline mode, it can't access the certificates that are stored in the key vault.</span></span> <span data-ttu-id="eeb39-108">In plaats daarvan moet het lokale certificaat worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eeb39-108">The local certificate should be used instead.</span></span> <span data-ttu-id="eeb39-109">De volgende mogelijkheden worden ondersteund:</span><span class="sxs-lookup"><span data-stu-id="eeb39-109">The following capabilities are supported:</span></span>

- <span data-ttu-id="eeb39-110">Het gebruik van lokale certificaten in terugvalscenario's voor sleutelkluis</span><span class="sxs-lookup"><span data-stu-id="eeb39-110">Using local certificates in key vault fallback scenarios</span></span>
- <span data-ttu-id="eeb39-111">Het gebruik van lokale certificaten zonder een sleutelkluis (bijvoorbeeld in een on-premises installatie)</span><span class="sxs-lookup"><span data-stu-id="eeb39-111">Using local certificates without a key vault (for example in an on-premises installation)</span></span>
- <span data-ttu-id="eeb39-112">Een geleidelijke update van certificaten, waarbij sommige winkels en terminals een nieuwe versie van het certificaat gebruiken, maar andere winkels en terminals de vorige versie blijven gebruiken</span><span class="sxs-lookup"><span data-stu-id="eeb39-112">Gradual update of certificates, where some stores and terminals use a new version of the certificate, but other stores and terminals continue to use the previous version</span></span>

<span data-ttu-id="eeb39-113">Met de functie voor certificaatprofielen kunt u een standaardcertificaat opgeven en de volgorde instellen waarin certificaten in hetzelfde certificaatprofiel worden doorzocht.</span><span class="sxs-lookup"><span data-stu-id="eeb39-113">The certificate profiles functionality lets you specify a default certificate and set the order that certificates in the same certificate profile are searched in.</span></span> <span data-ttu-id="eeb39-114">Deze functionaliteit biedt ook een vergelijkbare instellingsmethode voor lokale certificaten en sleutelkluiscertificaten.</span><span class="sxs-lookup"><span data-stu-id="eeb39-114">This functionality also provides a similar setup approach for local certificates and Key Vault certificates.</span></span> <span data-ttu-id="eeb39-115">U kunt bedrijfsspecifieke instellingen voor certificaten toevoegen, maar de unieke ID tussen bedrijven voor elk certificaat kan worden gebruikt in de Commerce-kanalen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-115">You can add company-specific settings for certificates, but the unique cross-company identifier for each certificate can be used in the Commerce channels.</span></span>

### <a name="scenarios"></a><span data-ttu-id="eeb39-116">Scenario's</span><span class="sxs-lookup"><span data-stu-id="eeb39-116">Scenarios</span></span>

<span data-ttu-id="eeb39-117">De functionaliteit voor certificaatprofielen ondersteunt de volgende scenario's in Commerce-kanalen:</span><span class="sxs-lookup"><span data-stu-id="eeb39-117">The certificate profiles functionality supports the following scenarios in the Commerce channels:</span></span>

- <span data-ttu-id="eeb39-118">Het gebruik van een lokaal certificaat in terugvalscenario's voor sleutelkluis.</span><span class="sxs-lookup"><span data-stu-id="eeb39-118">Use a local certificate in key vault fallback scenarios.</span></span> <span data-ttu-id="eeb39-119">Hieronder volgen enkele voorbeelden van deze terugvalscenario´s:</span><span class="sxs-lookup"><span data-stu-id="eeb39-119">Here are some examples of these fallback scenarios:</span></span>

    - <span data-ttu-id="eeb39-120">De sleutelkluisopslag is niet toegankelijk.</span><span class="sxs-lookup"><span data-stu-id="eeb39-120">The key vault storage isn't accessible.</span></span>
    - <span data-ttu-id="eeb39-121">Er is geen certificaat gevonden in de sleutelkluisopslag.</span><span class="sxs-lookup"><span data-stu-id="eeb39-121">A certificate isn't found in the key vault storage.</span></span>
    - <span data-ttu-id="eeb39-122">Het verkooppunt (POS) wordt uitgevoerd in de offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="eeb39-122">The POS is running in offline mode.</span></span>

- <span data-ttu-id="eeb39-123">Gebruik lokale certificaten, maar zonder deze op te slaan in de sleutelkluis (bijvoorbeeld in een on-premises installatie).</span><span class="sxs-lookup"><span data-stu-id="eeb39-123">Use local certificates, but without storing them in the key vault (for example, in an on-premises installation).</span></span>
- <span data-ttu-id="eeb39-124">Voer een geleidelijke update van certificaten uit, waarbij een nieuwe versie van het certificaat alleen wordt gebruikt in winkels of op terminals waarin de nieuwe versie al beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="eeb39-124">Do a gradual update of certificates, where a new version of the certificate is used only in stores or on terminals where the new version is already available.</span></span>
- <span data-ttu-id="eeb39-125">Gebruik hetzelfde certificaat in meerdere bedrijven.</span><span class="sxs-lookup"><span data-stu-id="eeb39-125">Use the same certificate in several companies.</span></span>

## <a name="set-up-certificate-profiles"></a><span data-ttu-id="eeb39-126">Certificaatprofielen instellen</span><span class="sxs-lookup"><span data-stu-id="eeb39-126">Set up certificate profiles</span></span>

<span data-ttu-id="eeb39-127">In de volgende procedure wordt uitgelegd hoe u certificaatprofielen instelt.</span><span class="sxs-lookup"><span data-stu-id="eeb39-127">The following procedure explains how to set up certificate profiles.</span></span> <span data-ttu-id="eeb39-128">Voer de volgende stappen uit om de instellingen te configureren voordat u certificaatprofielen in Commerce-kanalen gaat gebruiken.</span><span class="sxs-lookup"><span data-stu-id="eeb39-128">Before you use certificate profiles in the Commerce channels, follow these steps to configure the settings.</span></span>

1. <span data-ttu-id="eeb39-129">Schakel in de werkruimte **Functiebeheer** de functie **Door gebruiker gedefinieerde certificaatprofielen voor winkels** in.</span><span class="sxs-lookup"><span data-stu-id="eeb39-129">In the **Feature management** workspace, turn on the **User-defined certificate profiles for retail stores** feature.</span></span>
2. <span data-ttu-id="eeb39-130">Ga naar **Systeembeheer \> Instellingen \> Certificaatprofielen**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-130">Go to **System administration \> Setup \> Certificate profiles**.</span></span>
3. <span data-ttu-id="eeb39-131">Maak een record en stel de velden **Certificaatprofiel**, **Naam** en **Beschrijving** voor de record in.</span><span class="sxs-lookup"><span data-stu-id="eeb39-131">Create a record, and set the **Certificate profile**, **Name**, and **Description** fields for it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eeb39-132">Het certificaatprofiel is een unieke ID van een certificaat voor alle bedrijven en Commerce-onderdelen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-132">The certificate profile is a unique identifier of a certificate across all companies and Commerce components.</span></span>

3. <span data-ttu-id="eeb39-133">Voeg op het tabblad **Rechtspersonen** een regel toe en selecteer de rechtspersoon (bedrijf) waarvoor het huidige certificaatprofiel moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="eeb39-133">On the **Legal entities** tab, add a line, and select the legal entity (company) that the current certificate profile should be used for.</span></span> <span data-ttu-id="eeb39-134">Als het certificaatprofiel moet worden gebruikt voor meerdere rechtspersonen, herhaalt u deze stap om een regel toe te voegen voor elke aanvullende rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="eeb39-134">If the certificate profile should be used for multiple legal entities, repeat this step to add a line for each additional legal entity.</span></span>
4. <span data-ttu-id="eeb39-135">Selecteer **Instellingen** om de pagina **Instellingen certificaatprofiel** te openen. Op deze pagina kunt u bedrijfsspecifieke instellingen voor het certificaatprofiel invoeren.</span><span class="sxs-lookup"><span data-stu-id="eeb39-135">Select **Settings** to open the **Certificate profile settings** page, where you can enter company-specific settings for the certificate profile.</span></span>

### <a name="certificate-profile-settings"></a><span data-ttu-id="eeb39-136">Instellingen voor certificaatprofielen</span><span class="sxs-lookup"><span data-stu-id="eeb39-136">Certificate profile settings</span></span>

<span data-ttu-id="eeb39-137">Wanneer u **Instellingen** voor certificaatprofielregels selecteert, wordt de pagina **Instellingen certificaatprofiel** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="eeb39-137">When you select **Settings** for certificate profile lines, the **Certificate profile settings** page appears.</span></span> <span data-ttu-id="eeb39-138">Op deze pagina kunt u opgeven welke certificaten kunnen worden gebruikt wanneer het huidige certificaatprofiel wordt aangeroepen in de Commerce-kanalen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-138">This page lets you specify which certificates can be used when the current certificate profile is called in the Commerce channels.</span></span> <span data-ttu-id="eeb39-139">U kunt ook de volgorde opgeven waarin certificaten moeten worden doorzocht.</span><span class="sxs-lookup"><span data-stu-id="eeb39-139">You can also specify the order that certificates should be searched in.</span></span>

> [!NOTE]
> <span data-ttu-id="eeb39-140">Het veld **Prioriteit** wordt automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="eeb39-140">The **Priority** field is automatically set.</span></span> <span data-ttu-id="eeb39-141">Een waarde van **1** staat voor de hoogste prioriteit.</span><span class="sxs-lookup"><span data-stu-id="eeb39-141">A value of **1** represents the highest priority.</span></span> <span data-ttu-id="eeb39-142">Wanneer een nieuwe regel op de pagina **Instellingen certificaatprofiel** wordt toegevoegd, wordt de prioriteit van de regel ingesteld op een nummer dat één hoger is dan de prioriteit van de vorige regel.</span><span class="sxs-lookup"><span data-stu-id="eeb39-142">When a new line is added on the **Certificate profile settings** page, its priority is set to a number that is one more than the priority of the previous line.</span></span> <span data-ttu-id="eeb39-143">Als u de prioriteit van een bepaalde regel wilt wijzigen, selecteert u de regel en selecteert u vervolgens **Omhoog** om de prioriteit te verhogen of **Omlaag** om de prioriteit te verlagen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-143">To change the priority of a specific line, select the line, and then select either **Move up** to increase the priority or **Move down** to decrease the priority.</span></span>

<span data-ttu-id="eeb39-144">Wanneer u een nieuwe regel toevoegt aan de pagina **Instellingen certificaatprofiel**, stelt u de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="eeb39-144">When you add a new line to the **Certificate profile settings** page, set the following fields:</span></span>

- <span data-ttu-id="eeb39-145">**Locatietype**: selecteer de locatie waar het certificaat is opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-145">**Location type** – Select the location where the certificate is stored.</span></span> <span data-ttu-id="eeb39-146">Dit veld heeft twee mogelijke waarden: **Lokaal certificaat** en **Sleutelkluis**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-146">This field has two possible values: **Local certificate** and **Key Vault**.</span></span>
- <span data-ttu-id="eeb39-147">**Sleutelkluiscertificaat**: dit veld is verplicht als u het veld **Locatietype** instelt op **Sleutelkluis**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-147">**Key Vault certificate** – This field is required if you set the **Location type** field to **Key Vault**.</span></span> <span data-ttu-id="eeb39-148">Gebruik dit veld om een geheim voor een sleutelkluiscertificaat op te geven.</span><span class="sxs-lookup"><span data-stu-id="eeb39-148">Use it to specify a Key Vault certificate secret.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eeb39-149">Voordat u een sleutelkluiscertificaat in certificaatprofielen gebruikt, moet u ervoor zorgen dat u een certificaat uploadt naar de sleutelkluisopslag en volgt u de instructies in [Client voor Azure-sleutelkluis instellen](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span><span class="sxs-lookup"><span data-stu-id="eeb39-149">Before you use a Key Vault certificate in certificate profiles, be sure to upload a certificate to the key vault storage, and follow the instructions in [Set up the Azure Key Vault client](https://docs.microsoft.com/dynamics365/finance/localizations/setting-up-azure-key-vault-client).</span></span>

- <span data-ttu-id="eeb39-150">**Winkelnaam**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-150">**Store name** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="eeb39-151">Gebruik dit veld om een standaardwinkelnaam op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.</span><span class="sxs-lookup"><span data-stu-id="eeb39-151">Use it to specify a default store name that should be used to search local certificates.</span></span>
- <span data-ttu-id="eeb39-152">**Winkellocatie**: dit veld is optioneel en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-152">**Store location** – This field is optional and is available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="eeb39-153">Gebruik dit veld om een standaardwinkellocatie op te geven die moet worden gebruikt voor het zoeken naar lokale certificaten.</span><span class="sxs-lookup"><span data-stu-id="eeb39-153">Use it to specify a default store location that should be used to search local certificates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eeb39-154">De standaardwinkelnaam en -winkellocatie worden toegevoegd om het zoeken naar lokale certificaten in Commerce Runtime te vereenvoudigen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-154">The default store name and store location are added to simplify the process of searching local certificates in the Commerce runtime.</span></span> <span data-ttu-id="eeb39-155">X509StoreProvider heeft een lijst met mappen waarin certificaten worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-155">X509StoreProvider has a list of folders where certificates are stored.</span></span> <span data-ttu-id="eeb39-156">Als de standaardwinkelnaam en de standaardwinkellocatie niet worden opgegeven, probeert X509StoreProvider een certificaat in de andere mappen in de lijst te vinden.</span><span class="sxs-lookup"><span data-stu-id="eeb39-156">If the default store name and the default store location aren't specified, X509StoreProvider tries to find a certificate in the other folders on its list.</span></span>

- <span data-ttu-id="eeb39-157">**Vingerafdruk**: dit veld is vereist en is alleen beschikbaar als u het veld **Locatietype** instelt op **Lokaal certificaat**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-157">**Thumbprint** – This field is required and available only if you set the **Location type** field to **Local certificate**.</span></span> <span data-ttu-id="eeb39-158">Gebruik dit veld om de vingerafdruk van het certificaat op te geven.</span><span class="sxs-lookup"><span data-stu-id="eeb39-158">Use it to specify the certificate thumbprint.</span></span>
- <span data-ttu-id="eeb39-159">**Opmerkingen**: dit veld is optioneel en gebruikers kunnen opmerkingen in dit veld invoeren.</span><span class="sxs-lookup"><span data-stu-id="eeb39-159">**Comments** – This field is optional and lets users enter notes.</span></span>

### <a name="workflow-searching-certificates-in-the-commerce-runtime"></a><span data-ttu-id="eeb39-160">Werkstroom: certificaten zoeken in Commerce Runtime</span><span class="sxs-lookup"><span data-stu-id="eeb39-160">Workflow: Searching certificates in the Commerce runtime</span></span>

<span data-ttu-id="eeb39-161">Dit is de basiswerkstroom die wordt gebruikt om te zoeken naar een certificaat wanneer een certificaatprofiel wordt aangeroepen in Commerce Runtime.</span><span class="sxs-lookup"><span data-stu-id="eeb39-161">Here is the basic workflow that is used to search for a certificate when a certificate profile is called in the Commerce runtime.</span></span>

1. <span data-ttu-id="eeb39-162">In het systeem wordt bepaald of het certificaatprofiel bedrijfsspecifieke instellingen voor de huidige rechtspersoon heeft.</span><span class="sxs-lookup"><span data-stu-id="eeb39-162">The system identifies whether the certificate profile has company-specific settings for the current legal entity.</span></span>
1. <span data-ttu-id="eeb39-163">Er wordt geprobeerd het certificaat te vinden aan de hand van de waarden op de pagina **Instellingen certificaatprofiel** voor de regel waarvan het veld **Prioriteit** is ingesteld op **1**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-163">The system tries to find the certificate by using the values on the **Certificate profile settings** page for the line where the **Priority** field is set to **1**.</span></span>

    - <span data-ttu-id="eeb39-164">Als het veld **Locatietype** is ingesteld op **Sleutelkluis**, wordt de waarde van het veld **Geheim voor sleutelkluiscertificaat** gebruikt om te zoeken naar het certificaat op de pagina **Parameters sleutelkluis**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-164">If the **Location type** field is set to **Key Vault**, the value of the **Key Vault certificate secret** field is used to search for the certificate on the **Key vault parameters** page.</span></span> <span data-ttu-id="eeb39-165">Het certificaat wordt vervolgens gezocht in de sleutelkluisopslag.</span><span class="sxs-lookup"><span data-stu-id="eeb39-165">The certificate is then searched for in the key vault storage.</span></span>
    - <span data-ttu-id="eeb39-166">Als het veld **Locatietype** is ingesteld op **Lokaal certificaat**, zoekt X509StoreProvider eerst naar het certificaat met behulp van de standaardwinkelnaam en de standaardwinkellocatie, als deze parameters zijn opgegeven.</span><span class="sxs-lookup"><span data-stu-id="eeb39-166">If the **Location type** field is set to **Local certificate**, X509StoreProvider first searches for the certificate by using the default store name and store location, if these parameters are specified.</span></span> <span data-ttu-id="eeb39-167">Vervolgens wordt in alle andere mappen in de lijst met mappen gezocht.</span><span class="sxs-lookup"><span data-stu-id="eeb39-167">It then searches in all other folders on its list of folders.</span></span>

1. <span data-ttu-id="eeb39-168">Als het certificaat niet wordt gevonden, wordt het proces herhaald voor de regel waarvan het veld **Prioriteit** is ingesteld op **2**, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="eeb39-168">If the certificate isn't found, the process is repeated for the line where the **Priority** field is set to **2**, and so on.</span></span>

> [!NOTE]
> <span data-ttu-id="eeb39-169">Als het certificaatprofiel geen instellingen heeft voor de huidige rechtspersoon of als de zoekopdracht naar het certificaat niet succesvol is voor alle regels op de pagina **Instellingen certificaatprofiel**, wordt het certificaat niet gevonden.</span><span class="sxs-lookup"><span data-stu-id="eeb39-169">If the certificate profile has no settings for the current legal entity, or if the certificate search is unsuccessful for all lines on the **Certificate profile settings** page, the certificate isn't found.</span></span>

#### <a name="caching-the-results-of-certificate-searches"></a><span data-ttu-id="eeb39-170">De resultaten van zoekopdrachten naar certificaten in de cache opslaan</span><span class="sxs-lookup"><span data-stu-id="eeb39-170">Caching the results of certificate searches</span></span>

<span data-ttu-id="eeb39-171">De resultaten van zoekopdrachten naar certificaten worden in de cache opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-171">The results of certificate searches are cached.</span></span> <span data-ttu-id="eeb39-172">De standaardvervaltijd voor een cache is één uur.</span><span class="sxs-lookup"><span data-stu-id="eeb39-172">The default expiration time for a cache is one hour.</span></span> <span data-ttu-id="eeb39-173">Deze tijd kan echter worden aangepast en kan worden ingesteld op een maximumwaarde van 24 uur.</span><span class="sxs-lookup"><span data-stu-id="eeb39-173">However, this time can be customized and can be set to a maximum value of 24 hours.</span></span>

### <a name="gradual-update"></a><span data-ttu-id="eeb39-174">Geleidelijke update</span><span class="sxs-lookup"><span data-stu-id="eeb39-174">Gradual update</span></span>

<span data-ttu-id="eeb39-175">Als er een nieuwe versie van het certificaat wordt ingevoerd, maar deze niet in alle winkels tegelijk kan worden bijgewerkt, kan het certificaat geleidelijk worden bijgewerkt met de functionaliteit voor certificaatprofielen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-175">If a new version of the certificate is introduced, but it can't be updated in all stores at the same time, the certificate profiles functionality enables the certificate to be updated gradually.</span></span>

1. <span data-ttu-id="eeb39-176">Zoek naar een certificaatprofiel en de regel die moeten worden bijgewerkt en selecteer vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="eeb39-176">Find a certificate profile and the line that should be updated, and then select **Settings**.</span></span>
1. <span data-ttu-id="eeb39-177">Voeg een regel toe en geef instellingen op die betrekking hebben op de meest recente versie van het certificaat.</span><span class="sxs-lookup"><span data-stu-id="eeb39-177">Add a line, and specify settings that are related to the latest version of the certificate.</span></span>
1. <span data-ttu-id="eeb39-178">Verhoog de waarde van **Prioriteit** van de nieuwe regel.</span><span class="sxs-lookup"><span data-stu-id="eeb39-178">Increase the **Priority** value of the new line.</span></span> <span data-ttu-id="eeb39-179">Gebruik de knop **Omhoog** om de regel zo te verplaatsen dat deze boven de regel staat voor de vorige versie van hetzelfde certificaat.</span><span class="sxs-lookup"><span data-stu-id="eeb39-179">Use the **Move up** button to move the line so that it's above the line for the previous version of the same certificate.</span></span>

> [!NOTE]
> <span data-ttu-id="eeb39-180">In Commerce Runtime wordt de nieuwe versie van het certificaat als eerste aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-180">In the Commerce runtime, the new version of the certificate will be called first.</span></span> <span data-ttu-id="eeb39-181">Als het certificaat in een specifieke winkel of op een specifieke terminal niet is bijgewerkt, wordt de vorige versie aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="eeb39-181">If the certificate hasn't yet been updated in a specific store or on a specific terminal, the previous version will be called.</span></span>