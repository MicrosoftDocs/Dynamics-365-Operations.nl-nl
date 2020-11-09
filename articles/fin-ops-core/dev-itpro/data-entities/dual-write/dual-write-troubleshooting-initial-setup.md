---
title: Problemen tijdens eerste installatie oplossen
description: In dit onderwerp vindt u informatie over het oplossen van problemen die kunnen optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven met Finance and Operations- apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 6fb71a17d767a1e84511743794d85523db25eba8
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997345"
---
# <a name="troubleshoot-issues-during-initial-setup"></a><span data-ttu-id="eec32-103">Problemen tijdens eerste installatie oplossen</span><span class="sxs-lookup"><span data-stu-id="eec32-103">Troubleshoot issues during initial setup</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="eec32-104">Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eec32-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="eec32-105">In dit onderwerp vindt u specifieke informatie over het oplossen van problemen die kunnen optreden tijdens de eerste installatie van de integratie van twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="eec32-105">Specifically, it provides information that can help you fix issues that might occur during the initial setup of dual-write integration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eec32-106">In sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de referenties van de Microsoft Azure Active Directory-tenantbeheerder (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="eec32-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="eec32-107">In de sectie voor elk probleem wordt uitgelegd of een specifieke rol of referenties vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="eec32-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a><span data-ttu-id="eec32-108">U kunt een Finance and Operations-app niet koppelen met Common Data Service</span><span class="sxs-lookup"><span data-stu-id="eec32-108">You can't link a Finance and Operations app to Common Data Service</span></span>

<span data-ttu-id="eec32-109">**Vereiste rol om twee keer wegschrijven in te stellen:** systeembeheerder in Finance and Operations-apps en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="eec32-109">**Required role to set up dual-write:** System administrator in Finance and Operations apps and Common Data Service.</span></span>

<span data-ttu-id="eec32-110">Fouten op de pagina **Koppeling instellen met Common Data Service** worden meestal veroorzaakt door problemen met onvolledige instellingen of machtigingen.</span><span class="sxs-lookup"><span data-stu-id="eec32-110">Errors on the **Setup link to Common Data Service** page are usually caused by incomplete setup or permissions issues.</span></span> <span data-ttu-id="eec32-111">Controleer of de volledige statuscontrole is geslaagd op de pagina **Koppeling instellen met Common Data Service** , zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="eec32-111">Make sure that the whole health check passes on the **Setup link to Common Data Service** page, as shown in the following illustration.</span></span> <span data-ttu-id="eec32-112">U kunt twee keer wegschrijven niet koppelen, tenzij de hele statuscontrole is geslaagd.</span><span class="sxs-lookup"><span data-stu-id="eec32-112">You can't link dual-write unless the whole health check passes.</span></span>

![Geslaagde statuscontrole](media/health_check.png)

<span data-ttu-id="eec32-114">U moet beschikken over referenties als Azure AD-tenantbeheerder om te kunnen koppelen met de Finance and Operations-en Common Data Service-omgevingen.</span><span class="sxs-lookup"><span data-stu-id="eec32-114">You must have Azure AD tenant admin credentials to link the Finance and Operations and Common Data Service environments.</span></span> <span data-ttu-id="eec32-115">Nadat u de omgevingen hebt gekoppeld, kunnen gebruikers zich aanmelden met hun accountreferenties en een bestaande entiteitstoewijzing bijwerken.</span><span class="sxs-lookup"><span data-stu-id="eec32-115">After you link the environments, users can sign in by using their account credentials and update an existing entity map.</span></span>

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a><span data-ttu-id="eec32-116">Fout wanneer u de pagina Koppeling met Common Data Service opent</span><span class="sxs-lookup"><span data-stu-id="eec32-116">Error when you open the Link to Common Data Service page</span></span>

<span data-ttu-id="eec32-117">**Vereiste referenties om het probleem op te lossen:** Azure AD-tenantbeheerder</span><span class="sxs-lookup"><span data-stu-id="eec32-117">**Required credentials to fix the issue:** Azure AD tenant admin</span></span>

<span data-ttu-id="eec32-118">Mogelijk wordt het volgende foutbericht weergegeven wanneer u de pagina **Koppelen met Common Data Service** opent in en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="eec32-118">You might receive the following error message when you open the **Link to Common Data Service** page in a Finance and Operations app:</span></span>

<span data-ttu-id="eec32-119">*Statuscode van antwoord geeft geen positief resultaat: 404 (niet gevonden).*</span><span class="sxs-lookup"><span data-stu-id="eec32-119">*Response status code does not indicate success: 404 (Not Found).*</span></span>

<span data-ttu-id="eec32-120">Deze fout treedt op wanneer de goedkeuringsstap niet is voltooid.</span><span class="sxs-lookup"><span data-stu-id="eec32-120">This error occurs when the consent step hasn't been completed.</span></span> <span data-ttu-id="eec32-121">Als u wilt controleren of de goedkeuringsstap is voltooid, meldt u zich aan bij portal.Azure.com met behulp van het Azure AD-tenantbeheerdersaccount en controleert u of de app van de andere leverancier met de id **33976c19-1db5-4c02-810e-c243db79efde** verschijnt in de lijst met Azure AD- **ondernemingstoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="eec32-121">To validate whether the consent step has been completed, sign in to portal.Azure.com by using the Azure AD tenant admin account, and see whether the third-party app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** appears in the Azure AD **Enterprise applications** list.</span></span> <span data-ttu-id="eec32-122">Als dat niet zo is, moet u de app goedkeuren.</span><span class="sxs-lookup"><span data-stu-id="eec32-122">If it doesn't, you must provide app consent.</span></span>

<span data-ttu-id="eec32-123">Voer de volgende stappen uit om een app goed te keuren.</span><span class="sxs-lookup"><span data-stu-id="eec32-123">To provide app consent, follow these steps.</span></span>

1. <span data-ttu-id="eec32-124">Open de volgende URL met uw beheerdersreferenties.</span><span class="sxs-lookup"><span data-stu-id="eec32-124">Open the following URL by using your admin credentials.</span></span> <span data-ttu-id="eec32-125">U moet om toestemming worden gevraagd.</span><span class="sxs-lookup"><span data-stu-id="eec32-125">You should be prompted for consent.</span></span>

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. <span data-ttu-id="eec32-126">Selecteer **Accepteren** om aan te geven dat u uw toestemming geeft om de app met de id **33976c19-1db5-4c02-810e-c243db79efde** in uw tenant te installeren.</span><span class="sxs-lookup"><span data-stu-id="eec32-126">Select **Accept** to indicate that you're giving your consent to install the app that has the ID **33976c19-1db5-4c02-810e-c243db79efde** in your tenant.</span></span>

    > [!TIP]
    > <span data-ttu-id="eec32-127">Deze app is vereist om de apps Common Data Service en Finance and Operations te koppelen.</span><span class="sxs-lookup"><span data-stu-id="eec32-127">This app is required to link Common Data Service and Finance and Operations apps.</span></span> <span data-ttu-id="eec32-128">Als u problemen ondervindt met deze stap, opent u de browser in de modus Incognito (in Google Chrome) of InPrivate-modus (in Microsoft Edge).</span><span class="sxs-lookup"><span data-stu-id="eec32-128">If you have trouble with this step, open your browser in incognito mode (in Google Chrome) or InPrivate mode (in Microsoft Edge).</span></span>

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a><span data-ttu-id="eec32-129">Controleren of bedrijfsgegevens en teams voor twee keer wegschrijven op de juiste wijze zijn ingesteld tijdens het koppelen</span><span class="sxs-lookup"><span data-stu-id="eec32-129">Verify that company data and dual-write teams are set up correctly during linking</span></span>

<span data-ttu-id="eec32-130">Om er zeker van te zijn dat twee keer wegschrijven goed werkt, worden de bedrijven die u tijdens de configuratie selecteert, in de Common Data Service-omgeving gemaakt.</span><span class="sxs-lookup"><span data-stu-id="eec32-130">To ensure that dual-write works correctly, the companies that you select during configuration are created in the Common Data Service environment.</span></span> <span data-ttu-id="eec32-131">Standaard zijn deze bedrijven alleen-lezen en wordt de eigenschap **IsDualWriteEnable** ingesteld op **True**.</span><span class="sxs-lookup"><span data-stu-id="eec32-131">By default, these companies are read-only, and the **IsDualWriteEnable** property is set to **True**.</span></span> <span data-ttu-id="eec32-132">Daarnaast worden de standaard bedrijfseenheid die eigenaar is en het team gemaakt en wordt de bedrijfsnaam opgenomen.</span><span class="sxs-lookup"><span data-stu-id="eec32-132">In addition, the default owning business unit owner and team are created and include the company name.</span></span> <span data-ttu-id="eec32-133">Voordat u de toewijzingen inschakelt, controleert u of de standaard eigenaar van het team is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="eec32-133">Before you enable the maps, verify that the default team owner is specified.</span></span> <span data-ttu-id="eec32-134">Voer de volgende stappen uit om de entiteit **Bedrijven (CDM\_Company)** te zoeken.</span><span class="sxs-lookup"><span data-stu-id="eec32-134">To find the **Companies (CDM\_Company)** entity, follow these steps.</span></span>

1. <span data-ttu-id="eec32-135">Selecteer in de modelgestuurde app in Dynamics 365 het filter in de rechterbovenhoek.</span><span class="sxs-lookup"><span data-stu-id="eec32-135">In the model-driven app in Dynamics 365, select the filter in the upper-right corner.</span></span>
2. <span data-ttu-id="eec32-136">Selecteer **Bedrijf** in de vervolgkeuzelijst.</span><span class="sxs-lookup"><span data-stu-id="eec32-136">In the drop-down list, select **Company**.</span></span>
3. <span data-ttu-id="eec32-137">Selecteer **Uitvoeren** om de resultaten weer te geven.</span><span class="sxs-lookup"><span data-stu-id="eec32-137">Select **Run** to see the results.</span></span>
4. <span data-ttu-id="eec32-138">Selecteer het bedrijf dat was gekoppeld tijdens het configureren van twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="eec32-138">Select the company that was linked when you configured dual-write.</span></span>
5. <span data-ttu-id="eec32-139">Controleer of het veld **Standaardeigenaarsteam** een waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="eec32-139">Verify that the **Default owning team** field has a value.</span></span> <span data-ttu-id="eec32-140">In de volgende afbeelding is het veld **Standaardeigenaarsteam** ingesteld op **USMF twee keer wegschrijven**.</span><span class="sxs-lookup"><span data-stu-id="eec32-140">In the following illustration, the **Default owning team** field is set to **USMF Dual Write**.</span></span>

    ![Het standaardeigenaarsteam controleren](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a><span data-ttu-id="eec32-142">De limiet zoeken voor het aantal rechtspersonen of bedrijven dat kan worden gekoppeld voor twee keer wegschrijven</span><span class="sxs-lookup"><span data-stu-id="eec32-142">Find the limit on the number of legal entities or companies that can be linked for dual-write</span></span>

<span data-ttu-id="eec32-143">Mogelijk wordt het volgende foutbericht weergegeven wanneer u toewijzingen probeert in te schakelen:</span><span class="sxs-lookup"><span data-stu-id="eec32-143">You might receive the following error message when you try to enable maps:</span></span>

<span data-ttu-id="eec32-144">*Fout met twee keer wegschrijven - Registratie van invoegtoepassing mislukt: \[(Kan partitietoewijzing voor project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea niet ophalen. Fout: de maximum toegestane partities overschreden voor toewijzing DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Er zijn een of meer fouten opgetreden.*</span><span class="sxs-lookup"><span data-stu-id="eec32-144">*Dual write failure - Plugin registration failed: \[(Unable to get partition map for project DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Error Exceeds the maximum partitions allowed for mapping DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], One or more errors occurred.*</span></span>

<span data-ttu-id="eec32-145">De huidige limiet voor het koppelen van de omgevingen is ongeveer 40 rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="eec32-145">The current limit when you link the environments is approximately 40 legal entities.</span></span> <span data-ttu-id="eec32-146">Deze fout treedt op als u toewijzingen probeert in te schakelen en er meer dan 40 rechtspersonen tussen de omgevingen zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="eec32-146">This error occurs if you try to enable maps, and more than 40 legal entities are linked between the environments.</span></span>
