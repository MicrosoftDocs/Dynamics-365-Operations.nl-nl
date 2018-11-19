---
title: Fiscale integratie voor detailhandelafzetkanaal
description: Dit onderwerp biedt een overzicht van de fiscale integratie voor Retail POS.
author: josaw
manager: annbe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile, RetailFormLayout, RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-11-1
ms.dyn365.ops.version: 8.1.1
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: c852d095505abecbd44d29e9e7b53875e9069def
ms.contentlocale: nl-nl
ms.lasthandoff: 11/01/2018

---
# <a name="fiscal-integration-for-retail-channel"></a><span data-ttu-id="2bddb-103">Fiscale integratie voor detailhandelafzetkanaal</span><span class="sxs-lookup"><span data-stu-id="2bddb-103">Fiscal integration for Retail channel</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2bddb-104">In dit onderwerp wordt een overzicht gegeven van de functionaliteit voor fiscale integratie die beschikbaar is in Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="2bddb-104">This topic is an overview of the fiscal integration functionality that is available in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="2bddb-105">De functionaliteit voor fiscale integratie is een raamwerk ter ondersteuning van fiscale wetgeving die erop gericht is om fraude in de detailhandel te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-105">The fiscal integration functionality is a framework designed to support local fiscal laws that are aimed to prevent fraud in the Retail industry.</span></span> <span data-ttu-id="2bddb-106">Typische scenario's die kunnen worden gedekt door fiscale integratie omvatten:</span><span class="sxs-lookup"><span data-stu-id="2bddb-106">Typical scenarios that could be covered by using fiscal integration include:</span></span>

- <span data-ttu-id="2bddb-107">Een fiscaal ontvangstbewijs afdrukken en geven aan de klant.</span><span class="sxs-lookup"><span data-stu-id="2bddb-107">Printing a fiscal receipt and giving it to the customer.</span></span>
- <span data-ttu-id="2bddb-108">De indiening beveiligen van informatie die gerelateerd is aan verkopen en retouren die worden uitgevoerd op het POS, bij een externe service die wordt geboden door de belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="2bddb-108">Securing the submission of the information related to sales and returns performed on POS to an external service provided by the authority.</span></span>
- <span data-ttu-id="2bddb-109">Gegevensbeveiliging gebruiken met een digitale handtekening die door de belastingdienst is geautoriseerd.</span><span class="sxs-lookup"><span data-stu-id="2bddb-109">Using data protection with a digital signature authorized by the authority.</span></span>

<span data-ttu-id="2bddb-110">Dit onderwerp bevat richtlijnen voor het instellen van fiscale integratie, zodat gebruikers de volgende taken kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2bddb-110">This topic provides guidelines for setting up fiscal integration so users can perform the following tasks.</span></span> 

- <span data-ttu-id="2bddb-111">Fiscale connectors configureren. Dit zijn fiscale apparaten of services die worden gebruikt voor fiscale registratiedoeleinden zoals opslaan, digitale handtekeningen en beveiligde indiening van belastinggegevens.</span><span class="sxs-lookup"><span data-stu-id="2bddb-111">Configure fiscal connectors, which are fiscal devices or services used for fiscal registration purposes like saving, digital signatures, and secured submission of fiscal data.</span></span>
- <span data-ttu-id="2bddb-112">De documentprovider configureren, die een uitvoermethode en een algoritme voor het genereren van fiscale documenten definieert.</span><span class="sxs-lookup"><span data-stu-id="2bddb-112">Configure the document provider, which defines an output method and an algorithm of fiscal document generation.</span></span>
- <span data-ttu-id="2bddb-113">Het fiscale registratieproces configureren, dat een sequentie van stappen definieert en een groep connectors die in elke stap worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2bddb-113">Configure the fiscal registration process, which is defines a sequence of steps and a group of connectors used on each step.</span></span>
- <span data-ttu-id="2bddb-114">Fiscale registratieprocessen toewijzen aan POS-functionaliteitsprofielen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-114">Assign fiscal registration processes to POS functionality profiles.</span></span>
- <span data-ttu-id="2bddb-115">Connectortechnische profielen toewijzen aan hardwareprofielen (voor de locale fiscale connectors) of aan POS-functionaliteitsprofielen (voor andere fiscale connectortypen).</span><span class="sxs-lookup"><span data-stu-id="2bddb-115">Assign connector technical profiles, either to hardware profiles (for the local fiscal connectors) or to POS functionality profiles (for other fiscal connector types).</span></span>

## <a name="fiscal-integration-execution-flow"></a><span data-ttu-id="2bddb-116">Uitvoeringsstroom voor fiscale integratie</span><span class="sxs-lookup"><span data-stu-id="2bddb-116">Fiscal integration execution flow</span></span>
<span data-ttu-id="2bddb-117">In het volgende scenario ziet u de gemeenschappelijke uitvoeringsstroom voor fiscale integratie.</span><span class="sxs-lookup"><span data-stu-id="2bddb-117">The following scenario shows the common fiscal integration execution flow.</span></span>

1. <span data-ttu-id="2bddb-118">Initialisatie van het fiscale registratieproces.</span><span class="sxs-lookup"><span data-stu-id="2bddb-118">Initialization of the fiscal registration process.</span></span>
  
   <span data-ttu-id="2bddb-119">Na het uitvoeren van sommige acties waar fiscale registratie vereist is, bijvoorbeeld nadat een detailhandelstransactie is uitgevoerd, wordt het fiscale registratieproces gekoppeld aan het huidige POS-functionaliteitsprofiel.</span><span class="sxs-lookup"><span data-stu-id="2bddb-119">After performing some actions where fiscal registration is required, such as after a retail transaction has been concluded, the fiscal registration process is associated with the current POS functionality profile.</span></span>

1. <span data-ttu-id="2bddb-120">Zoeken naar een fiscale connector.</span><span class="sxs-lookup"><span data-stu-id="2bddb-120">Search for a fiscal connector.</span></span>
   
   <span data-ttu-id="2bddb-121">Voor elke fiscale registratiestap die is opgenomen in het fiscale registratieproces, zoekt het systeem overeenkomst met de lijst met fiscale connectors.</span><span class="sxs-lookup"><span data-stu-id="2bddb-121">For each fiscal registration step included in the fiscal registration process, the system matches the list of fiscal connectors.</span></span> <span data-ttu-id="2bddb-122">Deze connectors hebben een functioneel profiel dat is opgenomen in de opgegeven connectorgroep, met een lijst connectors die een technisch profiel hebben gekoppeld aan het huidige hardwareprofiel (alleen voor een connectortype dat gelijk is aan **Lokaal**) of aan het huidige POS-functionaliteitsprofiel (voor andere connectortypen).</span><span class="sxs-lookup"><span data-stu-id="2bddb-122">These connectors have a functional profile included in the specified connector group, with a list of connectors that have a technical profile associated with the current hardware profile (for a connector type that equals **Local** only) or with the current POS functionality profile (for other connector types).</span></span>
   
1. <span data-ttu-id="2bddb-123">De fiscale integratie uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="2bddb-123">Perform the fiscal integration.</span></span>

   <span data-ttu-id="2bddb-124">Het systeem voert alle benodigde acties uit die worden gedefinieerd door een assembly die is gekoppeld aan de gevonden connector.</span><span class="sxs-lookup"><span data-stu-id="2bddb-124">The system executes all necessary actions defined by an assembly linked with the found connector.</span></span> <span data-ttu-id="2bddb-125">Dit wordt gedaan overeenkomstig de instellingen van het functionele profiel en het technische profiel die in de vorige stap voor deze connector zijn gevonden.</span><span class="sxs-lookup"><span data-stu-id="2bddb-125">This is done in accordance with the settings of the functional profile and technical profile that were found on the previous step for this connector.</span></span>

## <a name="setup-needed-before-using-fiscal-integration"></a><span data-ttu-id="2bddb-126">Instelling die nodig is vóór gebruik van fiscale integratie</span><span class="sxs-lookup"><span data-stu-id="2bddb-126">Setup needed before using fiscal integration</span></span>
<span data-ttu-id="2bddb-127">Voordat u de functionaliteit voor fiscale integratie gebruikt, moet u de volgende instellingen definiëren:</span><span class="sxs-lookup"><span data-stu-id="2bddb-127">Before using the fiscal integration functionality, you should define the following settings:</span></span>

- <span data-ttu-id="2bddb-128">Definieer de getalreeks op de pagina **Detailhandelparameters** voor het nummer van het fiscale functionele profiel.</span><span class="sxs-lookup"><span data-stu-id="2bddb-128">Define the number sequence on the **Retail parameters** page for the fiscal functional profile number.</span></span>
  
- <span data-ttu-id="2bddb-129">Definieer de getalreeksen op de pagina **Gedeelde parameters detailhandel** voor de volgende referenties:</span><span class="sxs-lookup"><span data-stu-id="2bddb-129">Define the number sequences on the **Retail shared parameters** page for the following references:</span></span>
  
  - <span data-ttu-id="2bddb-130">Nummer van fiscaal technisch profiel</span><span class="sxs-lookup"><span data-stu-id="2bddb-130">Fiscal technical profile number</span></span>
  - <span data-ttu-id="2bddb-131">Nummer fiscale connectorgroep</span><span class="sxs-lookup"><span data-stu-id="2bddb-131">Fiscal connector group number</span></span>
  - <span data-ttu-id="2bddb-132">Nummer van registratieproces</span><span class="sxs-lookup"><span data-stu-id="2bddb-132">Registration process number</span></span>

- <span data-ttu-id="2bddb-133">Maak een **fiscale connector** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale verbindingen** voor elk apparaat of elke service die u wilt gebruiken voor fiscale integratie.</span><span class="sxs-lookup"><span data-stu-id="2bddb-133">Create a **Fiscal connector** in **Retail > Channel setup > Fiscal integration > Fiscal connectors** for each device or service that you plan to use for fiscal integration purposes.</span></span>

-  <span data-ttu-id="2bddb-134">Maak een **Fiscale documentprovider** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale documentproviders** voor alle fiscale connectors.</span><span class="sxs-lookup"><span data-stu-id="2bddb-134">Create a **Fiscal document provider** in **Retail > Channel setup > Fiscal integration > Fiscal document providers** for all fiscal connectors.</span></span> <span data-ttu-id="2bddb-135">Toewijzing van gegevens wordt beschouwd als onderdeel van de fiscale documentprovider.</span><span class="sxs-lookup"><span data-stu-id="2bddb-135">Data mapping is considered a part of the fiscal document provider.</span></span> <span data-ttu-id="2bddb-136">Als u andere toewijzingen van gegevens voor de dezelfde connector wilt instellen (zoals staatspecifieke regelgeving), moet u verschillende fiscale documentproviders maken.</span><span class="sxs-lookup"><span data-stu-id="2bddb-136">To set up different data mappings for the same connector (like state-specific regulations), you should create different fiscal document providers.</span></span>

- <span data-ttu-id="2bddb-137">Maak een **functioneel connectorprofiel** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Functionele connectorprofielen** voor elke fiscale documentprovider.</span><span class="sxs-lookup"><span data-stu-id="2bddb-137">Create a **Connector functional profile** in **Retail > Channel setup > Fiscal integration > Connector functional profiles** for each fiscal document provider.</span></span>
  - <span data-ttu-id="2bddb-138">Selecteer een connectornaam.</span><span class="sxs-lookup"><span data-stu-id="2bddb-138">Select a connector name.</span></span>
  - <span data-ttu-id="2bddb-139">Selecteer een documentprovider.</span><span class="sxs-lookup"><span data-stu-id="2bddb-139">Select a document provider.</span></span>
  - <span data-ttu-id="2bddb-140">Geef btw-tarieven op het tabblad **Instelling service** op.</span><span class="sxs-lookup"><span data-stu-id="2bddb-140">Specify VAT rates settings on the **Service setup** tab.</span></span>
  - <span data-ttu-id="2bddb-141">Geef de toewijzing van btw-codes en de toewijzing van betalingsmethoden op het tabblad **Toewijzing van gegevens** op.</span><span class="sxs-lookup"><span data-stu-id="2bddb-141">Specify VAT codes mapping and tender type mapping on the **Data mapping** tab.</span></span>

  #### <a name="examples"></a><span data-ttu-id="2bddb-142">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="2bddb-142">Examples</span></span> 

  |  | <span data-ttu-id="2bddb-143">Opmaak</span><span class="sxs-lookup"><span data-stu-id="2bddb-143">Format</span></span> | <span data-ttu-id="2bddb-144">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2bddb-144">Example</span></span> | 
  |--------|--------|--------|
  | <span data-ttu-id="2bddb-145">Btw-tariefinstellingen</span><span class="sxs-lookup"><span data-stu-id="2bddb-145">VAT rates settings</span></span> | <span data-ttu-id="2bddb-146">waarde : VATrate</span><span class="sxs-lookup"><span data-stu-id="2bddb-146">value : VATrate</span></span> | <span data-ttu-id="2bddb-147">1 : 2000, 2 : 1800</span><span class="sxs-lookup"><span data-stu-id="2bddb-147">1 : 2000, 2 : 1800</span></span> |
  | <span data-ttu-id="2bddb-148">Toewijzing van btw-codes</span><span class="sxs-lookup"><span data-stu-id="2bddb-148">VAT codes mapping</span></span> | <span data-ttu-id="2bddb-149">VATcode : waarde</span><span class="sxs-lookup"><span data-stu-id="2bddb-149">VATcode : value</span></span> | <span data-ttu-id="2bddb-150">vat20 : 1, vat18 : 2</span><span class="sxs-lookup"><span data-stu-id="2bddb-150">vat20 : 1, vat18 : 2</span></span> |
  | <span data-ttu-id="2bddb-151">Toewijzing van betalingsmethoden</span><span class="sxs-lookup"><span data-stu-id="2bddb-151">Tender types mapping</span></span> | <span data-ttu-id="2bddb-152">TenderTyp: waarde</span><span class="sxs-lookup"><span data-stu-id="2bddb-152">TenderTyp : value</span></span> | <span data-ttu-id="2bddb-153">Contant : 1, Kaart : 2</span><span class="sxs-lookup"><span data-stu-id="2bddb-153">Cash : 1, Card : 2</span></span> |

- <span data-ttu-id="2bddb-154">Maak **fiscale connectorgroepen** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscale connectorgroep**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-154">Create **Fiscal connector groups** in **Retail > Channel setup > Fiscal integration > Fiscal connector group**.</span></span> <span data-ttu-id="2bddb-155">Een connectorgroep is een subset van functionele profielen die zijn gekoppeld aan fiscale connectors die identieke functies uitvoeren en worden gebruikt in dezelfde fase binnen een fiscaal registratieproces.</span><span class="sxs-lookup"><span data-stu-id="2bddb-155">A connector group is a subset of functional profiles linked with fiscal connectors that perform identical functions and are used at the same stage within a fiscal registration process.</span></span>

   - <span data-ttu-id="2bddb-156">Voeg functionele profielen toe aan de connectorgroep.</span><span class="sxs-lookup"><span data-stu-id="2bddb-156">Add functional profiles to the connector group.</span></span> <span data-ttu-id="2bddb-157">Klik op **Toevoegen** op de pagina **Functionele profielen** en selecteer een profielnummer.</span><span class="sxs-lookup"><span data-stu-id="2bddb-157">Click **Add** on the **Functional profiles** page and select a profile number.</span></span>
   - <span data-ttu-id="2bddb-158">Als u gebruik van het functionele profiel wilt onderbreken, stelt u **Uitschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-158">If you want to suspend usage of the functional profile, set **Disable** to **Yes**.</span></span> 
   
     <span data-ttu-id="2bddb-159">Deze wijziging is alleen van invloed op de huidige connectorgroep.</span><span class="sxs-lookup"><span data-stu-id="2bddb-159">This change affects the current connector group only.</span></span> <span data-ttu-id="2bddb-160">U kunt doorgaan met hetzelfde functionele profiel in andere connectorgroepen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-160">You can continue using the same functional profile in other connector groups.</span></span>

     >[!NOTE]
     > <span data-ttu-id="2bddb-161">Binnen een connectorgroep kan elke fiscale connector slechts één functioneel profiel hebben.</span><span class="sxs-lookup"><span data-stu-id="2bddb-161">Within a connector group, each fiscal connector can only have one functional profile.</span></span>

- <span data-ttu-id="2bddb-162">Maak een **technisch connectorprofiel** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Technische connectorprofielen** voor elke fiscale connector.</span><span class="sxs-lookup"><span data-stu-id="2bddb-162">Create a **Connector technical profile** in **Retail > Channel setup > Fiscal integration > Connector technical profiles** for each fiscal connector.</span></span>
  - <span data-ttu-id="2bddb-163">Selecteer een connectornaam.</span><span class="sxs-lookup"><span data-stu-id="2bddb-163">Select a connector name.</span></span>
  - <span data-ttu-id="2bddb-164">Selecteer een connectortype:</span><span class="sxs-lookup"><span data-stu-id="2bddb-164">Select a connector type:</span></span> 
      - <span data-ttu-id="2bddb-165">**Lokaal**: stel dit type in voor fysieke apparaten of toepassingen die zijn geïnstalleerd op een lokale computer.</span><span class="sxs-lookup"><span data-stu-id="2bddb-165">**Local** - Set this type for physical devices or applications installed on a local machine.</span></span>
      - <span data-ttu-id="2bddb-166">**Intern**: stel dit type in voor fiscale apparaten en services die zijn verbonden met Retail Server.</span><span class="sxs-lookup"><span data-stu-id="2bddb-166">**Internal** - Set this type for fiscal devices and services connected to Retail Server.</span></span>
      - <span data-ttu-id="2bddb-167">**Extern**: voor externe fiscale services, zoals een webportal dat wordt verschaft door een belastingdienst.</span><span class="sxs-lookup"><span data-stu-id="2bddb-167">**External** - For external fiscal services like a web-portal provided by a tax authority.</span></span>
    
  - <span data-ttu-id="2bddb-168">Geef instellingen op het tabblad **Verbinding** op.</span><span class="sxs-lookup"><span data-stu-id="2bddb-168">Specify settings on the **Connection** tab.</span></span>

      
 >[!NOTE]
 > <span data-ttu-id="2bddb-169">Een bijgewerkte versie van een configuratie die eerder is geladen, wordt geladen voor zowel functionele als technische profielen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-169">An updated version of a configuration that was loaded earlier will be loaded for both functional and technical profiles.</span></span> <span data-ttu-id="2bddb-170">Als een juiste connector of documentprovider al in gebruik is, wordt u geïnformeerd.</span><span class="sxs-lookup"><span data-stu-id="2bddb-170">If an appropriate connector or document provider is already in use, you will be notified.</span></span> <span data-ttu-id="2bddb-171">Standaard worden alle wijzigingen die handmatig zijn aangebracht in de functionele en technische profielen, opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-171">By default, all changes that have been made manually in functional and technical profiles will be stored.</span></span> <span data-ttu-id="2bddb-172">Als u deze profielen wilt overschrijven met de standaardset parameters uit een configuratie, klikt u op **Bijwerken** op de pagina **Functionele connectorprofielen** en de pagina **Technische connectorprofielen**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-172">In order to override these profiles with the default set of parameters from a configuration, click **Update** on the **Connector functional profiles** page and **Connector technical profiles** page.</span></span>
 
- <span data-ttu-id="2bddb-173">Maak een **fiscaal registratieproces** in **Detailhandel > Afzetkanaalinstellingen > Fiscale integratie > Fiscaal registratieproces** voor elk uniek proces van de fiscale integratie.</span><span class="sxs-lookup"><span data-stu-id="2bddb-173">Create a **Fiscal registration process** in **Retail > Channel setup > Fiscal integration > Fiscal registration processes** for each unique process of the fiscal integration.</span></span> <span data-ttu-id="2bddb-174">Een registratieproces wordt gedefinieerd door de volgorde van de registratiestappen en de connectorgroep die in elke stap worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2bddb-174">A registration process is defined by the sequence of the registration steps and the connector group used on each step.</span></span> 
  
  - <span data-ttu-id="2bddb-175">Voeg registratiestappen aan het proces toe:</span><span class="sxs-lookup"><span data-stu-id="2bddb-175">Add registration steps to the process:</span></span>
      - <span data-ttu-id="2bddb-176">Klik op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-176">Click **Add**.</span></span>
      - <span data-ttu-id="2bddb-177">Selecteer een connectortype.</span><span class="sxs-lookup"><span data-stu-id="2bddb-177">Select a connector type.</span></span>
      
      >[!NOTE]
      > <span data-ttu-id="2bddb-178">Dit veld bepaalt waar wordt gezocht in een technisch profiel voor de connector: in hardwareprofielen voor connectortype **Lokaal** of in POS-functionaliteitsprofielen voor andere fiscale connectortypen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-178">This field defines where the system will search in a technical profile for the connector, either in hardware profiles for connector type **Local**, or in POS functionality profiles for other fiscal connector types.</span></span>
      
   - <span data-ttu-id="2bddb-179">Selecteer een connectorgroep.</span><span class="sxs-lookup"><span data-stu-id="2bddb-179">Select a connector group.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="2bddb-180">Klik op **Valideren** om de integriteit van de structuur van het registratieproces te controleren.</span><span class="sxs-lookup"><span data-stu-id="2bddb-180">Click **Validate** to check the integrity of the registration process structure.</span></span> <span data-ttu-id="2bddb-181">U wordt aangeraden validaties uit te voeren in de volgende gevallen:</span><span class="sxs-lookup"><span data-stu-id="2bddb-181">It’s recommended that validations be made in the following cases:</span></span>
       >- <span data-ttu-id="2bddb-182">Voor een nieuw registratieproces nadat alle de instellingen zijn voltooid, met inbegrip van binding met POS-functionaliteitsprofielen en hardwareprofielen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-182">For a new registration process after all the settings are completed, including binding to POS functionality profiles and hardware profiles.</span></span>
       >- <span data-ttu-id="2bddb-183">Na het aanbrengen van updates in een bestaand registratieproces.</span><span class="sxs-lookup"><span data-stu-id="2bddb-183">After making updates to an existing registration process.</span></span>

-  <span data-ttu-id="2bddb-184">Verbind fiscale registratieprocessen met POS-functionaliteitsprofielen in **Detailhandel > Afzetkanaalinstellingen > POS-instellingen > POS-profielen > Functionaliteitsprofielen**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-184">Bind fiscal registration processes to POS functionality profiles in **Retail > Channel setup > POS setup > POS profiles > Functionality profiles**.</span></span>
   - <span data-ttu-id="2bddb-185">Klik op **Bewerken** en selecteer een **Procesnummer** op het tabblad **Fiscaal registratieproces**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-185">Click **Edit** and select a **Process number** on the **Fiscal registration process** tab.</span></span>
- <span data-ttu-id="2bddb-186">Verbind de technische connectorprofielen met de hardwareprofielen in **Detailhandel > Afzetkanaalinstellingen > POS-instellingen > POS-profielen > Hardwareprofielen**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-186">Bind the connector technical profiles to the hardware profiles in **Retail > Channel setup > POS setup > POS profiles > Hardware profiles**.</span></span>
   - <span data-ttu-id="2bddb-187">Klik op **bewerken** en klik vervolgens op **Nieuw** op het tabblad **Fiscaal technisch profiel**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-187">Click **Edit**, then click **New** on the **Fiscal technical profile** tab.</span></span>
   - <span data-ttu-id="2bddb-188">Selecteer een technisch connectorprofiel in het veld **Profielnummer**.</span><span class="sxs-lookup"><span data-stu-id="2bddb-188">Select a connector technical profile in the **Profile number** field.</span></span>
   
     >[!NOTE]
     > <span data-ttu-id="2bddb-189">U kunt verschillende technische profielen toevoegen aan een hardwareprofiel.</span><span class="sxs-lookup"><span data-stu-id="2bddb-189">You can add several technical profiles to a hardware profile.</span></span> <span data-ttu-id="2bddb-190">Dit wordt echter niet ondersteund als een hardwareprofiel meer dan één snijpunt met een connectorgroep heeft.</span><span class="sxs-lookup"><span data-stu-id="2bddb-190">However, this is not supported if a hardware profile has more than one intersection with any connector group.</span></span> <span data-ttu-id="2bddb-191">Als u onjuiste instellingen wilt voorkomen, is het raadzaam dat u het registratieproces valideert na het bijwerken van alle hardwareprofielen.</span><span class="sxs-lookup"><span data-stu-id="2bddb-191">To avoid incorrect settings, it’s recommended that you validate the registration process after updating all the hardware profiles.</span></span>

